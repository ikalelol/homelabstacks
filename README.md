# Homelab Docker Stack WORK IN PROGRESS

My personal homelab setup powered by Docker, focused on networking, system tools, media management, and remote access—all running across a few small devices with minimal budget.





##  Docker Stack

| Category     | Name         | Purpose                                |
|--------------|--------------|----------------------------------------|
| Networking   | Adguard      | Primary DNS                            |
|              | Adguard 2    | Backup DNS (running on Proxmox)        |
|              | nginx-proxy  | Reverse proxy for hosted services      |
|              | Twingate     | Personal VPN                           |
|              | Tailscale    | Secondary VPN (mesh VPN)               |
| Applications | IT-Tools     | Swiss army knife for IT tools          |
|              | upsnap       | Wake-on-LAN management tool            |
|              | Portainer    | Container management UI                |
|              | rr's stack   | Media management suite                |
|              | qBittorrent  | Torrent client with VPN integration    |
|              | NZBGet       | NZB downloader for Usenet              |
|              | Homarr       | Dashboard/homepage for fast navigation |






## 💻 Hardware

  **Mini PC #1**  
  - Role: Running TrueNAS with Docker containers
  
  **Mini PC #2**  
  - Role: Running Proxmox and backup services


##  Coming Soon

  Old Gaming Desktop  
  - Plan: Convert into NAS with TrueNAS and migrate current data
  - Budget: **None** (brokie currently)


##  Networking Setup

| Device                  | Role                                       |
| -----------------------| ------------------------------------------ |
| AT&T Fiber Gateway     | In passthrough mode for external access    |
| Deco X55 (x3)          | Main wireless mesh network (⚠️ not recommended for homelab) |

###  Future Upgrade Plans

- ✅ Replace Deco with **Ubiquiti Dream Router SE** or **UDM Pro**  
  - Goal: Full control, better VLAN, and scalability for homelab networking


## 📌 Notes

- DNS redundancy with Adguard (main + Proxmox backup)
- VPN options for flexibility: Twingate (zero trust) and Tailscale (mesh)
- Service access simplified using Homarr dashboard
- No external hosting—everything self-hosted at home


> 💬 *Suggestions welcome! Feel free to fork or open an issue if you're building something similar.*
