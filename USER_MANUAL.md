# DashCam App — User Manual

**Version:** 1.0.0 Beta
**Platform:** Android 8.0+ (API 26+)
**Last Updated:** October 2025

---

## Quick Start

1. **Install and Launch:** Grant camera, microphone, and location permissions when prompted.
2. **Mount Your Phone:** Securely mount on your windshield in landscape orientation, rear camera facing forward.
3. **Power It Up:** Connect to a power source that turns on with your car’s ignition (ACC). The app automatically starts recording when power is detected and stops when power is lost.
4. **Storage:** Videos are saved internally by default. You can change to SD card or external storage in settings.
5. **Uploads (Optional):** Configure uploads to your home computer, NAS, or cloud storage (Google Drive, OneDrive) via Wi-Fi.

---

## Introduction

DashCam transforms an old Android phone into a reliable, full-featured vehicle dash camera. Designed for **stability, automation, and simplicity**, it automatically records when your car starts and saves or uploads your footage when it stops.

### Main Features

* Automatic recording linked to ignition or impact
* Impact detection with circular video buffer
* GPS, speed, and motion sensor data logging
* Secure uploads to network shares (SMB/CIFS) or cloud (Google Drive, OneDrive)
* Multiple output formats: MP4, SRT, CSV, GPX
* Encrypted credential storage via Android Keystore
* Hostname resolution via NetBIOS for Windows networks
* Optimized for minimal user interaction — install once, drive daily

---

## Getting Started

### Permissions

Grant these permissions at first launch:

* **Camera** – Required for video recording.
* **Microphone** – For audio capture.
* **Location** – For GPS and speed logging.
* **Storage** – (Android 9 and below) For saving recordings.

### Mounting Your Phone

* Use a **windshield or dashboard mount** with a stable forward view.
* Keep cables neat and out of your line of sight.
* Connect power from a charger wired to ignition (ACC) for automatic operation.

### Power Behavior

* **Ignition On (Power Connected):** Recording starts automatically.
* **Ignition Off (Power Lost):** Recording stops safely and uploads begin (if configured).
  The phone remains awake to finish uploads, then sleeps to conserve power.

---

## Main Screen

* **Top-Left:** Date and time
* **Bottom-Left:** GPS coordinates and heading
* **Bottom-Right:** Speed (mph or km/h)
* **Center:** Camera preview and recording indicator
* **Floating Button:** Tap red to start, white to stop manual recording

⚠️ *If you see “EMULATOR – Video recording disabled,” you’re running in a virtual device. Use a real phone for recording.*

---

## Recording Modes

### 1. AUTO (Impact Detection)

Records continuously in short loops, saving only the last two minutes. When an impact (1.5G–3.0G) is detected, DashCam preserves:

* Two minutes before impact
* Ten seconds after
* All telemetry (GPS + sensor logs)

### 2. PER_TRIP

Starts when ignition turns on, stops when it turns off. Saves each trip as a single file with synchronized logs.

### 3. Timed Loop (5/10/30 minutes)

Splits recordings into smaller rotating files for easier upload and management.

### 4. Manual

Tap the red button to start or stop recording anytime.

---

## Settings Overview

### Display

* **Speed Units:** mph or km/h
* **Video Quality:** 720p, 1080p (default), 4K
* **Date/Time Format:** Regional customization
* **Keep Screen On:** Prevent timeout while recording

### Recording

* **Mode:** AUTO, PER_TRIP, 5/10/30 min
* **Impact Sensitivity:** Low (3.0G), Medium (2.0G default), High (1.5G)

---

## Storage Management

### Default Location

`/Android/data/com.dashcam.app/files/DashCam/`

### External or SD Card Storage

1. Go to **Settings → Storage Settings**.
2. Choose **EXTERNAL**.
3. Tap **Select Custom Folder** and pick your SD card or USB path.

### File Sizes (Approximate)

| Quality | MB/min | Recommended Use            |
| ------- | ------ | -------------------------- |
| 720p    | 50     | Long drives, low storage   |
| 1080p   | 80     | Balanced quality (default) |
| 4K      | 200    | High detail, large storage |

💡 *Telemetry logs (.srt, .csv, .gpx) remain under 0.2 MB/min combined.*

---

## Upload Configuration

DashCam supports automatic uploads over Wi-Fi to **SMB/CIFS shares**, **Google Drive**, or **OneDrive**.

### SMB Configuration

1. **Enable Uploads** in Settings.
2. **Set Upload Timing:** Manual, During Recording, or After Recording.
3. **Network Policy:** Wi-Fi only (default) or Allow Metered.
4. **Enter Server Details:**

   * **Host:** Windows hostname (NetBIOS) or IP address.
   * **Share:** Folder share name, e.g., `dashcam`.
   * **Username / Password:** Local Windows account credentials.

### Hostname Resolution (Windows Networks)

DashCam supports **NetBIOS name resolution**, allowing you to use Windows hostnames instead of IP addresses (e.g., `MYPC`).
Ensure both devices are on the same Wi-Fi network and that **Network Discovery** is enabled in Windows.

> macOS or Linux users may still need to connect using the IP address.

### Why You Need a Local Windows Account

Windows 10+ no longer supports guest shares. Create a dedicated **local user** with password access:

1. **Win + I → Accounts → Family & other users**.
2. Select **Add account → Add a user without a Microsoft account**.
3. Create username (e.g., `dashcam_user`) and password.
4. Grant folder **Read/Write** permissions under both **Sharing** and **Security** tabs.

💡 *Find your PC’s IP via Command Prompt → `ipconfig` → IPv4 Address.*

### Cloud Uploads

DashCam can also upload directly to cloud storage.

* **Google Drive:** Fully supported. Authorize your Google account once in settings.
* **OneDrive:** Fully supported. Sign in to your Microsoft account and select target folder.
* **Dropbox:** Planned for future versions if requested by users.

Uploads retry automatically if interrupted, and you may choose to delete local files after successful transfer.

---

## Troubleshooting

| Issue               | Possible Fix                                                 |
| ------------------- | ------------------------------------------------------------ |
| No video            | Grant camera permission; restart app.                        |
| GPS stuck           | Move outdoors for signal; ensure GPS is on.                  |
| Impact not detected | Adjust sensitivity; secure mount.                            |
| Upload fails        | Confirm credentials; ensure same Wi-Fi; enable SMB port 445. |
| Hostname not found  | Verify NetBIOS discovery; fallback to IP.                    |
| Storage full        | Lower video quality or enable auto-delete after upload.      |

### Performance Tips

* Disable Android battery optimization for DashCam.
* Use a quality charger (2A+).
* Avoid overheating — direct sunlight may trigger shutdown.

---

## Technical Notes

* **Video:** H.264/AVC MP4 @ 30 fps
* **Telemetry:** SRT (GPS/speed), CSV (10 Hz sensor data), GPX (map track)
* **Impact Buffer:** Two-minute rolling loop, saves +10s post-impact
* **Permissions:** CAMERA, RECORD_AUDIO, ACCESS_FINE_LOCATION, INTERNET, WAKE_LOCK, FOREGROUND_SERVICE
* **Credential Storage:** Encrypted via Android Keystore

---

## Known Limitations (Beta)

* Dropbox integration pending user demand.
* Extremely long continuous trips may require large storage capacity.

---

## Safety & Responsibility

DashCam assists drivers — it is **not** a substitute for safe driving. Always follow local laws regarding in-car recording.

---

## Support & Feedback

This is a **beta release** — stable for daily use, with active development continuing.

* Report issues or suggestions via the project’s GitHub page.
* Include your phone model, Android version, and a short problem description.

**Thank you for using DashCam. Drive safe — and record responsibly.**
