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

## 📚 What I Learned

- Basic Prometheus architecture
- Node Exporter and Linux metrics
- PromQL queries
- Creating Grafana dashboards
- Configuring Grafana alerts
- Running monitoring tools using Docker
- Basic Linux server monitoring

## 👨‍💻 Project Purpose

This project was created as a hands-on DevOps learning project to understand the fundamentals of infrastructure monitoring and alerting.
