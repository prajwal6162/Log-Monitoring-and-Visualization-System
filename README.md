# 📊 Log Monitoring and Visualization System

This project demonstrates monitoring of both a **website** and the **server on which the website is running** using Prometheus, Node Exporter, Blackbox Exporter, and Grafana.

---

## 🚀 Tools Used

### 1. Prometheus
- Acts as a **data source**.
- Collects and stores **time series data (metrics)** in its own database **TSDB**.
- Uses **PromQL** for querying.
- Scrapes metrics from `/metrics` endpoints.

### 2. Exporters
Exporters collect metrics and expose them for Prometheus.

- **Node Exporter**  
  - Collects server metrics such as **CPU, RAM, Disk usage, etc.**  
  - Runs on port **`9100`**.  
  - Must be installed manually on the server.  

- **Blackbox Exporter**  
  - Monitors websites for **availability, SSL, and response time**.  
  - Sends requests to websites and exposes results.  

### 3. Grafana
- A **visualization tool** for metrics collected by Prometheus.  
- Connects to Prometheus as a data source.  
- Provides dashboards and alerts.

---

## 📡 Ports to Open

| Port | Protocol | Description |
|------|----------|-------------|
| 9100 | TCP      | Node Exporter (server metrics) |
| 9090 | TCP      | Prometheus server |
| 3000 | TCP      | Grafana dashboard |
| 80   | HTTP     | Website access |
| 443  | HTTPS    | Secure website access |
| 22   | SSH      | Secure server login |
| 587  | TCP      | Custom (mail/alerts if configured) |

---

## 🛠️ Project Workflow

1. **Node Exporter** installed on the server to expose system metrics.  
2. **Blackbox Exporter** configured to monitor a website (up/down, SSL, latency).  
3. **Prometheus** scrapes data from exporters via `/metrics`.  
4. **Grafana** connects to Prometheus to visualize the data in dashboards.  

---

## 📸 Screenshots


![Grafana Dashboard](./screenshots/Grafana_application_health.png)  
![Prometheus Targets](./screenshots/prometheus.png)

---


