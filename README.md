#Offtrack
# 🎵 DIY Music Player (FLAC/MP3 + Bluetooth)

A Raspberry Pi–powered iPod-style music player that supports FLAC and MP3 playback, Bluetooth audio output (AAC), and touchscreen or physical controls.

## ✅ Features
- High-quality FLAC + MP3 support
- Bluetooth output (works with Denon AVR-X1700H)
- Optional wired headphone output via I2S DAC
- Touchscreen or physical button UI
- Local song storage (SD card or USB drag-and-drop)

## 📦 Hardware Used
- Raspberry Pi Zero 2 W
- PCM5102 I2S DAC
- 2.8" SPI Touchscreen
- TP4056 charging + LiPo battery
- 3D-printed or custom case

## 🛠 Software Stack
- Python 3
- PulseAudio + BlueZ for Bluetooth
- mpg123 or ffmpeg for audio
- Tkinter or Pygame for UI

## 🏁 Getting Started

### 1. Install Dependencies
```bash
sudo apt update
sudo apt install python3-pip mpg123 pulseaudio bluez git
pip3 install -r requirements.txt
```

| Folder       | Purpose                             |
| ------------ | ----------------------------------- |
| `ui/`        | UI code (touchscreen/buttons)       |
| `audio/`     | Playback functions                  |
| `bluetooth/` | Auto-connect & device pairing logic |
| `utils/`     | File handling, config, metadata     |
| `assets/`    | Icons, sample music, album art      |
| `config/`    | Settings file (`settings.json`)     |



