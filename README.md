# Monitor App

A monitoring application designed for the OnePlus Ace 5 phone that displays a precise clock showing hours, minutes, seconds, and microseconds.

## Repository

This project is hosted on GitHub: [https://github.com/cnetboy/Monitor_App](https://github.com/cnetboy/Monitor_App)

## Description

This app provides real-time monitoring capabilities with an accurate time display. It is specifically optimized for the OnePlus Ace 5 device.

## Features

- Real-time clock display with microsecond precision
- Optimized performance on OnePlus Ace 5
- System monitoring integration

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/cnetboy/Monitor_App.git
   ```

2. Ensure you have Android SDK and Gradle installed.

3. Build the APK:
   ```
   cd Monitor_App
   gradle assembleDebug
   ```

4. The APK will be located at `app/build/outputs/apk/debug/app-debug.apk`.

### Installing via ADB (Recommended)

1. Install ADB on your system:
   - Ubuntu/Debian: `sudo apt install android-tools-adb`
   - Other systems: Download from Android SDK Platform Tools

2. Enable USB Debugging on your OnePlus Ace 5:
   - Go to Settings > About Phone > Tap "Build number" 7 times to enable Developer Options
   - Go to Settings > Developer Options > Enable "USB Debugging"

3. Connect your phone via USB and run:
   ```
   adb devices
   ```
   Your device should appear in the list.

4. Install the APK:
   ```
   adb install app/build/outputs/apk/debug/app-debug.apk
   ```

5. Launch the app on your device.

### Manual Installation

5. Transfer the APK to your OnePlus Ace 5 phone.

6. On your phone, enable "Install unknown apps" in Settings > Security.

7. Use a file manager to locate and install the APK.

8. Launch the app to view the real-time clock.

## Usage

Launch the app on your OnePlus Ace 5 phone to start monitoring and view the precise clock display.

## Troubleshooting

### Device Not Detected by ADB

If `adb devices` shows no devices attached:

- **Virtual Machine Users**: Ensure USB passthrough is configured in your VM settings (VirtualBox/VMware) to allow access to the physical USB device.
- **USB Connection Issues**: Try a different USB cable, port, or enable "File Transfer" mode on your phone.
- **Driver Issues**: On Windows, install OEM USB drivers for OnePlus devices.
- **Permission Issues**: On Linux, you may need to add your user to the `plugdev` group or run ADB as root.

### Build Issues

If the build fails:
- Ensure Java JDK 11+ is installed
- Update Gradle wrapper if needed: `./gradlew wrapper --gradle-version 8.14.3`
- Clean build: `gradle clean build`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.
