# 📺 Media Hub Card

[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg)](https://github.com/hacs/integration)
[![GitHub release](https://img.shields.io/github/v/release/Liionboy/ha-media-hub-card)](https://github.com/Liionboy/ha-media-hub-card/releases)
[![License](https://img.shields.io/github/license/Liionboy/ha-media-hub-card)](LICENSE)

**Hub media pentru toată casa.** TV, HomePod, Spotify, Plex — now playing, controale, favorite, volum.

## ✨ Features

- Now Playing display cu controale
- Player list cu status (playing/paused/off)
- Play/Pause/Volume controls
- Favorite apps (Netflix, YouTube, Plex, Spotify)
- Click-through la detalii
- Visual config editor
- HACS ready

## 📦 Installation

### Option 1: HACS (recommended)

1. Open **HACS** → **Frontend** → ⋮ → **Custom Repositories**
2. Add repository: `Liionboy/ha-media-hub-card`
3. Category: **Lovelace** → Click **Add**
4. Find **Media Hub Card** in HACS → Click **Install**
5. Go to **Settings** → **Dashboards** → **Resources** → **Add**:
   ```
   /hacsfiles/ha-media-hub-card/ha-media-hub-card.js
   type: JavaScript Module
   ```
6. **Restart Home Assistant** (or clear browser cache with Ctrl+Shift+R)
7. Edit your dashboard → Add card → Search for `ha-media-hub-card`

### Option 2: Manual Install

1. Download `ha-media-hub-card.js` from [Releases](https://github.com/Liionboy/ha-media-hub-card/releases/latest)
2. Copy the file to your Home Assistant `/config/www/` directory
3. Go to **Settings** → **Dashboards** → **Resources** → **Add**:
   ```
   /local/ha-media-hub-card.js
   type: JavaScript Module
   ```
4. **Restart Home Assistant** (or clear browser cache)
5. Edit your dashboard → Add card → Search for `ha-media-hub-card`

### Option 3: Manual via YAML

Add to your `configuration.yaml`:
```yaml
lovelace:
  resources:
    - url: /local/ha-media-hub-card.js
      type: module
```

## ⚙️ Configuration

### Minimal

```yaml
type: custom:ha-media-hub-card
```

### Full Configuration

```yaml
type: custom:ha-media-hub-card
title: 📺 Media Hub
show_now_playing: true
show_favorites: true
entities:
  - media_player.living_tv
  - media_player.homepod_bucatarie
  - media_player.hisense_40a3he_6hl51674_smart_tv
favorites:
  - name: Netflix
    icon: mdi:netflix
  - name: YouTube
    icon: mdi:youtube
  - name: Plex
    icon: mdi:plex
  - name: Spotify
    icon: mdi:spotify
```

## 📄 License

MIT
