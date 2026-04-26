<p align="left">
  <img src="https://github.com/user-attachments/assets/1da1f46e-8617-4f03-911d-c0c71baf2229" width="90" height="90" />
</p>

# BloomClassifier

<p align="center">
  <img src="https://img.shields.io/badge/Swift-FA7343?style=for-the-badge&logo=swift&logoColor=white" />
  <img src="https://img.shields.io/badge/UIKit-2396F3?style=for-the-badge&logo=apple&logoColor=white" />
  <img src="https://img.shields.io/badge/Core%20ML-000000?style=for-the-badge&logo=apple&logoColor=white" />
  <img src="https://img.shields.io/badge/Vision-555555?style=for-the-badge&logo=apple&logoColor=white" />
</p>

BloomClassifier is an iOS app that identifies flowers from camera images using Core ML and Vision.

After classification, the app sends the detected flower name to Wikipedia API and displays a short description on the screen.

## Screenshots

<p align="center">
  <img src="YOUR_SCREENSHOT_1_URL" width="250" />
  <img src="YOUR_SCREENSHOT_2_URL" width="250" />
  <img src="YOUR_SCREENSHOT_3_URL" width="250" />
</p>

## Features

- Take a flower photo using the camera
- Classify the image with a Core ML model
- Show the predicted flower name in the navigation bar
- Fetch a short flower description from Wikipedia API
- Display flower information inside the app

## Technologies

- Swift
- UIKit
- Core ML
- Vision
- Alamofire
- SwiftyJSON
- CocoaPods
- Wikipedia API

## How It Works

1. The user takes or edits a flower photo.
2. The app displays the selected image.
3. The image is converted from `UIImage` to `CIImage`.
4. Vision sends the image to the Core ML model.
5. The model returns the most likely flower class.
6. The app requests a short description from Wikipedia API.
7. The flower name and description are shown to the user.

## Model

The app uses `FlowerClassifier.mlmodel` for flower image classification.

The model is integrated with Apple Vision framework, which prepares the selected image and returns the most likely flower class. The result may depend on image quality, lighting, background, and camera angle.

The model can also be replaced with another Core ML image classifier trained with Create ML.

## Installation

1. Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/BloomClassifier.git
```

2.	Open the project folder:

```bash
cd BloomClassifier
```

3.	Install dependencies:

```bash
pod install
```

4.	Open the workspace file:

```bash
open BloomClassifier.xcworkspace
```

5. Run the app on a real iOS device.

> The camera does not work in the iOS Simulator, so the app should be tested on a physical device.

## Permissions

The app requires camera access to take flower photos for classification.

Example `Privacy - Camera Usage Description`:

```text
This app needs camera access to take photos of flowers and identify their species.
```

## Project Structure

```text
BloomClassifier
├── ViewController.swift
├── FlowerClassifier.mlmodel
├── Main.storyboard
├── Assets.xcassets
├── Info.plist
├── Podfile
└── README.md
```

## Learning Purpose

This project was created as part of my iOS development learning journey.

It helped me practice working with Core ML, Vision, camera input, CocoaPods, third-party libraries, and API requests in Swift.

## Author

Created by Arina Agafonova.
