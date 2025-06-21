# internet_speed_test_new

[![pub package](https://img.shields.io/pub/v/internet_speed_test_new.svg)](https://pub.dev/packages/internet_speed_test_new)

A Flutter plugin for measuring the **download** and **upload speed** of the current internet connection on **Android** and **iOS**.  
Supports both **WiFi** and **mobile (cellular)** networks.

---

## Features

- 🚀 Measure **download speed**
- 📤 Measure **upload speed**
- 📡 Works with WiFi and Mobile Data
- 📱 Supports Android and iOS

---

## Getting Started

Add the dependency in your `pubspec.yaml`:

```yaml
dependencies:
  internet_speed_test_new: ^1.0.0
```
Then run:
```termianl
flutter pub get
```


Import the package:

```import
import 'package:internet_speed_test_new/internet_speed_test_new.dart';
```
Create an instance:
```object
final networkSpeed = NetworkSpeedPlus();
```
📥 Measure Download Speed
```
final downloadSpeed = await networkSpeed.getDownloadSpeed(
  testUrl: 'https://speed.hetzner.de/10MB.bin', // Replace with a valid file
  fileSize: 10 * 1024 * 1024, // in bytes
);
print('Download speed: $downloadSpeed Mbps');
```

📤 Measure Upload Speed
```
final uploadSpeed = await networkSpeed.getUploadSpeed(
  testUrl: 'https://your-upload-endpoint.com', // Replace with valid upload URL
  fileSize: 5 * 1024 * 1024, // in bytes
);
print('Upload speed: $uploadSpeed Mbps');
```

Permissions:

AndroidManifest.xml
```
<uses-permission android:name="android.permission.INTERNET" />
```

iOS:

No special permission is required, but ensure your app has internet access.


Example:

Check out the full example in the example/ directory:
```
cd example
flutter run
```

Platform Support


| Platform | Supported |
| -------- | --------- |
| Android  | ✅         |
| iOS      | ✅         |
| Web      | ❌         |
| macOS    | ❌         |
| Windows  | ❌         |
| Linux    | ❌         |




🙂Contributions are welcome! Feel free to open issues or submit pull requests.




Licensed under the [MIT License](https://opensource.org/licenses/MIT) © 2023 Harsh Khant

