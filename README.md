# 🎨 Homelab Excalidraw

Collaborative virtual whiteboard and diagramming tool for the `roadtotech.me` homelab cluster.

---

## 🏗️ Architecture & Requirements

- **Proxy Network**: Attached to external `proxy-net`
- **Domain**: `excalidraw.roadtotech.me`
- **Target Port**: `80` (HTTP Web), Socket.io backend support

---

## ⚙️ Configuration & Metadata (`app.yaml`)

```yaml
name: "excalidraw"
aliases:
  - "draw"
  - "sketch"
domain: "excalidraw.roadtotech.me"
description: "Collaborative Whiteboarding & Sketching Tool"
visible: true
auth: false
networks:
  - proxy-net
homepage:
  title: "Excalidraw"
  group: "Knowledge & Notes"
  icon: "excalidraw.png"
  container: "excalidraw-excalidraw-1"
  weight: 20
```

---

## 🚀 Deployment

### Via Orchestrator (`appctl`)
```bash
appctl up excalidraw
# or using shortcut alias
appctl up draw
```

### Manual Deployment
```bash
docker compose up -d
```

---

## 📄 License
This repository is released into the public domain under the [Unlicense](LICENSE).
