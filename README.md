---

# internet\_speed\_test\_new

[![pub package](https://img.shields.io/pub/v/internet_speed_test_new.svg)](https://pub.dev/packages/internet_speed_test_new)

A Flutter plugin to measure **download** and **upload** internet speed on **Android** and **iOS**.
Supports both **Wi-Fi** and **mobile data (cellular)** networks.

---

## 🚀 Features

* Measure **Download Speed**
* Measure **Upload Speed**
* Works on **Wi-Fi** and **Mobile Data**
* Supports **Android** and **iOS**

---

## 🛠 Getting Started

### 1. Add Dependency

In your `pubspec.yaml`:

```yaml
dependencies:
  internet_speed_test_new: ^1.0.5
```

Then run:

```bash
flutter pub get
```

---

### 2. Import the Package

```dart
import 'package:internet_speed_test_new/internet_speed_test_new.dart';
```

---

### 3. Create an Instance

```dart
final networkSpeed = NetworkSpeedPlus();
```

---

### 4. Measure Internet Speed

#### 📥 Download Speed

```dart
final downloadSpeed = await networkSpeed.getDownloadSpeed(
  testUrl: 'https://speed.hetzner.de/10MB.bin', // Replace with a valid URL
  fileSize: 10 * 1024 * 1024, // File size in bytes
);
print('Download speed: $downloadSpeed Mbps');
```

#### 📤 Upload Speed

```dart
final uploadSpeed = await networkSpeed.getUploadSpeed(
  testUrl: 'https://your-upload-endpoint.com', // Replace with a valid endpoint
  fileSize: 5 * 1024 * 1024, // File size in bytes
);
print('Upload speed: $uploadSpeed Mbps');
```

---

## ⚙️ Permissions

### Android (`AndroidManifest.xml`)

```xml
<uses-permission android:name="android.permission.INTERNET" />
```

### iOS

No additional permissions required, but ensure the app has internet access.

---

## 💡 Example

Check out the complete example:

```bash
cd example
flutter run
```

---

## 🖥 Platform Support

| Platform | Supported |
| -------- | --------- |
| Android  | ✅         |
| iOS      | ✅         |
| Web      | ❌         |
| macOS    | ❌         |
| Windows  | ❌         |
| Linux    | ❌         |

---

## 🤝 Contributions

Contributions are welcome!
Feel free to open [issues](https://github.com/your-repo/issues) or submit pull requests.

**Found an issue?** Contact me: [khantharsh87@gmail.com](mailto:khantharsh87@gmail.com)

---

## 📄 License

This project is licensed under the MIT License.

```
MIT License

Copyright (c) 2023 Harsh Khant

Permission is hereby granted, free of charge, to any person obtaining a copy...
```

[Read the full license](https://opensource.org/licenses/MIT)

---
