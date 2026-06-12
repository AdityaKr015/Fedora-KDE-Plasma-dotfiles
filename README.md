# Fedora KDE Plasma Dotfiles

> My personal KDE Plasma rice on Fedora — configs, themes, and setup guide.

![KDE Plasma](https://img.shields.io/badge/KDE_Plasma-6.6.5-blue?style=for-the-badge&logo=kde&logoColor=white)
![Fedora](https://img.shields.io/badge/Fedora-44-51A2DA?style=for-the-badge&logo=fedora&logoColor=white)
![Theme](https://img.shields.io/badge/Theme-Catppuccin_Mocha_Lavender-CBA6F7?style=for-the-badge)
![Icons](https://img.shields.io/badge/Icons-Tela_Circle-89B4FA?style=for-the-badge)

---

## Preview

![Desktop Preview](./preview.png)

---

## System Info

| Component | Details |
|-----------|---------|
| **OS** | Fedora 44 |
| **DE** | KDE Plasma 6.6.5 |
| **Theme** | Catppuccin Mocha Lavender Classic |
| **Icons** | Tela Circle |
| **Terminal** | Konsole |
| **Font** | Inter 8pt |
| **Wallpaper** | Slideshow (custom collection) |

---

## What's in This Repo

```
kde/
├── .config/
│   ├── kdeglobals                               # Colors, fonts
│   ├── kwinrc                                   # Blur, transparency, window effects
│   ├── plasmarc                                 # Plasma settings
│   ├── plasmashellrc                            # Panel layout
│   ├── plasma-org.kde.plasma.desktop-appletsrc  # Widgets + panel config
│   ├── kcminputrc                               # Mouse/input settings
│   ├── kscreenlockerrc                          # Lock screen settings
│   ├── kglobalshortcutsrc                       # Keyboard shortcuts
│   ├── kcmfonts                                 # Font settings
│   ├── krunnerrc                                # KRunner settings
│   └── konsolerc                                # Konsole window settings
└── .local/share/konsole/
    ├── aditya.profile                           # Konsole profile
    └── WhiteOnBlack.colorscheme                 # Konsole color scheme
```

---

## Installation

### 1. Clone This Repo

```bash
git clone https://github.com/AdityaKr015/Fedora-KDE-Plasma-dotfiles.git
cd Fedora-KDE-Plasma-dotfiles
```

### 2. Copy Config Files

```bash
cp -r kde/.config/* ~/.config/
cp -r kde/.local/share/konsole/* ~/.local/share/konsole/
```

> ⚠️ This will overwrite your existing KDE configs. Back up your current configs first if needed.

---

## Theme Setup

### Catppuccin KDE

Check the [Catppuccin KDE repo](https://github.com/catppuccin/kde) for previews of all flavours and colour schemes before installing.

```bash
git clone --depth=1 https://github.com/catppuccin/kde catppuccin-kde
cd catppuccin-kde
./install.sh
```

Follow the prompts:-

Choose your flavour and accent colour. I use **Mocha + Lavender + Classic**.

After installing:
- Go to **System Settings -> Global Theme** and select Catppuccin
- Go to **Colors & Themes -> Window Decorations** to customise further

---

### Tela Circle Icons

Check the [Tela Circle repo](https://github.com/vinceliuice/Tela-circle-icon-theme) for previews.

```bash
git clone https://github.com/vinceliuice/Tela-circle-icon-theme.git
cd Tela-circle-icon-theme
./install.sh --help   # See available variants
./install.sh -a -c    # Install all variants + circular style (what I use)
```

After installing:
- Go to **System Settings -> Global Theme -> Icons** and select your preferred Tela variant

---

## Widgets

| Widget | Purpose |
|--------|---------|
| **KDE Control Station** | System tray popup (pre-installed, just add from widget menu) |
| **Thermal Monitor** | CPU temperature on desktop |
| **Clear Clock** | Clean clock widget on desktop |
| **PlasMusic Toolbar** | Music player controls in taskbar (album art, seek bar, prev/next/pause) |

To add widgets: **Right click on desktop -> Add or Manage Widgets**

> For system tray: right click taskbar -> Configure, move items to popup as preferred.

---

## 🕐 Clock Settings

Using the **Digital Clock** widget with a custom date format:

- Date format: `Custom` → `MMM d,ddd` (shows like `Jun 8, Mon`)
- Text display: `Manual` → Inter 8pt
- Show date: Always beside time

![Clock Settings](Clock%20Settings/clock-setting.webp)

---

## 🖼️ Wallpapers

Wallpapers are set as a **slideshow** — mix of downloaded ones and my own.
Some wallpapers sourced from [this collection](https://github.com/catppuccin/wallpapers).

To set up slideshow: **Right click desktop → Configure Desktop and Wallpaper → Slideshow**

---

## 🚀 App Launcher Icon

Right click on the **Application Launcher** in the taskbar → **Configure** → change the icon to whatever you like.

---

## otes

- Catppuccin and Tela are installed system-wide via their install scripts — those files are not included in this repo, just follow the setup steps above
- If KDE looks off after copying configs, log out and log back in (or restart plasmashell: `plasmashell --replace &`)
- Single-channel RAM users: some blur/transparency effects may impact performance

---

## Credits

- [Catppuccin KDE](https://github.com/catppuccin/kde)
- [Tela Circle Icon Theme](https://github.com/vinceliuice/Tela-circle-icon-theme)
- [Catppuccin Wallpapers](https://github.com/catppuccin/wallpapers)
