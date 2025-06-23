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
  internet_speed_test_new: ^1.0.5
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
If you found any error than contact to khantharsh87@gmail.com



MIT License

Copyright (c) 2023 Harsh Khant

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

Licensed under the [MIT License](https://opensource.org/licenses/MIT) © 2023 Harsh Khant

