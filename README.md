# 🎵 gamdl GUI

A free, open-source graphical interface for [gamdl](https://github.com/glomatico/gamdl) —
a command-line tool that downloads Apple Music tracks as high-quality `.m4a` files
with full metadata and cover art embedded, ready to copy to your iPod or any music player.

This GUI wraps gamdl in a friendly Frutiger Aero styled desktop app so you never
have to touch the command line.

---

## ✨ Features

- Clean **Frutiger Aero** visual style — glossy sphere icons, sky-blue gradients, glass panels
- Download **songs, albums, and playlists** from Apple Music
- Output as **256 kbps AAC .m4a** with artist, album, track number, and cover art embedded
- **Auto-deletes lyrics (.lrc) files** after every download
- Saves your cookies path and output folder between sessions
- Live log output so you can watch the download as it happens
- Works on **Windows, Linux, and macOS**

---

## 📋 Requirements

Before running the app you need to install these on your system:

| Requirement | How to install |
|---|---|
| **Python 3.8+** | [python.org](https://www.python.org/downloads/) — tick "Add to PATH" on Windows |
| **FFmpeg** | [ffmpeg.org](https://ffmpeg.org/download.html) — add `bin/` to PATH on Windows |
| **gamdl** | `pip install gamdl` |
| **PyQt6** | `pip install PyQt6` |
| **Apple Music subscription** | [music.apple.com](https://music.apple.com) |

---

## 🚀 How to use

### 1. Export your Apple Music cookies

gamdl needs your browser session to authenticate.

1. Open Chrome or Firefox and go to [music.apple.com](https://music.apple.com)
2. Sign in to your Apple Music account
3. Install a cookie export extension:
   - Chrome / Chromium → **"Get cookies.txt LOCALLY"**
   - Firefox → **"cookies.txt"**
4. While on music.apple.com, click the extension icon and export as `cookies.txt`
5. Save it somewhere you can find it

### 2. Configure the app

- Open the **Settings** tab
- Set your `cookies.txt` path
- Set your output folder (where music will be saved)
- Click **Save Settings**

### 3. Download

- Copy any Apple Music URL (song, album, or playlist)
- Paste it into the URL field in the **Download** tab
- Click **Download**
- Your `.m4a` files appear in your output folder when done

---

## 📦 Installation

### Download a pre-built executable

Head to the [Releases](../../releases) page and download the file for your platform:

- `gamdl-GUI-Windows.exe` — Windows
- `gamdl-GUI-Linux` — Linux (make executable with `chmod +x gamdl-GUI-Linux`)
- `gamdl-GUI-macOS` — macOS

> **Note:** Windows Defender may flag the `.exe` as suspicious — this is a known false positive
> with PyInstaller apps. Right-click → Properties → Unblock, or right-click → Run anyway.

### Run from source

```bash
pip install PyQt6
python gamdl_gui.py
```

---

## 🙏 Credits & Shout-outs

This app would not exist without the following incredible open-source projects and tools:

### Core engine
- **[gamdl](https://github.com/glomatico/gamdl)** by **glomatico** —
  the actual downloader that does all the hard work.
  This GUI is just a pretty face on top of their amazing tool.
  All credit for the downloading functionality goes to them.

### Libraries used
- **[PyQt6](https://www.riverbankcomputing.com/software/pyqt/)** by Riverbank Computing —
  the GUI framework powering all the windows, buttons, and layouts
- **[FFmpeg](https://ffmpeg.org/)** — the legendary audio/video processing engine
  that gamdl uses under the hood
- **[Python](https://www.python.org/)** — the language everything is written in
- **[PyInstaller](https://pyinstaller.org/)** — used to package the app into
  standalone executables for each platform

### Distribution
- **[GitHub Actions](https://github.com/features/actions)** — automatically builds
  Windows, Linux, and macOS executables on every release for free

---

## 🤖 A note on how this was made

This entire project — every line of code, every style decision, every icon, the build
pipeline, and even this README — was created with the help of
**[Claude](https://claude.ai)** by Anthropic, an AI assistant.

I had the idea, described what I wanted, and Claude wrote it.
I am deeply sorry for my own incompetence and for not knowing how to do any of this myself.
Shout out to Claude for having the patience of a saint while I asked the same question
four different ways.

If this app is useful to you, the real heroes are **glomatico** for gamdl and
**Anthropic** for Claude. I just asked nicely.

---

## ⚠️ Legal disclaimer

This tool requires an active Apple Music subscription to function.
Downloading music is intended for **personal archival use only**.
Using this tool to remove DRM protection from Apple Music content may violate
Apple's Terms of Service. The authors take no responsibility for how you use this software.

---

## 📄 License

MIT — do whatever you want with it.
