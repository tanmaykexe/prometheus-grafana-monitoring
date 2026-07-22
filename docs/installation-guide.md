# Installation Guide

## Prerequisites

- Ubuntu / WSL
- Internet Connection
- sudo privileges

---

# Step 1 — Install Node Exporter

Download:

```bash
LATEST=$(curl -s https://api.github.com/repos/prometheus/node_exporter/releases/latest | grep tag_name | cut -d '"' -f4)

wget https://github.com/prometheus/node_exporter/releases/download/${LATEST}/node_exporter-${LATEST#v}.linux-amd64.tar.gz
```

Extract:

```bash
tar -xvf node_exporter*.tar.gz
```

Run:

```bash
cd node_exporter*

./node_exporter
```

Verify:

```bash
curl http://localhost:9100/metrics
```

---

# Step 2 — Install Prometheus

Download:

```bash
LATEST=$(curl -s https://api.github.com/repos/prometheus/prometheus/releases/latest | grep tag_name | cut -d '"' -f4)

wget https://github.com/prometheus/prometheus/releases/download/${LATEST}/prometheus-${LATEST#v}.linux-amd64.tar.gz
```

Extract:

```bash
tar -xvf prometheus*.tar.gz
```

Run:

```bash
cd prometheus*

./prometheus
```

Verify:

```bash
curl http://localhost:9090/-/healthy
```

---

# Step 3 — Configure Prometheus

Update `prometheus.yml`:

```yaml
scrape_configs:
  - job_name: "prometheus"

    static_configs:
      - targets: ["localhost:9090"]

  - job_name: "node-exporter"

    static_configs:
      - targets: ["localhost:9100"]
```

---

# Step 4 — Install Grafana

```bash
sudo apt update

sudo apt install grafana -y

sudo systemctl enable grafana-server

sudo systemctl start grafana-server
```

Verify:

```bash
sudo systemctl status grafana-server
```

---

# Step 5 — Configure Grafana

- Open `http://localhost:3000`
- Login using the admin account
- Add **Prometheus** as the data source
- URL:

```
http://localhost:9090
```

- Click **Save & Test**

---

# Step 6 — Import Dashboard

Dashboard ID:

```
1860
```

Import the dashboard and select the Prometheus data source.

---

# Verification

Prometheus

```
http://localhost:9090
```

Grafana

```
http://localhost:3000
```

Node Exporter

```
http://localhost:9100/metrics
```
