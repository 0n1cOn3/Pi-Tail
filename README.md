# 📌 Pi-Tail Komplett (Deutsch)

> **🔗 Original-Anleitung auf Englisch:** [Pi-Tail Guide](https://whitedome.com.au/re4son/pi-tail/)

## 🛠 Installation und Einrichtung

### 📥 Image-Download

**Image:** `Pi-Tail.img` von *re4son* (letztes Update 2018)
- 📁 Datei: `Pi-Tail-180925.img.xz` (2,2 GB)
- ⚠ **Wichtig:** *Kein* `apt-get update/upgrade` durchführen, da sonst die Funktionalität beeinträchtigt wird.

### 🔧 Kernel und Setup

Der *re4son*-Kernel ermöglicht den Monitor-Mode auf dem Raspberry Pi **ohne** zusätzliche WLAN-Karte.

**🔗 Benötigte Downloads:**
- [📥 Pi-Tail Image](https://whitedome.com.au/re4son/download/pi-tail/)
- [📥 Raspberry Pi Imager](https://downloads.raspberrypi.org/imager/imager_latest.exe)

**🚀 Setup:**
1. Lade das Image herunter und kopiere es mit dem Raspberry Pi Imager auf eine SD-Karte.
2. Setze die SD-Karte in den Raspberry Pi Zero ein.
3. Starte den Pi durch Anschluss an eine Stromquelle.

---

## 📡 Verbindung mit Android

1. **📶 WiFi-Hotspot einrichten**
   - **SSID:** `sepultura`
   - **Passwort:** `R4t4m4h4tt4`
2. **🔐 ConnectBot Konfiguration**
   - SSH-Host: `root@192.168.43.254`
   - Passwort: `toor`
3. **📜 Wichtige Befehle**
   - `mon0up` (Monitor-Mode aktivieren)
   - `wifite` (WLAN-Analyse starten)
   - *(Beenden mit `CTRL+C`, Monitor-Mode deaktivieren mit `mon0down`)*

---

## 🖥 VNC-Steuerung (Optional)

1. **🎛 Starten des VNC-Servers**
   ```sh
   vncserver
   ```
2. **⚙️ Port-Weiterleitung in ConnectBot**
   - **Nickname:** `localhost`
   - **Typ:** `local`
   - **Quellport:** `5901`
   - **Ziel:** `127.0.0.1:5901`
3. **🔗 VNC-Verbindung konfigurieren**
   - **Name:** `PiTail0`
   - **Adresse:** `127.0.0.1:5901`
   - **Benutzer:** `root`
   - **Passwort:** `toortoor`

---

## 🔄 Alternative: Pi-Tail von Kali.org

> **📥 Aktuelle Version:** `kali-linux-2021.3-rpi0w-pitail-armel.img.xz`

Die *kali.org*-Version erfordert zusätzliche Konfigurationen, da sie standardmäßig ohne Root-Zugriff läuft.

### 🔑 Trick 1: Root-Zugriff mit `sudo`

1. Verbindung mit:
   ```sh
   kali@192.168.43.254
   ```
   **Passwort:** `kali`
2. **🔏 Root-Passwort setzen:**
   ```sh
   sudo passwd root
   ```
   - Neues Passwort: `toor`
   - Bestätigen: `toor`
3. **🛠 Root-Zugriff aktivieren:**
   ```sh
   su
   ```
   - Passwort: `toor`

---

### 🔓 Trick 2: Root-Login per SSH

1. Verbindung mit:
   ```sh
   kali@192.168.43.254
   ```
   **Passwort:** `kali`
2. **🔄 Passwort ändern:**
   ```sh
   passwd
   ```
   - Altes Passwort: `kali`
   - Neues Passwort: `toortoor`
   - Bestätigen: `toortoor`
3. **🔗 Verbindung trennen und neuen SSH-Host erstellen:**
   ```sh
   root@192.168.43.254
   ```
   - **Passwort:** `toortoor`

---

## 📚 Weitere Informationen

- 🔗 [Re4son auf GitHub](https://github.com/Re4son/)

