# 🦆 Duck Wi-Fi Monitor

<div align="center">

<pre style="font-size:14px; font-weight:bold; color:#00ffcc; background:#0d1117; padding:20px; border-radius:10px;">
██████╗ ██╗   ██╗ ██████╗██╗  ██╗    ██╗    ██╗██╗███████╗██╗
██╔══██╗██║   ██║██╔════╝██║ ██╔╝    ██║    ██║██║██╔════╝██║
██║  ██║██║   ██║██║     █████╔╝     ██║ █╗ ██║██║█████╗  ██║
██║  ██║██║   ██║██║     ██╔═██╗     ██║███╗██║██║██╔══╝  ██║
██████╔╝╚██████╔╝╚██████╗██║  ██╗    ╚███╔███╔╝██║██║     ██║
╚═════╝  ╚═════╝  ╚═════╝╚═╝  ╚═╝     ╚══╝╚══╝ ╚═╝╚═╝     ╚═╝
                                                             
</pre>

<h3>📡 Duck Wi-Fi Monitor – FastAPI-based OpenWrt Monitoring</h3>

by <b>MozzieGM</b>  
<a href="https://github.com/MozzieGM">github.com/MozzieGM</a>  

</div>

---

## 📖 About

**Duck Wi-Fi Monitor** is a **FastAPI-based system** for monitoring **OpenWrt routers**.  
It collects **DNS logs**, **DHCP leases**, **Wi-Fi station metrics (iw station dump)**, and **router status** in real time, storing everything in **SQLite** and exposing it via a **REST API**.

⚡ The project is still in **development** (*coming soon*), but already includes:
- 🚀 DNS log capture  
- 📡 DHCP monitoring  
- 📶 Full Wi-Fi station stats  
- 🖥️ Router system info (CPU, RAM, uptime)  

---

## ✨ Features (Coming Soon)

- Real-time DNS logging  
- DHCP leases with history (`first_seen` and `last_seen`)  
- Wi-Fi stations with complete metrics (bytes, packets, retries, bitrates, etc.)  
- Router status (CPU usage, memory, uptime, load average)  
- REST API with FastAPI  
- SQLite database with auto-updates  

---

## 📂 Project Structure

```bash
duck_wifi_monitor/
│
├── api/                        # API endpoints
│   ├── dns_routes.py           # DNS log routes
│   ├── network_routes.py       # DHCP + Stations routes
│   ├── router_routes.py        # Router status routes
│   └── routes.py               # Main router registration
│
├── config/                     # Configurations
│   └── settings.py             # IP, password, paths, etc.
│
├── core/                       # Core logic
│   ├── log_parser.py           # DNS log regex + parsing
│   ├── monitor.py              # Real-time DNS capture
│   ├── network_info.py         # DHCP & Wi-Fi Stations via SSH
│   ├── network_monitor.py      # Background monitor (auto-save in DB)
│   ├── router_status.py        # CPU, RAM, uptime & router usage
│   ├── ssh_client.py           # SSH connection to router
│   └── storage.py              # SQLite database management
│
└── db/                         # Database
    └── wifi_logs.db            # SQLite file (auto-created)
│
├── main.py                     # Entry point (API + monitor)
└── estrutura.md                # Structure documentation
```

## 🚀 Installation & Usage (Coming Soon)

```bash
# Clone the repository
git clone https://github.com/MozzieGM/duck-wifi-monitor.git
cd duck-wifi-monitor

# Install dependencies
pip install -r requirements.txt

# Start the system
python main.py
```

## 📜 License

This project will be licensed soon (probably MIT).

<div align="center">

👨‍💻 Developed with ❤️ by MozzieGM
🔗 <a href="https://github.com/MozzieGM">github.com/MozzieGM</a>

</div> ```