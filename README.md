# Android BLE Peripheral + Central Sample

A sample Android app demonstrating **Bluetooth Low Energy (BLE)** communication in both
**central** and **peripheral** roles. The app can advertise as a peripheral, scan/connect
as a central, and read/notify a sample characteristic. This is a practical template for
**connect / send / receive / disconnect** flows using the standard Android BLE APIs.

## Features

- **Peripheral mode** (BLE advertising)
- **Central mode** (scan, connect, discover services)
- **Read characteristic** and receive **notifications**
- Basic UI for device discovery and connection state
- Example service/characteristic using Heart Rate profile UUIDs

## Screenshots

<img src="screenshots/1.png" height="500" alt="Screenshot"/> <img src="screenshots/2.png" height="500" alt="Screenshot"/>
<img src="screenshots/3.png" height="500" alt="Screenshot"/> <img src="screenshots/4.png" height="500" alt="Screenshot"/>

## Project Structure (key files)

- `MainActivity` – entry point + role selection
- `CentralRoleActivity` – scanning / connection UI
- `PeripheralRoleActivity` – advertising UI
- `CentralService` – GATT client (connect/read/notify)
- `PeripheralAdvertiseService` – BLE advertising as peripheral
- `DeviceConnectActivity` – device connection + characteristic read
- `Constants` – UUIDs and shared constants

## Setup

**Requirements**
- Android Studio
- Android SDK 26 (compile/target)
- **minSdkVersion 21** (BLE peripheral role requires Android 5.0+)
- A BLE‑capable Android device

**Build & Run**
1. Clone this repository
2. Open in Android Studio
3. Build and run on a real device (BLE features may not work on emulators)

## Usage

1. Launch the app
2. Choose **Central** or **Peripheral** role
3. Peripheral: start advertising
4. Central: scan, select device, connect
5. Read/notify the sample characteristic

> The sample uses Heart Rate profile UUIDs (see `Constants.java`).

## Permissions

Declared in `AndroidManifest.xml`:
- `BLUETOOTH`
- `BLUETOOTH_ADMIN`
- `ACCESS_COARSE_LOCATION` (required for BLE scanning on older Android)

## License

This repository is a copy of the upstream sample. Check the original repository for
license details and attribution.

## Acknowledgements

- https://github.com/googlesamples/android-BluetoothLeGatt
- https://github.com/googlesamples/android-BluetoothAdvertisements
- https://github.com/WebBluetoothCG/ble-test-peripheral-android

## Program Summary

- Android sample app that demonstrates BLE in both **peripheral** (advertising) and **central** (scan/connect) roles.
- Lets a central read/receive notifications from a sample characteristic (Heart Rate UUIDs).

## How to Use

- Open the project in Android Studio and run on a real BLE‑capable device.
- Optional CLI build: `./gradlew assembleDebug` (Not verified).
- In-app: choose **Central** or **Peripheral**, then advertise or scan/connect and read/notify.
- Not verified: build/run steps were not executed in this environment.

## Completion Status

- **Usable (sample/template)**: core BLE flows are implemented with a basic UI and Heart Rate sample UUIDs; this targets SDK 26 and uses Android support libraries (not AndroidX), indicating a demonstration sample rather than a production app.

## Program Summary

- Android BLE sample app implementing both **peripheral** (advertising) and **central** (scan/connect/GATT) roles.
- Uses Heart Rate service/characteristic UUIDs for the example read/notify flow (see `Constants.java`).

## How to Use

- Open the project in Android Studio and run on a real BLE-capable Android device.
- Optional CLI build: `./gradlew assembleDebug` (Not verified).
- In-app: pick **Central** or **Peripheral**, then advertise or scan/connect and read/notify.
- Not verified: these steps were not executed in this environment.

## Completion Status

- **Usable (sample/template)**: core BLE flows and UI are present, but it targets SDK 26 with legacy support libraries and does not present production hardening (e.g., modern permissions, AndroidX migration).

## Program Summary

- Android sample app showing BLE **peripheral** (advertise) and **central** (scan/connect/GATT) roles in one project.
- Demonstrates read/notify of a sample characteristic using Heart Rate UUIDs.

## How to Use

- Open in Android Studio and run on a real BLE-capable Android device.
- Optional CLI build: `./gradlew assembleDebug` (Not verified).
- In-app: choose **Central** or **Peripheral**, then advertise or scan/connect and read/notify (Not verified).

## Completion Status

- **Usable (sample/template)**: core BLE flows and basic UI are implemented; appears intended for learning/demo rather than production hardening.
