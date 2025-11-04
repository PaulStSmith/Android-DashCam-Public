# DashCam v1.0.0 Release Notes

## Overview

DashCam v1.0.0 is the initial release of an advanced dashcam application that repurposes old Android phones as professional-grade vehicle cameras. This release introduces comprehensive video recording capabilities, impact detection, GPS telemetry, and cloud upload features using modern Android technologies.

## Key Features

### 🎥 Core Recording Features
- **CameraX Integration**: High-quality video recording with hardware-accelerated encoding
- **Real-time Telemetry**: GPS location, speed, and direction data embedded as SRT subtitles
- **Multiple Recording Modes**:
  - **AUTO Mode**: Circular buffer recording with intelligent impact detection that automatically saves critical footage during collisions
  - **Per Trip Mode**: Automatic start/stop recording based on vehicle power connection
  - **Timed Loop Mode**: Configurable 5/10/30 minute segments with seamless file management

### 🚗 Impact Detection & Safety
- **Accelerometer-based Detection**: Advanced algorithms detect sudden impacts and protect important footage
- **Circular Buffer**: Continuous recording with automatic cleanup while preserving critical moments
- **File Protection**: Important recordings are automatically marked and protected from deletion

### ☁️ Cloud Upload System
- **Multi-Platform Support**: Upload to Google Drive, OneDrive, and SMB/CIFS network shares
- **Background Processing**: Reliable upload worker that continues even when app is closed
- **Network Management**: Configurable WiFi-only or metered network upload policies
- **Queue Management**: Visual upload queue viewer with retry functionality and progress tracking
- **OAuth Integration**: Secure authentication for cloud services

### ⚙️ Advanced Settings
- **Comprehensive Configuration**: Speed units (mph/km/h), date/time formats, video quality settings
- **Storage Management**: Custom storage paths, automatic cleanup, and file organization
- **Power Management**: Battery optimization handling and screen timeout controls
- **Crash Reporting**: Optional Firebase Crashlytics integration for diagnostics

### 🎨 Modern User Interface
- **Jetpack Compose**: Modern, declarative UI with smooth animations
- **Material Design 3**: Consistent design language with dark/light theme support
- **Immersive Experience**: Full-screen camera view with hidden system bars
- **Multi-language Support**: Localized interface in multiple languages

### 🔧 Technical Features
- **Foreground Service**: Reliable background operation for continuous recording
- **WorkManager Integration**: Scheduled background uploads and maintenance tasks
- **DataStore Preferences**: Secure, efficient settings storage
- **Permissions Handling**: Comprehensive permission management for camera, location, and storage
- **Battery Optimization**: Smart handling of Android battery restrictions

## System Requirements
- **Android Version**: 8.0 (API 26) or higher
- **Hardware**: Camera, GPS, accelerometer sensors
- **Storage**: Sufficient space for video recordings and circular buffer

## Known Limitations
- Requires Android device with adequate camera and sensor capabilities
- Cloud upload requires stable internet connection
- Some features may have limited functionality on older Android versions

## Installation
Install the APK file on a compatible Android device. Grant all requested permissions for full functionality.

## Support
For issues, feature requests, or questions, please refer to the project documentation or contact the development team.

## Future Plans
- Temperature monitoring integration
- Enhanced cloud backup functionality
- Additional UI themes and customization options
- Expanded platform support

---

*Released: November 3, 2025*  
*Version: 1.0.0 (Build 1)*</content>
<parameter name="filePath">c:\Users\pauls\source\repos\DashCam\public\lang\en\release-notes-v1.md