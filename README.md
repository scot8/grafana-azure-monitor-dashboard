# 📊 Ubuntu Server Monitoring Dashboard with Grafana & Azure Monitor

Monitor, visualize, and analyze real-time performance metrics of a cloud-hosted Ubuntu server using **Grafana** integrated with **Azure Monitor** — authenticated securely through **Managed Identity**.

---

## 🧠 Overview

This project sets up a modern observability stack to monitor an Ubuntu VM running on Microsoft Azure. Using Grafana as the front-end and Azure Monitor as the metrics provider, the dashboard offers real-time insights into system health, including CPU usage, memory availability, disk activity, and network traffic.

---

## ⚙️ Stack

- 🐧 **Ubuntu Server 20.04 LTS** (Azure-hosted)
- 📈 **Grafana v11.5.2**
- ☁️ **Azure Monitor**
- 🔐 **Azure Managed Identity (RBAC secured)**
- 🧰 **Linux (CLI), systemd, SSH**

---

## 🚀 Features

- 🔍 Real-time visualization of key server performance metrics
- ✅ Secure authentication via Azure Managed Identity
- 📊 Custom Grafana dashboard with threshold-based panel customization
- 🔄 Fully cloud-native and production-scalable approach

---

## 🔧 Setup Highlights

### ✅ Azure VM Configuration

- **OS:** Ubuntu Server 20.04
- **Public IP + SSH enabled**
- **Port 3000 opened** for Grafana access
- **System Assigned Managed Identity** activated
- Assigned roles:
  - `Monitoring Reader` (Azure Monitor)
  - `Reader` (Subscription)

### 📦 Grafana Installation

```bash
sudo apt-get update
sudo apt-get install -y grafana
sudo systemctl start grafana-server
sudo systemctl enable grafana-server
```

### 🔐 Managed Identity Integration

In `/etc/grafana/grafana.ini`:

```ini
[azure]
managed_identity_enabled = true
auth_type = managed_identity
```

After restarting Grafana, Azure Monitor was added as a data source using Managed Identity — no client secrets or credentials needed.

---

## 📊 Dashboard Metrics

The Grafana dashboard includes panels for:

- **🧠 CPU Usage** (%)
- **💾 Available Memory**
- **📀 Disk Read/Write**
- **🌐 Network In/Out**

All panels include color-coded thresholds and clear labeling for quick diagnostics.

---

## 📸 Screenshots

> *(Add your screenshots in a `/screenshots` folder and link them below)*

- ✅ Azure Monitor Data Source Setup  
- ✅ CPU Usage Panel  
- ✅ Memory Usage Panel  
- ✅ Final Dashboard Overview
![Capture](https://github.com/user-attachments/assets/3161c826-04b9-41af-8cf6-4ed84491001d)
![Capture2](https://github.com/user-attachments/assets/a5250dcb-a207-4d08-b22d-21aeda546a0b)
![Capture3](https://github.com/user-attachments/assets/26820f19-c2a0-4356-a41b-dc0355a7c717)
![Capture4](https://github.com/user-attachments/assets/11633fa6-9d75-4fdb-8d97-c1ee2bb5d977)
![Capture5](https://github.com/user-attachments/assets/5683c210-4c68-4697-a6b7-d0fade8a4fda)
![Capture6](https://github.com/user-attachments/assets/ab4ff9a1-4168-44ad-a75c-da285a01503b)







---

## 💼 What This Demonstrates

- 🔒 Secure, credential-free cloud integration (Managed Identity)
- 🌐 Real-world observability tooling (Grafana + Azure Monitor)
- ☁️ Infrastructure monitoring at scale
- 💡 Ability to configure, visualize, and

---

