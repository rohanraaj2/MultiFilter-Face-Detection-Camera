# Multi Filter Face Detection Camera

A real-time video processing application that captures video from a camera, applies various image processing operations, and outputs the processed video to a virtual camera for use in applications like Zoom, Discord, or OBS Studio.

## 🎯 Project Overview

This project was developed as part of a Computer Vision course at Technische Hochschule Ingolstadt. It demonstrates real-time image processing capabilities including statistical analysis, filtering operations, and face recognition.

## ✨ Features

### Core Functionality
- **Real-time video capture** from physical camera using OpenCV
- **Virtual camera output** using pyvirtualcam for integration with video conferencing apps
- **Live histogram visualization** with RGB channel analysis
- **Interactive controls** for switching between different processing modes

#### Transformations & Filters:
- **Linear Transformation** - Contrast and brightness adjustment
- **Histogram Equalization** - Automatic contrast enhancement
- **Edge Detection** - Sobel filter for edge highlighting
- **Gaussian Blur** - Smoothing filter
- **Sharpen Filter** - Detail enhancement
- **Gabor Filter** - Texture analysis and pattern detection

### Special Feature - Face Recognition
- **Face identification** with known faces from image database
- **Privacy protection** with automatic face blurring for unknown individuals
- **Visual indicators** with bounding boxes and name labels

## 🚀 Installation & Setup

### Prerequisites
- Python 3.8 or higher
- OBS Studio (for virtual camera functionality)
- Compatible webcam

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/rohanraaj2/Virtual-Camera.git
   cd Virtual-Camera
   ```

2. **Install required packages:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Setup face recognition (optional):**
   - Add face images to the `images/` directory
   - Supported formats: .jpg, .png
   - Name files as "PersonName.jpg" for automatic recognition

4. **Install OBS Studio:**
   - Download from [https://obsproject.com](https://obsproject.com)
   - Install virtual camera plugin if needed

## 🎮 Usage

### Running the Application

```bash
python run.py
```

### Interactive Controls

| Key | Function |
|-----|----------|
| `1` | Original image (no filter) |
| `2` | Linear transformation |
| `3` | Histogram equalization |
| `4` | Edge detection |
| `5` | Gaussian blur |
| `6` | Sharpen filter |
| `7` | Gabor filter |
| `S` | Toggle statistics display |
| `Q` | Quit application |

### Virtual Camera Setup

1. Start the application with `python run.py`
2. Open OBS Studio
3. Add "Video Capture Device" source
4. Select "OBS Virtual Camera" as device
5. The processed video feed will appear in OBS
6. Use OBS Virtual Camera in your video conferencing application

## 🔧 Technical Implementation

### Architecture Overview
```
[Physical Camera] → [OpenCV Capture] → [Image Processing] → [Virtual Camera] → [Output Applications]
```

## 🤝 Contributing

This project was developed as part of an academic assignment. Contributions and improvements are welcome for educational purposes.

## 📝 License

This project is developed for educational purposes as part of a university course.

## 👥 Authors

Developed by students at Technische Hochschule Ingolstadt under the guidance of Professor Dominik Rößle.

## 🔗 References

- [pyvirtualcam Documentation](https://github.com/letmaik/pyvirtualcam)
- [OpenCV Documentation](https://docs.opencv.org/)
- [Face Recognition Library](https://github.com/ageitgey/face_recognition)
- [OBS Studio](https://obsproject.com)