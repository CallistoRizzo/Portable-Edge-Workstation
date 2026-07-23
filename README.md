# Portable Edge Workstation
 
This workstation is a portable, battery-powered Raspberry Pi built for IT administration, field diagnostics, and offline computing.
 
Rather than relying on cloud services, the system is designed to remain fully functional without Internet connectivity while seamlessly reconnecting to remote infrastructure whenever a trusted network becomes available.
 
The project emphasizes portability, reliability, and lightweight system administration tools inside a compact hardware platform.

## Dashboard

The onboard dashboard provides real-time visibility into system health. Designed to remain fully functional even when the workstation is completely disconnected from the internet, providing a centralized control and information layer for the device. 

**Live metrics include:**
- system health overview
- current uptime
- local service access
- offline documentation library 
- local map and gps integration

> 📸 *(Insert dashboard screenshot here)*

## Architecture

```
                   Portable Edge Workstation
                             │
            ┌────────────────┴────────────────┐
            │                                 │
   Offline Environment               Connected Environment
            │                                 │
 ┌──────────┼──────────┐              ┌───────┴───────┐
 │          │          │              │               │
Docs      Tools    Utilities      Tailscale     Remote Access
 │          │          │
 └──────────┼──────────┘
            │
  Local Operations Layer
            │
  Web Dashboard Interface
            │
 ┌──────────┼──────────┐
 │          │          │
System    Storage   Services
Metrics   Status    Controls
```

## Software Stack

| Software             | Role                    | 
|----------------------|-------------------------|
| Debian 12 (bookworm) | Base Distribution       |
| Nginx                | Local Web Server        |
| HTML/CSS             | Dashboard Interface     |
| JavaScript           | Live Dashboard Logic    |
| Node Exporter        | System Metrics          |
| Prometheus           | Metrics Collection      |
| Tailscale            | Secure Remote Access    |

## Hardware

| Component          | Purpose                  |
|--------------------|--------------------------|
| Raspberry Pi       | Primary compute platform |
| Portable 2K Display| Field workstation display|
| Battery Pack       | Portable power source    |
| Wireless Keyboard  | Compact input device     |
| Protective Case    | Portable enclosure       |

## Project Structure
 
```
Nomad/
│
├── README.md
│
│
├── dashboard/
│   ├── index.html
│   ├── dashboard.js
│   ├── style.css
│   └── assets/
│       └── icons/
│
├── monitoring/
│   ├── prometheus.yml
│   ├── node_exporter/
│   │   └── service-file
│   └── scripts/
│       ├── disk-check.sh
│       ├── system-info.sh
│       └── health-check.sh
│
├── offline/
│   ├── documentation/
│   │   ├── README.md
│   │   └── sources.md
│   │
│   ├── maps/
│   │   └── README.md
│   │
│   └── knowledge-base/
│       └── README.md
│
├── tools/
│   ├── networking/
│   │   ├── README.md
│   │   └── scripts/
│   │
│   ├── administration/
│   │   ├── README.md
│   │   └── scripts/
│   │
│   └── recovery/
│       └── README.md
│
├── networking/
│   ├── tailscale/
│   │   └── setup.md
│   │
│   └── configuration/
│       └── network-notes.md
│
├── scripts/
│   ├── install.sh
│   ├── update.sh
│   └── backup.sh
│
├── screenshots/
│   ├── workstation.jpg
│   ├── dashboard.png
│   └── architecture.png
│
└── hardware/
    ├── parts-list.md
    └── wiring.md
```

## Roadmap

### Completed 
- [x] Responsive dashboard
- [x] Local documentation library
- [x] Live CPU monitoring
- [x] Live memory monitoring
- [x] Live disk monitoring
- [x] System uptime display
- [x] Prometheus integration
- [x] Node Exporter integration
- [x] Mobile interface
- [x] Offline operation

### Planned
- [ ] Network diagnostics tookit
- [ ] local file management
- [ ] emergency recovery tools
- [ ] local AI assistanct interface
- [ ] SSH connection manager
 
