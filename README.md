<p align="center">
  <img src="https://raw.githubusercontent.com/hyprwm/Hyprland/main/assets/header.svg" alt="Hyprland" width="600" />
</p>

<p align="center">
  RPM packages for <a href="https://hyprland.org/">Hyprland</a> and the Hypr ecosystem — <strong>Fedora 44+</strong> support.<br>
  Fork of <a href="https://github.com/solopasha/hyprlandRPM">solopasha/hyprlandRPM</a>.
</p>

[![COPR](https://img.shields.io/badge/COPR-eli--xciv%2Fhyprland-blue?logo=fedora)](https://copr.fedorainfracloud.org/coprs/eli-xciv/hyprland/)
[![Fedora](https://img.shields.io/badge/Fedora-42%20%7C%2043%20%7C%2044-294172?logo=fedora)](https://fedoraproject.org/)
[![License](https://img.shields.io/badge/license-GPL--2.0-green)](LICENSE)

---

## 📦 Installation

```bash
sudo dnf copr enable eli-xciv/hyprland
sudo dnf install hyprland
```

> **Note:** `hyprland-git` tracks nightly snapshots and is recommended for the latest fixes.

---

## 🧩 Packages

### Core

| Package | Description |
|---|---|
| [hyprland](https://wiki.hyprland.org/) | A highly customizable dynamic tiling Wayland compositor |
| [hyprland-git](https://wiki.hyprland.org/) | Hyprland — nightly git snapshots |
| [xdg-desktop-portal-hyprland](https://wiki.hyprland.org/Useful-Utilities/Hyprland-desktop-portal/) | XDG desktop portal backend for Hyprland |
| [hyprland-plugins](https://github.com/hyprwm/hyprland-plugins) | Official plugins for `hyprland` |
| [hyprland-plugins-git](https://github.com/hyprwm/hyprland-plugins) | Official plugins for `hyprland-git` |
| [hyprland-contrib](https://github.com/hyprwm/contrib) | Community scripts and utilities for Hypr projects |

### 🔒 Session & System

| Package | Description |
|---|---|
| [hyprlock](https://github.com/hyprwm/hyprlock) | GPU-accelerated screen locking utility |
| [hypridle](https://github.com/hyprwm/hypridle) | Idle daemon for Hyprland |
| [hyprpolkitagent](https://github.com/hyprwm/hyprpolkitagent) | Polkit authentication agent |
| [hyprsysteminfo](https://github.com/hyprwm/hyprsysteminfo) | System information display |
| [uwsm](https://github.com/Vladimir-csp/uwsm) | Universal Wayland Session Manager |

### 🖼️ Wallpaper & Display

| Package | Description |
|---|---|
| [hyprpaper](https://github.com/hyprwm/hyprpaper) | Blazing fast Wayland wallpaper utility with IPC |
| [swww](https://github.com/Horus645/swww) | Efficient animated wallpaper daemon |
| [mpvpaper](https://github.com/GhostNaN/mpvpaper) | Video wallpaper for wlroots compositors |
| [waypaper](https://github.com/anufrievroman/waypaper) | GUI wallpaper manager |
| [hyprsunset](https://github.com/hyprwm/hyprsunset) | Blue-light filter for Hyprland |

### 🛠️ Utilities

| Package | Description |
|---|---|
| [hyprpicker](https://github.com/hyprwm/hyprpicker) | Wayland color picker |
| [hyprshot](https://github.com/Gustash/Hyprshot) | Screenshot utility with mouse support |
| [satty](https://github.com/gabm/Satty) | Screenshot annotation tool |
| [hyprlauncher](https://github.com/hyprwm/hyprlauncher) | Multipurpose launcher / picker |
| [cliphist](https://github.com/sentriz/cliphist) | Wayland clipboard manager |
| [nwg-clipman](https://github.com/nwg-piotr/nwg-clipman) | GTK3 GUI frontend for cliphist |
| [hyprnome](https://github.com/donovanglover/hyprnome) | GNOME-like workspace switching |
| [hyprdim](https://github.com/donovanglover/hyprdim) | Auto-dim inactive windows |
| [pyprland](https://github.com/hyprland-community/pyprland) | Hyprland extensions in Python |
| [hyprland-autoname-workspaces](https://github.com/hyprland-community/hyprland-autoname-workspaces) | Auto-rename workspaces with app icons |

### 🎨 Theming & Widgets

| Package | Description |
|---|---|
| [aylurs-gtk-shell](https://github.com/Aylur/ags) | AGS — GTK widget system (legacy) |
| [aylurs-gtk-shell2](https://github.com/Aylur/ags) | AGS v2 — CLI for Astal-based projects |
| [hyprpanel](https://hyprpanel.com/) | Feature-rich bar/panel for Hyprland |
| [eww-git](https://elkowar.github.io/eww/) | Rust-based widget system (nightly) |
| [waybar-git](https://github.com/Alexays/Waybar) | Highly customizable Wayland bar (nightly) |
| [swaylock-effects](https://github.com/jirutka/swaylock-effects) | Swaylock with visual effects |
| [qt6ct-kde](https://github.com/ilya-fedin/qt6ct) | Qt6 configuration utility with KDE patches |
| [hyprqt6engine](https://github.com/hyprwm/hyprqt6engine) | Qt6 theme provider for Hyprland |

---

## 🔧 Fedora 44 Compatibility

This fork applies patches to build cleanly against **GCC 16** and updated library sonames on Fedora 44:

- **GCC 16 implicit header removals** — `<mutex>`, `<climits>`, `<unistd.h>` added where needed
- **aquamarine** — bumped to 0.11.0; strips `-Wpedantic` for GCC 16 zero-size array errors
- **hyprutils** — bumped to 0.13.0 (soname 9→12)
- **hyprgraphics** — bumped to 0.5.1 (soname 1→4); adds `mesa-libGLES-devel` + `libdrm` build deps
- **hyprtoolkit** — bumped to 0.5.3 (soname 2→5)
- **COPR build method** — `source_build_method: make_srpm` with explicit `--spec` (required for Go/Rust vendor bundles)

---

## 🙏 Credits

- Upstream: [solopasha/hyprlandRPM](https://github.com/solopasha/hyprlandRPM) — original RPM packaging
- [Hyprland](https://hyprland.org/) and the [hyprwm](https://github.com/hyprwm) team for the ecosystem
