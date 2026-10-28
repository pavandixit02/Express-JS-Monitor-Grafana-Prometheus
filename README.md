# Node.js Monitoring with Prometheus and Grafana

A hands-on monitoring project that demonstrates how to observe a Node.js application using **Prometheus** and **Grafana**. The application exposes monitoring metrics, Prometheus collects the metrics, and Grafana presents them in dashboards for easier analysis.

> For the complete implementation steps and configuration details, follow **[Rull-Book.md](./Rull-Book.md)**. This README provides a clear project overview and links to the included evidence.

## Project Overview

This project connects a Node.js application to a monitoring stack so application activity and metrics can be collected and visualized.

- **Node.js** runs the application and exposes metrics for monitoring.
- **Prometheus** collects and stores the metrics based on its scrape configuration.
- **Grafana** uses Prometheus as a data source to visualize the collected metrics in dashboards.

## Technology Stack

| Technology | Role |
|---|---|
| **Node.js** | Runs the application being monitored |
| **Prometheus** | Collects and stores application metrics |
| **Grafana** | Visualizes metrics through dashboards |
| **Prometheus configuration** | Defines the monitoring target and collection settings |

## Architecture

```text
                  Node.js Application
                         |
                         | Exposes metrics
                         v
                     Prometheus
                  Scrapes and stores
                         |
                         | Data source
                         v
                      Grafana
                  Dashboards / Panels
```

## Project Structure

```text
.
├── Config_file-prometheus_yml.png
├── Output-Grafana.png
├── Output-prometheus.png
├── package.json
├── package-lock.json
├── Rull-Book.md
├── run-localhost.png
├── run-localhost-with-matric.png
├── server.js
├── server_js.png
└── Terminal-Commands.png
```

## How It Works

1. **Run the Node.js application.** The application provides the service and its monitoring metrics.
2. **Configure Prometheus.** Prometheus is set up to collect metrics from the intended application endpoint.
3. **Collect metrics.** Prometheus periodically scrapes the configured target and stores the results.
4. **Connect Grafana.** Grafana uses Prometheus as its data source.
5. **Visualize the results.** Dashboards and panels display the metrics, making application behavior easier to inspect.

The exact setup and configuration details are documented in **[Rull-Book.md](./Rull-Book.md)**.

## Project Evidence

### Application Running Locally

![Node.js application running locally](./run-localhost.png)

### Node.js Application with Metrics

![Node.js application with metrics](./run-localhost-with-matric.png)

### Application Server Implementation

![Node.js server implementation](./server_js.png)

### Prometheus Configuration

![Prometheus configuration](./Config_file-prometheus_yml.png)

### Prometheus Metrics Output

![Prometheus output](./Output-prometheus.png)

### Grafana Dashboard

![Grafana dashboard output](./Output-Grafana.png)

### Terminal and Setup

![Terminal commands used during setup](./Terminal-Commands.png)

## Key Learning Outcomes

- Understanding the role of application metrics in monitoring.
- Instrumenting a Node.js application for metrics collection.
- Understanding how Prometheus scrapes and stores metrics.
- Connecting Grafana to Prometheus as a data source.
- Visualizing application metrics with Grafana dashboards.
- Following a monitoring workflow from application instrumentation to visualization.

## Configuration Reference

For the full setup procedure, required packages, configuration contents, and run instructions, refer to **[Rull-Book.md](./Rull-Book.md)**. Use that document as the source of truth for the exact steps and configuration used in this project.

## Future Improvements

- Add more application and runtime metrics where useful.
- Create dashboards for request rate, errors, and response time if those metrics are available.
- Configure alerting for important thresholds.
- Add service health checks and monitoring for deployment environments.
- Document metric names, labels, and dashboard panels.

---

**Project Focus:** Node.js · Prometheus · Grafana · Application Monitoring · Observability
