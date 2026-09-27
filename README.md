# Linux Server Monitoring using Prometheus and Grafana

## 📌 Project Overview

This project demonstrates basic Linux server monitoring using Prometheus, Node Exporter, Grafana, and Docker.

The monitoring setup collects Linux system metrics and displays them through a Grafana dashboard. CPU and RAM alerts were also configured to detect high resource usage.

## 🏗️ Architecture

Linux Server
     ↓
Node Exporter
     ↓
Prometheus
     ↓
Grafana
     ↓
Dashboard & Alerts

## 🛠️ Technologies Used

- Linux (RHEL)
- Docker
- Prometheus
- Node Exporter
- Grafana
- PromQL

### Grafana Dashboard

![Grafana Dashboard](Grafana%20Dashboard.png)

### CPU Usage

![CPU Usage graph](CPU%20Usage%20graph.png)

### CPU Alert

![CPU Alerts firing](CPU%20Alerts%20firing.png)## 🚨 Alerts

Configured Grafana alerts for:

- High CPU Usage
- High RAM Usage

The alert threshold was configured at 80%.

CPU alerting was tested by generating temporary CPU load and verifying that the alert changed to a firing state.

## 🐳 Docker Containers

The monitoring components were deployed using Docker containers:

- Prometheus
- Grafana
- Node Exporter

## ⚙️ Prometheus Configuration

Prometheus was configured to scrape metrics from Node Exporter.

Example target:

`192.168.139.128:9100`

## 🔄 Monitoring Flow

1. Node Exporter collects Linux system metrics.
2. Prometheus scrapes and stores the metrics.
3. Grafana connects to Prometheus as a data source.
4. Grafana visualizes the metrics through dashboards.
5. Grafana Alerting monitors resource thresholds.

## 🔧 How I Built This Project

### 1. Set Up Docker

Installed and verified Docker on the RHEL Linux server.

### 2. Deploy Node Exporter

Ran Node Exporter in a Docker container to collect Linux system metrics such as CPU, memory, and network statistics.

### 3. Configure Prometheus

Created a Prometheus configuration file and configured Node Exporter as a scrape target:

`192.168.139.128:9100`

Prometheus was then started using Docker.

### 4. Set Up Grafana

Deployed Grafana using Docker and connected it to Prometheus as a data source.

### 5. Create Monitoring Dashboard

Created Grafana panels using PromQL queries to monitor:

- CPU Usage
- RAM Usage
- Disk Usage
- Network Traffic

### 6. Configure Alerts

Created Grafana alerts for:

- High CPU Usage — 80% threshold
- High RAM Usage — 80% threshold

### 7. Test Alerting

Generated temporary CPU load on the Linux server and verified that the CPU alert changed to a firing state.

After stopping the CPU load, the system returned to normal.

### 8. Document the Project

Added the Prometheus configuration, Grafana screenshots, and project documentation to GitHub.

## 👨‍💻 Project Purpose

This project was created as a hands-on DevOps learning project to understand the fundamentals of infrastructure monitoring and alerting.
