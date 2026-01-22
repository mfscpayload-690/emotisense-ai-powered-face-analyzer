# EmotiSense

<div align="center">

![EmotiSense Logo](https://img.shields.io/badge/EmotiSense-7c3aed?style=for-the-badge)
![Version](https://img.shields.io/badge/version-2.0-blue?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
![Demo](https://img.shields.io/badge/demo-live-brightgreen?style=flat-square)

**Real-time Facial Expression & Eye Tracking with AI-Powered Mood Insights**

[Features](#features) • [Quick Start](#quick-start) • [How It Works](#how-it-works) • [Configuration](#configuration)

</div>

---

## Features

### Expression Detection
- **7 Emotion Recognition**: Happy, Sad, Angry, Surprised, Fearful, Disgusted, Neutral
- **Real-time Confidence Scoring**: Detection confidence for each emotion
- **Visual Progress Bars**: Live visualization of all emotion probabilities
- **Smooth Transitions**: Animated UI updates as expressions change

### Eye Tracking
- **Blink Rate Monitoring**: Tracks blinks per minute
- **Gaze Stability Analysis**: Measures focus steadiness
- **Eye State Indicators**: Visual feedback for left/right eye open/closed states
- **EAR-based Detection**: Uses Eye Aspect Ratio for accurate tracking

### AI-Powered Analysis
- **Local AI Processing**: Uses Ollama for privacy-first analysis
- **Contextual Insights**: Understands emotion and eye data together
- **Natural Language Feedback**: Conversational mood assessments
- **No Cloud Required**: All processing runs on your local machine

### Sudden Change Alerts
- **Rapid Emotion Detection**: Catches sudden shifts in expression
- **Alert Logging**: Maintains history of detected changes
- **Visual Notifications**: Animated banner alerts
- **Timestamped Events**: Tracks when changes occurred

### Session Analytics
- **Duration Tracking**: Monitor session length
- **Emotion Change Counter**: Track expression transitions
- **Dominant Emotion**: Identifies your most common expression
- **Snapshot Capture**: Save moments with one click

---

## Quick Start

### Prerequisites
- Modern web browser (Chrome, Firefox, or Edge)
- Webcam with access permissions
- (Optional) [Ollama](https://ollama.ai/) for AI-powered analysis

### Installation Steps

#### 1. Clone the Repository
```bash
git clone https://github.com/mfscpayload-690/emotisense-ai-powered-face-analyzer.git
cd emotisense-ai-powered-face-analyzer
```

#### 2. Run the Application

**Option A: Direct File Access** (Basic)
```bash
# Windows
start index.html

# macOS
open index.html

# Linux
xdg-open index.html
```

**Option B: Local Development Server** (Recommended)

Running via a local server ensures all features work correctly and prevents CORS issues:

```bash
# Using npx (requires Node.js)
npx http-server . -p 8080

# Then navigate to http://localhost:8080 in your browser
```

Alternatively, you can use Python's built-in server:

```bash
# Python 3.x
python -m http.server 8080

# Then navigate to http://localhost:8080 in your browser
```

#### 3. Enable AI Analysis (Optional)

For advanced AI-powered mood insights:

1. **Install Ollama**: Download and install from [https://ollama.ai](https://ollama.ai/)
2. **Pull the Required Model**:
   ```bash
   ollama run qwen2.5-coder:7b-instruct-q4_K_M
   ```
3. **Verify Ollama is Running**: The application will automatically connect to `http://localhost:11434`

**Note**: AI analysis is optional. The application will function without it, providing expression and eye tracking features.

---

## How It Works

1. **Start Analysis**: Click the start button and grant camera access permissions
2. **Face Detection**: AI models detect your face and 68 facial landmarks
3. **Expression Analysis**: Neural network classifies your expression in real-time
4. **Eye Tracking**: Facial landmarks track eye openness and gaze stability
5. **AI Insights**: Local LLM provides contextual mood analysis (if Ollama is configured)

---

## Technology Stack

| Component | Technology |
|-----------|------------|
| Face Detection | [face-api.js](https://github.com/justadudewhohacks/face-api.js) |
| Landmarks | 68-point facial landmark model |
| Expressions | Pre-trained expression classifier |
| AI Analysis | [Ollama](https://ollama.ai/) (local LLM) |
| UI Framework | Vanilla JavaScript + CSS3 |
| Fonts | [Inter](https://fonts.google.com/specimen/Inter) |

---

## Configuration

You can customize the application by modifying the following constants in `index.html`:

```javascript
// AI Settings
const OLLAMA_URL = 'http://localhost:11434';  // Ollama endpoint URL
const MODEL = 'qwen2.5-coder:7b-instruct-q4_K_M';  // LLM model name
const AI_INTERVAL = 3000;  // Analysis frequency in milliseconds
```

Adjust these values based on your Ollama setup and performance requirements.

---

## Metrics Explained

| Metric | Description | Normal Range |
|--------|-------------|--------------|
| **Blink Rate** | Blinks per minute | 15-20 |
| **Gaze Stability** | Focus steadiness | High/Med/Low |
| **Confidence** | Detection certainty | 0-100% |
| **Emotion Changes** | Expression transitions | Varies |

---

## UI Features

- **Glassmorphism Design**: Modern frosted glass effects
- **Dark Theme**: Easy on the eyes for extended use
- **Responsive Layout**: Optimized for desktop and tablet devices
- **Smooth Animations**: Polished micro-interactions
- **Gradient Accents**: Violet to pink color scheme

---

## Disclaimer

> **For Demonstration Purposes Only**: Expression detection is approximate and may vary based on individual characteristics, lighting conditions, and camera quality. This tool is NOT intended for clinical, diagnostic, or professional assessment purposes. All processing occurs locally on your machine; no data is transmitted to external servers.

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

<div align="center">

**Developed for the open-source community**

[Report Bug](../../issues) • [Request Feature](../../issues)

</div>
