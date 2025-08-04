# 🎵 Offtrack – DIY Smart Music Player

**Offtrack** is a Raspberry Pi–powered iPod-style music player designed for high-quality offline listening. Built to ditch Spotify and regain control over your music library, it supports **FLAC/MP3 playback**, **Bluetooth streaming**, and even learns from your behavior using lightweight **reinforcement learning techniques**.

---

## ✅ Features
- High-quality **FLAC + MP3** audio playback
- **Bluetooth output** (AAC codec – works with Denon AVR-X1700H)
- Optional **wired headphone output** via I2S DAC
- Touchscreen or physical button interface
- **Local song storage** (via SD card or USB drag-and-drop)
- **Skip pattern tracking** — recommends song removals you skip often
- **Adaptive power management** — extends battery life using learned policy

---

## 🎯 RL-Inspired Smart Behavior

| Module                     | Purpose                                                        |
|----------------------------|----------------------------------------------------------------|
| 🧠 `PowerManager`          | Learns to optimize playback, screen dimming, and pause states to extend battery life without annoying the user |
| 🎶 `SkipTracker`           | Tracks play/skip rates and prompts to remove songs you consistently skip |
| 🎓 RL Concepts             | Q-learning, multi-armed bandits, action-reward loops           |

These modules showcase embedded RL-style reasoning, bridging music tech and autonomous system design — ideal for embedded robotics or human-adaptive agents.

---

## 📦 Hardware Used
- **Raspberry Pi Zero 2 W**
- **PCM5102 I2S DAC** (for headphone output)
- **2.8" SPI Touchscreen** (or GPIO buttons)
- **TP4056 charging circuit** + **LiPo battery**
- Custom or 3D-printed enclosure

---

## 🛠 Software Stack
- Python 3
- PulseAudio + BlueZ (Bluetooth stack)
- `mpg123` or `ffmpeg` (audio playback)
- `Tkinter`, `PyGame`, or `Kivy` (UI frontend)
- `json`, `random`, `time` (policy/state tracking)

---

## 🏁 Getting Started

### 1. Install System Dependencies
```bash
sudo apt update
sudo apt install python3-pip mpg123 pulseaudio bluez git

2. Install Python Requirements

pip3 install -r requirements.txt

3. Run the Player

python3 player.py

```
## 📂 File Structure

| Folder       | Purpose                                      |
|--------------|----------------------------------------------|
| `ui/`        | UI code (touchscreen/buttons)                |
| `audio/`     | Audio playback logic                         |
| `bluetooth/` | Bluetooth setup and reconnect logic          |
| `rl/`        | Smart skip tracking + power policy (RL)      |
| `utils/`     | File handling, metadata, system I/O          |
| `assets/`    | Icons, album art, sample music               |
| `config/`    | User settings and learned policies (JSON)    |

---

## 🚧 Planned Features

- [ ] Playlist support  
- [ ] Shuffle and repeat modes  
- [ ] Album art display  
- [ ] Web-based drag-and-drop upload interface  
- [ ] Offline RL training via simulated playback environment

