# 🎨 Homelab Excalidraw

Self-hosted virtual collaborative whiteboard for architecture sketches, visual notes, and diagrams.

Part of the [homelab-core](https://github.com/kiskaadee/homelab-core) cluster ecosystem.

---

## 🏗️ Architecture & Requirements

- **Container Image**: `excalidraw/excalidraw:latest`
- **Proxy**: Traefik (attached to `proxy-net`)
- **Domain**: `excalidraw.arch-services.mywire.org`

---

## ⚙️ Environment Variables

| Variable | Description | Default / Example |
| :--- | :--- | :--- |
| `EXCALIDRAW_DOMAIN` | Whiteboard FQDN | `excalidraw.arch-services.mywire.org` |
| `PROXY_NETWORK` | External Docker network | `proxy-net` |

---

## 🚀 Deployment

### Via Orchestrator (`appctl`)
```bash
appctl up homelab-excalidraw
```

### Manual Deployment
```bash
docker compose up -d
```
