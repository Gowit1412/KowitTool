# KOWIT TOOL

A simple command-line ADB package installer for Android devices.

![KOWIT TOOL](https://github.com/user-attachments/assets/76ada953-0a96-4b2b-aa50-242a8db86073)

## Overview

KOWIT TOOL is a lightweight command-line utility that helps install Android application packages through ADB. It supports both single APK files and split-package formats such as XAPK, APKS, APKM, and ZIP archives containing APK files.

The tool can automatically download and configure Android Platform Tools (ADB) if they are not already installed on your system.

---

## Features

* Install standard APK files directly.
* Install split packages:

  * XAPK
  * APKS
  * APKM
  * ZIP archives containing APK files
* Automatic ADB detection.
* Automatic Android Platform Tools download and setup.
* Device connection checking.
* ADB reconnect utility.
* Colored terminal output.
* Windows, Linux, and macOS support.

---

## Requirements

Before using this tool, ensure you have:

* A USB cable that supports data transfer.
* An Android phone or tablet.
* USB Debugging enabled on the device.
* Python 3.8+ (when running from source).

---

## Enable USB Debugging

1. Open **Settings**.
2. Go to **About Phone** (or About Tablet).
3. Tap **Build Number** 7 times.
4. Open **Developer Options**.
5. Enable **USB Debugging**.
6. Connect the device to your computer and allow the debugging authorization prompt.

---

## Installation

### Clone Repository

```bash
git clone https://github.com/Gowit1412/KowitTool.git
cd kowittool
```

### Install Dependencies

```bash
pip install colorama
```

### Run

```bash
python kowit_tool.py
```

---

## Usage

After launching the program:

1. Connect your Android device via USB.
2. Verify that the device appears in the connected device list.
3. Select:

```text
[1] Install Package
```

4. Drag and drop your file into the terminal or paste the full path.

Supported formats:

```text
.apk
.xapk
.apks
.apkm
.zip
```

5. Wait for the installation process to complete.

---

## Menu Options

```text
[1] Install Package
[2] Reconnect Device
[3] Check Device
[4] Exit
```

### Install Package

Install APK, XAPK, APKS, APKM, or ZIP packages.

### Reconnect Device

Restart the ADB server and reconnect devices.

### Check Device

Display the output of:

```bash
adb devices
```

---

## Troubleshooting

### Device Not Detected

* Check the USB cable.
* Use a USB port that supports data transfer.
* Reconnect the device.
* Enable USB Debugging.

### Unauthorized Device

If the device shows:

```text
unauthorized
```

Disconnect and reconnect the device, then accept the USB debugging prompt on the Android device.

### ADB Not Found

No action is required.

KOWIT TOOL will automatically download Android Platform Tools and configure ADB for you.

---

## Build Executable

Create a standalone executable using PyInstaller:

```bash
pyinstaller --onefile --name "KOWIT_TOOL" kowit_tool.py
```

---

## Disclaimer

This software is intended for educational, development, testing, and device management purposes.

The developer is not responsible for any damage, data loss, device malfunction, or misuse resulting from the use of this software. Use at your own risk.
