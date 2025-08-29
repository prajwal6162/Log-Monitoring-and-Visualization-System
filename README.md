This project demonstrates end-to-end monitoring of:

A website (uptime, SSL, latency)

The server hosting the website (CPU, RAM, Disk, etc.)

using Prometheus, Node Exporter, Blackbox Exporter, and Grafana.

⚙️ Tools & Components
1. Prometheus

A time-series database for metrics.

Collects metrics from exporters via /metrics endpoints.

Stores data in TSDB (Time Series Database).

Query language: PromQL.

Default port: 9090

2. Exporters

Exporters collect metrics from different systems and expose them for Prometheus.

Node Exporter

Scrapes metrics from the server (CPU, RAM, Disk, Network).

Runs on port 9100.

Blackbox Exporter

Scrapes metrics from websites/endpoints (SSL expiry, uptime, response time, DNS, TCP, ICMP).

Runs on port 9115.

3. Grafana

Visualization and dashboarding tool.

Connects to Prometheus as a data source.

Provides customizable dashboards for metrics.

Default port: 3000

🔑 Required Open Ports

To run this stack successfully, the following ports must be accessible:

Port	Protocol	Purpose
3000	TCP	Grafana UI
9090	TCP	Prometheus UI
9100	TCP	Node Exporter
9115	TCP	Blackbox Exporter
80	HTTP	Website monitoring
443	HTTPS	Website monitoring
22	SSH	Server access (if needed)
587	TCP	(Optional) SMTP alerts via Prometheus Alertmanager