# AI Reel & Shorts Generator

A full-stack automated video creation tool that turns a collection of uploaded images and a text script into a fully rendered, ready-to-post vertical video (1080x1920). 

It uses **Flask** for the web interface, the **ElevenLabs API** for ultra-realistic AI voiceovers, and **FFmpeg** to stitch the audio and images together into an MP4 Reel/Short.

##  Features
- **Web Interface:** Easy-to-use UI to upload images and input your video's script.
- **AI Voiceovers:** Integrates with ElevenLabs (Flash v2.5 model) to generate high-quality, human-like voiceovers from your text.
- **Automated Video Editing:** Uses FFmpeg to automatically scale, pad, and concatenate images to fit TikTok/Reels/Shorts dimensions (1080x1920) synced with the generated audio.
- **Background Processing:** A dedicated worker script constantly monitors the upload queue and processes videos in the background without freezing the web interface.
- **Video Gallery:** View all your generated AI reels directly from the web app.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:
1. **Python 3.x**
2. **FFmpeg** (Must be installed and added to your system's PATH). 
   - *Windows:* [Download here](https://ffmpeg.org/download.html) or use `winget install ffmpeg`
   - *Mac:* `brew install ffmpeg`
   - *Linux:* `sudo apt install ffmpeg`
3. An **ElevenLabs API Key** ([Get one here](https://elevenlabs.io/)).

## Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/kajalmaurya4311/VidSnapAI.git
   cd VidSnapAI
