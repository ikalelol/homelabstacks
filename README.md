# Homelab Docker Stack WORK IN PROGRESS

My personal homelab setup powered by Docker, focused on networking, system tools, media management, and remote access—all running across a few small devices with minimal budget.





##  Docker Stack

| Category     | Name                                                                 | Purpose                                |
|--------------|----------------------------------------------------------------------|----------------------------------------|
| Networking   | [Adguard](https://github.com/AdguardTeam/AdGuardHome)               | Primary DNS                            |
|              | [Adguard 2](https://github.com/AdguardTeam/AdGuardHome)             | Backup DNS (running on Proxmox)        |
|              | [nginx-proxy](https://github.com/nginx-proxy/nginx-proxy)           | Reverse proxy for hosted services      |
|              | [Twingate](https://www.twingate.com/)                                | Personal VPN                           |
|              | [Tailscale](https://tailscale.com/)                                  | Secondary VPN (mesh VPN)               |
|              | [Cloudflared tunnel](https://www.cloudflare.com/)                    | External Access to hosted services      |
| Applications | [IT-Tools](https://github.com/CorentinTh/it-tools)                  | Swiss army knife for IT tools          |
|              | [upsnap](https://github.com/seriousm4x/UpSnap)                      | Wake-on-LAN management tool            |
|              | [Portainer](https://www.portainer.io/)                               | Container management UI                |
|              | [rr's stack](https://wiki.servarr.com/)                              | Media management suite                 |
|              | [qBittorrent](https://hub.docker.com/r/linuxserver/qbittorrent)     | Torrent client with VPN integration    |
|              | [NZBGet](https://nzbget.net/)                                        | NZB downloader for Usenet              |
|              | [Homarr](https://github.com/ajnart/homarr)                          | Dashboard/homepage for fast navigation |
|              | [Plex](https://www.plex.tv/)                                         | Media Software to watch from multitude of devices |
|              | [Jellyfun](https://jellyfin.org/)                                    | Alternate Media Software for friends that use Jellyfin |

---

###  Future Consideration List

| Category       | Name                                                                   | Purpose                                                                 |
|----------------|------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Utilities      | [Mealie](https://mealie.io/)                                           | Self-hosted recipe manager with meal planning and shopping lists         |
|                | [File Browser](https://filebrowser.org/)                               | File management interface for your server via browser                    |
|                | [Stirling PDF](https://www.stirlingpdf.com/)                           | All-in-one self-hosted PDF toolkit (merge, split, OCR, more)             |
| Monitoring     | [Uptime Kuma](https://uptime.kuma.pet/)                                | Self-hosted uptime monitoring tool with status pages                     |
| Automation     | [n8n](https://n8n.io/)                                                  | Workflow automation tool with node-based UI                              |
| AI             | [OpenWebUI](https://github.com/open-webui/open-webui)                  | Self-hosted web interface for LLMs (like OpenAI, LM Studio, etc.)        |
| Authentication | [Authentik](https://goauthentik.io/)                                   | Identity provider and SSO platform with OAuth2, SAML, LDAP               |
| Networking     | [Traefik](https://traefik.io/)                                         | Reverse proxy and load balancer with dynamic config & TLS                |






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
| Deco X55 (x3)          | Main wireless mesh network (⚠️ personally don't recommended for homelab) |

###  Future Upgrade Plans

-  Replace Deco with **Ubiquiti Dream Router 7** or **UDM Pro**  
  - Goal: Full control, better VLAN, and scalability for homelab networking


## 📌 Notes

- DNS redundancy with Adguard (main + Proxmox backup)
- VPN options for flexibility: Twingate (zero trust) and Tailscale (mesh)
- Service access simplified using Homarr dashboard
- No external hosting—everything self-hosted at home
- Cloudflare tunnel allows me to expose services without exposing ports


> 💬 *Suggestions welcome! Feel free to fork or open an issue if you're building something similar.*
