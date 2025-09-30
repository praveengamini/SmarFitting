# Body Metrics Application 📏

A web-based application that provides accurate body measurements including shoulder width, waist length, and hip length using computer vision and pose detection technology.

## Overview

This application uses your device's camera to capture your body pose and calculate key measurements. By using the average distance between eyes (6.5 cm) as a reference point, the app provides real-time body measurements that can be useful for clothing purchases, fitness tracking, or tailoring needs.

## Features

- **Real-time Body Detection**: Uses advanced pose detection models to identify body landmarks
- **Accurate Measurements**: Calculates shoulder width, waist length, and hip length
- **Reference-based Scaling**: Uses inter-eye distance (6.5 cm average) for accurate real-world measurements
- **Privacy-First**: All processing happens locally in your browser - no data is sent to servers
- **User-Friendly Interface**: Clean, intuitive interface for easy measurements

## Technologies Used

- **React 18** - Modern UI framework
- **TensorFlow.js** - Machine learning in the browser
- **MediaPipe** - Google's pose and hand tracking solutions
- **Vite** - Fast build tool and development server
- **Tailwind CSS** - Utility-first styling
- **Lucide React** - Beautiful icon set

### AI/ML Models

- `@tensorflow-models/pose-detection` - Body pose estimation
- `@tensorflow-models/hand-pose-detection` - Hand landmark detection
- `@tensorflow-models/blazeface` - Face detection
- `@mediapipe/hands` & `@mediapipe/pose` - MediaPipe solutions

## Installation

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn package manager

### Setup

1. Clone the repository:
```bash
git clone https://github.com/yourusername/body-metrics-app.git
cd body-metrics-app
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open your browser and navigate to `http://localhost:5173`

## Usage

1. **Allow Camera Access**: Grant permission for the app to access your camera
2. **Position Yourself**: Stand 6-8 feet away from the camera in good lighting
3. **Face the Camera**: Ensure your full body is visible in the frame
4. **Get Measurements**: The app will automatically detect your pose and display measurements

### Tips for Accurate Measurements

- Ensure good, even lighting
- Wear fitted clothing for better landmark detection
- Stand straight with arms slightly away from your body
- Keep a consistent distance from the camera
- Avoid cluttered backgrounds

## Measurements Provided

- **Shoulder Width**: Distance between left and right shoulder points
- **Waist Length**: Measurement around the waist area
- **Hip Length**: Measurement around the hip area

All measurements are calibrated using the standard inter-eye distance of 6.5 cm as a reference.

## Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

## Project Structure

```
body-metrics-app/
├── src/
│   ├── components/     # React components
│   ├── utils/          # Helper functions
│   ├── App.jsx         # Main application component
│   └── main.jsx        # Entry point
├── public/             # Static assets
├── package.json        # Dependencies and scripts
└── vite.config.js      # Vite configuration
```

## How It Works

1. **Face Detection**: First detects the face and measures the distance between eyes
2. **Pose Estimation**: Identifies key body landmarks (shoulders, waist, hips)
3. **Scale Calculation**: Uses eye distance (6.5 cm) to calculate pixel-to-cm ratio
4. **Measurement Computation**: Calculates body measurements based on detected landmarks
5. **Display Results**: Shows measurements in real-time on screen

## Browser Compatibility

- Chrome/Edge (recommended)
- Firefox
- Safari (latest versions)
- Opera

**Note**: Requires a device with a camera and support for WebGL.

## Privacy & Security

- All processing is done locally in your browser
- No images or data are uploaded to any server
- No data is stored or collected
- Camera access is only used during active measurement sessions

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- TensorFlow.js team for machine learning models
- MediaPipe for pose detection solutions
- The open-source community for various dependencies

## Support

If you encounter any issues or have questions, please open an issue on GitHub.

---

**Note**: This application is for informational purposes. For professional tailoring or medical assessments, please consult qualified professionals.
