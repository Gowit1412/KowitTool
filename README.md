# KOWIT TOOL

A powerful command-line ADB package installer for Android devices.

![KOWIT TOOL](https://github.com/user-attachments/assets/76ada953-0a96-4b2b-aa50-242a8db86073)

## Overview

KOWIT TOOL is a lightweight yet powerful command-line utility for installing Android application packages through ADB.

It supports both standard APK files and split-package formats such as XAPK, APKS, APKM, and ZIP archives containing APK files.

The tool can automatically install required dependencies, download Android Platform Tools (ADB), detect connected devices, and manage package installation with minimal setup.

---

## Features

* Install standard APK files directly.
* Install split packages:

  * XAPK
  * APKS
  * APKM
  * ZIP archives containing APK files
* Install multiple packages in a queue.
* Automatic dependency installation.
* Automatic ADB detection.
* Automatic Android Platform Tools download and setup.
* Device connection status checking.
* ADB reconnect utility.
* File picker for multiple package installation.
* Temporary file cleanup after installation.
* Colored terminal interface.
* Progress bars for downloads and extraction.
* Windows, Linux, and macOS support.

---

## Supported Formats

| Format                   | Supported |
| ------------------------ | --------- |
| APK                      | ✅         |
| XAPK                     | ✅         |
| APKS                     | ✅         |
| APKM                     | ✅         |
| ZIP (contains APK files) | ✅         |

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
2. Go to **About Phone** or **About Tablet**.
3. Tap **Build Number** 7 times.
4. Open **Developer Options**.
5. Enable **USB Debugging**.
6. Connect the device to your computer.
7. Accept the USB debugging authorization prompt.

---

## Installation

### Clone Repository

```bash
git clone https://github.com/Gowit1412/KowitTool.git
cd KowitTool
```

### Install Dependencies

```bash
pip install colorama
```

### Run From Source

```bash
python kowit_tool.py
```

---

## First Launch

On the first launch, KOWIT TOOL may automatically:

1. Install required Python dependencies.
2. Download Android Platform Tools.
3. Configure ADB.
4. Start the ADB environment.

No manual ADB installation is required.

---

## Usage

### Install a Single Package

1. Connect your Android device via USB.
2. Verify that the device appears as connected.
3. Select:

```text
[1] Install Package (Drag & Drop)
```

4. Drag and drop the package file into the terminal or paste the full path.
5. Press Enter.
6. Wait for the installation process to finish.

Supported file types:

```text
.apk
.xapk
.apks
.apkm
.zip
```

---

### Install Multiple Packages

1. Select:

```text
[2] Install Multiple APK
```

2. A file selection window will open.
3. Select one or more package files.
4. Click Open.
5. The packages will be installed sequentially.

---

## Menu Options

```text
[1] Install Package (Drag & Drop)
[2] Install Multiple APK (Select Files)
[3] Reconnect Device
[4] Check Device Connection
[5] Exit
```

### Install Package

Install APK, XAPK, APKS, APKM, or ZIP packages.

### Install Multiple APK

Select and install multiple packages through a graphical file picker.

### Reconnect Device

Restart the ADB server and reconnect Android devices.

### Check Device Connection

Display the output of:

```bash
adb devices
```

### Exit

Close the application.

---

## Troubleshooting

### Device Not Detected

* Check the USB cable.
* Use a USB port that supports data transfer.
* Reconnect the device.
* Enable USB Debugging.
* Try the Reconnect Device option.

---

### Unauthorized Device

If the device shows:

```text
unauthorized
```

Disconnect and reconnect the device, then accept the USB debugging prompt on the Android device.

You may also try:

```bash
adb kill-server
adb start-server
```

---

### ADB Not Found

No action is required.

KOWIT TOOL will automatically download Android Platform Tools and configure ADB.

---

### Installation Failed

Possible causes:

* Corrupted APK package.
* Incompatible Android version.
* Insufficient device storage.
* Package signature mismatch.

Try uninstalling the existing application before reinstalling.

---

## Disclaimer

This software is intended for educational, development, testing, and device management purposes.

The developer is not responsible for any damage, data loss, device malfunction, account issues, or misuse resulting from the use of this software.

Use at your own risk.

---

## License

This project is provided as-is without warranty of any kind.
