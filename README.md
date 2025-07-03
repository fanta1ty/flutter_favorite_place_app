# Flutter Favorite Places App

A beautiful Flutter application that allows users to save and manage their favorite places with photos, locations, and
memories. Built with native device features integration including camera access, GPS location, and map display.

## 🌟 Features

- **Add Favorite Places**: Save your favorite locations with custom titles and descriptions
- **Camera Integration**: Take photos directly from the app using device camera
- **Location Services**: Automatically capture current location or manually select from map
- **Interactive Maps**: View and select locations using Google Maps integration
- **Local Storage**: Store all your favorite places locally on the device
- **Place Details**: View detailed information about each saved place
- **Edit & Delete**: Modify or remove saved places
- **Responsive Design**: Works seamlessly on both Android and iOS devices

## 📱 Screenshots

<!-- Add your app screenshots here -->
*Screenshots coming soon...*

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (3.0.0 or higher)
- Dart SDK (2.17.0 or higher)
- Android Studio / VS Code with Flutter plugins
- Android device/emulator or iOS device/simulator

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/fanta1ty/flutter_favorite_place_app.git
   cd flutter_favorite_place_app
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Configure Google Maps API (if using Google Maps)**
    - Get your API key from [Google Cloud Console](https://console.cloud.google.com/)
    - Add the API key to your platform-specific configuration:

   **Android**: Add to `android/app/src/main/AndroidManifest.xml`
   ```xml
   <meta-data android:name="com.google.android.geo.API_KEY"
              android:value="YOUR_API_KEY_HERE"/>
   ```

   **iOS**: Add to `ios/Runner/AppDelegate.swift`
   ```swift
   GMSServices.provideAPIKey("YOUR_API_KEY_HERE")
   ```

4. **Run the app**
   ```bash
   flutter run
   ```

## 🏗️ Project Structure

```
lib/
├── main.dart                 # App entry point
├── models/                   # Data models
│   └── place.dart           # Place model
├── screens/                  # UI screens
│   ├── places_list_screen.dart
│   ├── add_place_screen.dart
│   ├── place_detail_screen.dart
│   └── map_screen.dart
├── widgets/                  # Custom widgets
│   ├── image_input.dart
│   ├── location_input.dart
│   └── place_item.dart
├── helpers/                  # Helper classes
│   ├── db_helper.dart       # Database operations
│   └── location_helper.dart # Location utilities
└── providers/               # State management
    └── places_provider.dart
```

## 🛠️ Built With

- **Flutter** - UI framework
- **Dart** - Programming language
- **Provider** - State management
- **SQLite** - Local database storage
- **Google Maps** - Map integration
- **Image Picker** - Camera/gallery access
- **Location** - GPS services
- **Path Provider** - File system access

## 📦 Dependencies

```yaml
dependencies:
  flutter:
    sdk: flutter
  provider: ^6.0.5
  image_picker: ^0.8.7+4
  location: ^4.4.0
  google_maps_flutter: ^2.2.5
  sqflite: ^2.2.8
  path_provider: ^2.0.14
  path: ^1.8.3
  http: ^0.13.5

dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^2.0.1
```

## 🎯 How to Use

1. **Launch the app** - You'll see your list of favorite places (empty initially)
2. **Add a new place** - Tap the '+' button to add a new favorite place
3. **Take a photo** - Use the camera to capture a photo of the place
4. **Add location** - Either use your current location or select from the map
5. **Save the place** - Add a title and save your favorite place
6. **View details** - Tap on any place to see its details and location on the map
7. **Edit or delete** - Long press on a place to edit or delete it

## 🔧 Configuration

### Permissions

The app requires the following permissions:

**Android** (`android/app/src/main/AndroidManifest.xml`):

```xml

<uses-permission android:name="android.permission.CAMERA" /><uses-permission
android:name="android.permission.ACCESS_FINE_LOCATION" /><uses-permission
android:name="android.permission.ACCESS_COARSE_LOCATION" /><uses-permission
android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
```

**iOS** (`ios/Runner/Info.plist`):

```xml

<key>NSCameraUsageDescription</key><string>This app needs access to camera to take pictures of places</string><key>
NSLocationWhenInUseUsageDescription
</key><string>This app needs access to location to save place locations</string>
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📋 Roadmap

- [ ] Add search functionality for places
- [ ] Implement place categories/tags
- [ ] Add sharing functionality
- [ ] Implement cloud backup
- [ ] Add offline map support
- [ ] Implement place rating system
- [ ] Add export/import functionality

## 🐛 Known Issues

- Camera permission needs to be granted manually on first launch
- Location services must be enabled for accurate positioning
- Google Maps API key is required for map functionality

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**fanta1ty**

- GitHub: [@fanta1ty](https://github.com/fanta1ty)

## 🙏 Acknowledgments

- Flutter team for the amazing framework
- Google Maps API for location services
- The Flutter community for inspiration and support

## 📞 Support

If you have any questions or need help with the app, please open an issue on GitHub or contact the author.

---

**Happy coding! 🚀**
