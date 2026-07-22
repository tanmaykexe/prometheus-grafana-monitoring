# Monitoring Architecture

```mermaid
graph TD

A[Linux Server]
-->
B[Node Exporter]

B
-->
C[Prometheus]

C
-->
D[Grafana]

D
-->
E[Real-Time Dashboard]
```
