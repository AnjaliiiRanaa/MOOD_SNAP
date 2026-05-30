# 📅 Mood Snap App

A sophisticated web application that builds a personalized mood calendar using daily selfies and AI-powered emotion detection. Track your emotional journey through visual snapshots and gain insights into your mood patterns over time.

![Mood Calendar Demo](https://img.shields.io/badge/Status-Active-brightgreen)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28%2B-red)
![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-orange)

## ✨ Features

### 📱 Core Functionality
- **Daily Selfie Capture**: Take daily selfies using your device's camera
- **AI Emotion Detection**: Automatically analyze facial expressions using deep learning
- **Visual Calendar**: Beautiful, interactive calendar showing your mood history
- **Digital Album**: Organized collection of all your selfies with grid and list views
- **Mood Notes**: Add personal notes to your daily mood entries
- **Color-Coded Organization**: Each emotion has its unique color scheme

### 📊 Analytics & Insights
- **Mood Timeline**: Track your emotional journey over time
- **Emotion Distribution**: See which emotions are most common
- **Confidence Metrics**: View AI prediction confidence levels
- **Pattern Recognition**: Identify trends in your emotional well-being

### 💾 Data Management
- **Local Storage**: All selfies and data stored securely on your device
- **Easy Organization**: Automatic file management and organization
- **Data Export**: Access your mood data in JSON format
- **Privacy First**: No cloud storage, complete data privacy

## 🎯 Supported Emotions

The app recognizes 7 core emotions with high accuracy:

| Emotion | Emoji | Description |
|---------|--------|-------------|
| Happy | 😊 | Joy, contentment, satisfaction |
| Sad | 😢 | Sadness, melancholy, disappointment |
| Angry | 😠 | Anger, frustration, irritation |
| Surprise | 😲 | Surprise, amazement, shock |
| Fear | 😨 | Fear, anxiety, worry |
| Disgust | 🤢 | Disgust, revulsion, distaste |
| Neutral | 😐 | Neutral, calm, balanced |

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- Webcam or camera access
- Modern web browser

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/Ayush95697/mood-snap-app.git
cd mood-calendar-app
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Prepare the model**
   - Ensure you have `model.py` containing your `EmotionCNN` class
   - Place your trained model file at `assets/emotion_cnn.pth`

4. **Run the application**
```bash
streamlit run app.py
```

5. **Open in browser**
   - The app will automatically open in your default browser
   - Usually at `http://localhost:8501`

## 📁 Project Structure

```
mood-calendar-app/
├── app.py                 # Main Streamlit application
├── model.py              # EmotionCNN model definition
├── requirements.txt      # Python dependencies
├── README.md            # This file
├── assets/
│   └── emotion_cnn.pth  # Trained PyTorch model
└── mood_selfies/        # Local storage (created automatically)
    ├── mood_data.json   # Mood data storage
    └── *.jpg           # Selfie images
```

## 💻 Usage Guide

### Taking Your First Selfie

1. Navigate to the **"📱 Daily Selfie"** tab
2. Click **"Take a selfie"** to activate your camera
3. Capture your photo when ready
4. The AI will automatically analyze your emotion
5. Add an optional mood note
6. Save to your calendar

### Viewing Your Calendar

1. Go to the **"📅 Calendar"** tab
2. Navigate through months using arrow buttons
3. Click on any date to view details
4. Dates with selfies show emotion emojis
5. Current day is highlighted in blue

### Exploring Your Album

1. Visit the **"📱 Album"** tab
2. Choose between Grid or List view
3. Browse your selfies chronologically
4. Use pagination for large collections

### Analyzing Your Moods

1. Check the **"📊 Insights"** tab
2. View your mood timeline chart
3. See emotion distribution pie chart
4. Track your confidence metrics
5. Identify patterns and trends

## 🛠️ Technical Details

### Model Architecture
- **Framework**: PyTorch
- **Architecture**: Convolutional Neural Network (CNN)
- **Input**: 48x48 grayscale images
- **Output**: 7-class emotion classification
- **Activation**: Softmax for probability distribution

### Data Storage
- **Format**: JSON for metadata, JPEG for images
- **Location**: Local `mood_selfies/` directory
- **Structure**: Date-indexed entries with emotion, confidence, and notes

### Performance
- **Real-time Processing**: Fast emotion detection (<1 second)
- **Accuracy**: High confidence emotion recognition
- **Responsive Design**: Works on desktop and mobile browsers

## 🔧 Configuration

### Model Customization
- Replace `assets/emotion_cnn.pth` with your trained model
- Modify `EMOTION_LABELS` in `app.py` for different emotion sets
- Adjust `EMOTION_COLORS` for custom color schemes

### Storage Settings
- Change `SELFIES_DIR` variable to modify storage location
- Customize image quality in `save_selfie_locally()` function

## 📱 Mobile Support

The app is fully responsive and works on:
- Desktop browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers (iOS Safari, Chrome Mobile)
- Tablet devices

## 🔒 Privacy & Security

- **Local Storage Only**: No data sent to external servers
- **Camera Permissions**: Only used when explicitly requested
- **Data Control**: Full control over your selfies and data
- **No Tracking**: No analytics or user tracking implemented

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Troubleshooting

### Common Issues

**Camera not working:**
- Ensure browser has camera permissions
- Try refreshing the page
- Check if camera is used by another application

**Model not loading:**
- Verify `emotion_cnn.pth` exists in `assets/` directory
- Check model file compatibility with PyTorch version
- Ensure `model.py` contains correct `EmotionCNN` class

**Selfies not saving:**
- Check file system permissions
- Ensure sufficient disk space
- Verify `mood_selfies/` directory can be created

**Performance issues:**
- Use a modern browser
- Ensure good lighting for better detection
- Close other resource-intensive applications

## 📞 Support

For issues and questions:
- Open an issue on GitHub
- Check the troubleshooting section
- Review the usage guide

## 🙏 Acknowledgments

- Built with [Streamlit](https://streamlit.io/)
- Powered by [PyTorch](https://pytorch.org/)
- Visualization by [Plotly](https://plotly.com/)
- Image processing with [OpenCV](https://opencv.org/)

---

**Start your mood tracking journey today!** 📸✨

Take a selfie, track your emotions, and discover patterns in your daily life with the power of AI.
