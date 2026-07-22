# 📊 Linux Monitoring with Prometheus & Grafana

<p align="center">

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Monitoring](https://img.shields.io/badge/Monitoring-0052CC?style=for-the-badge)

</p>

---

## 📌 Project Overview

This project demonstrates how to build a production-style Linux monitoring solution using **Prometheus**, **Node Exporter**, and **Grafana**.

The monitoring stack collects system metrics from a Linux machine using **Node Exporter**, stores them in **Prometheus**, and visualizes them through interactive **Grafana dashboards**.

---

## 🏗️ Architecture

```mermaid
graph TD
A[Linux Server] --> B[Node Exporter]
B --> C[Prometheus]
C --> D[Grafana]
D --> E[Monitoring Dashboard]
```

---

## 🚀 Features

- Real-time Linux Monitoring
- CPU Utilization Monitoring
- Memory Monitoring
- Disk Usage Monitoring
- Filesystem Monitoring
- Network Monitoring
- Prometheus Metrics Collection
- Grafana Dashboards
- Infrastructure Observability

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| Linux (WSL) | Host System |
| Prometheus | Metrics Collection |
| Node Exporter | Linux Metrics Exporter |
| Grafana | Dashboard & Visualization |

---

## 📂 Project Structure

```text
prometheus-grafana-monitoring
│
├── prometheus
├── docs
├── screenshots
├── architecture
├── README.md
└── LICENSE
```

---

# 📸 Screenshots

## Prometheus Targets

![Prometheus Targets](screenshots/01-prometheus-targets.png)

---

## Prometheus Query

![Prometheus Query](screenshots/02-prometheus-query.png)

---

## Grafana Dashboard

![Grafana Dashboard](screenshots/03-grafana-dashboard.png)

---

## Grafana Data Source

![Grafana Datasource](screenshots/04-grafana-datasource.png)

---

## Grafana Service Status

![Grafana Service](screenshots/05-grafana-service.png)

---

# 📖 Installation

A complete installation guide is available here:

➡️ **[Installation Guide](docs/installation-guide.md)**

---

# 📚 Skills Demonstrated

- Linux Administration
- Prometheus Configuration
- Grafana Configuration
- Infrastructure Monitoring
- Metrics Collection
- Time-Series Monitoring
- Dashboard Visualization
- Linux Performance Monitoring

---

# 🎯 Learning Outcomes

✔ Installed and configured Prometheus

✔ Configured scrape targets

✔ Installed and configured Node Exporter

✔ Installed and configured Grafana

✔ Connected Grafana with Prometheus

✔ Built real-time infrastructure dashboards

---

# 🔮 Future Improvements

- Docker Compose deployment
- Kubernetes deployment
- Helm Charts
- Alertmanager integration
- Email Alerts
- Slack Notifications
- Multi-node Monitoring

---

## 👨‍💻 Author

**Tanmay Khatri**

GitHub: https://github.com/tanmaykexe

## 📄 License

This project is licensed under the MIT License.
