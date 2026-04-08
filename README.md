# 🎵 AirWave-Hypr
AirPlay metadata integration for Hyprland (Waybar & Hyprlock).

This project allows you to see what's playing via **Shairport Sync** directly on your **Waybar** and **Hyprlock** screen, providing a seamless AirPlay experience on Linux.

## 🚀 How it Works
1. **Shairport Sync** receives the AirPlay stream and writes metadata to `/tmp/shairport-sync-metadata`.
2. A custom **bash script** parses this metadata to extract the song title.
3. **Waybar** displays the title in your status bar using a custom module.
4. **Hyprlock** can use the same logic to show current media on your lock screen.

## 🛠️ Installation
1. Install `shairport-sync`.
2. Configure `shairport-sync.conf` to enable metadata output.
3. Add the `airplay_title.sh` script to your Waybar scripts folder.
4. Add the custom module to your `waybar/config.jsonc`:
```json
"custom/airplay": {
    "exec": "~/.config/waybar/scripts/airplay_title.sh",
    "interval": 2,
    "return-type": "json"
}
```

## 📂 Included Files
- `config/shairport-sync/`: Configuration for the AirPlay receiver.
- `config/waybar/`: The script and Waybar module example.
- `config/hypr/`: Hyprlock example showing media integration.

## 🤝 Contribution
Feel free to fork and improve!
