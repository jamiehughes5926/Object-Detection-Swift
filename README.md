# Object-Detection-Swift: Text Detection with VisionKit

## Overview
This Swift app leverages Apple's VisionKit framework to perform real-time text detection using the device's camera. The app is designed to identify text in both English and Japanese, and it highlights detected Japanese text with a visually distinct overlay.

## Features
- **Real-Time Text Detection:** Use the device's camera to detect and display text in real-time.
- **Language Support:** Detects text in both English (`en-US`) and Japanese (`ja-JP`).
- **Japanese Text Highlighting:** Automatically highlights detected Japanese text with a magenta rounded rectangle overlay.
- **Customizable UI:** Flexible UI elements for text display and highlighting, ensuring clarity and ease of use.

## Requirements
- iOS 16.0+
- Xcode 14.0+
- Swift 5.0+
- VisionKit framework

## Installation

### Clone the Repository
```bash
git clone https://github.com/jamiehughes5926/Object-Detection-Swift.git
cd Object-Detection-Swift
```

### Open in Xcode
1. Open `Object-Detection-Swift.xcodeproj` in Xcode.
2. Ensure that your development team is set under **Signing & Capabilities**.
3. Select your target device or simulator.

## Usage
1. **Build and Run the App:** 
   - Select your target device in Xcode.
   - Press the `Run` button to build and deploy the app.

2. **Real-Time Scanning:**
   - The app automatically starts detecting text when the camera is active.
   - Detected Japanese text is highlighted with a magenta rounded rectangle.

3. **Interaction with Detected Items:**
   - The app dynamically updates the highlighted areas as text is detected, added, removed, or updated.

## Code Structure

- **`DataScannerView` Struct:** Encapsulates the VisionKit's `DataScannerViewController` within a SwiftUI view.
  - Initializes with support for detecting both text and barcodes.
  - Automatically starts scanning when the view appears.

- **Coordinator:** 
  - Acts as a delegate for the `DataScannerViewController`.
  - Handles the detection, addition, removal, and updating of recognized items.
  - Specifically looks for Japanese text and applies a magenta overlay with rounded corners to it.

- **RoundedRectLabel Class:** 
  - Custom UIView subclass used to display detected Japanese text within a rounded rectangle.
  - Configured with adjustable padding and opacity for clear and distinct text overlays.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request with any improvements, bug fixes, or new features.

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.

## Acknowledgments
- [Apple's VisionKit framework](https://developer.apple.com/documentation/visionkit) for enabling advanced text recognition on iOS devices.
