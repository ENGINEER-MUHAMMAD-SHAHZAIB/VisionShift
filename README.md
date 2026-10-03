
<h1 align="center">VisionShift</h1>

<p align="center">
  **VisionShift** enables seamless real-time face swapping and video deepfakes with just a single image and a single click. Leverage AI to effortlessly transform video content in an instant and explore advanced visual effects.
</p>

<p align="center">
  <a href="https://trendshift.io/repositories/11395" target="_blank"><img src="https://trendshift.io/api/badge/repositories/11395" alt="hacksider%2FDeep-Live-Cam | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>
</p>

<p align="center">
  <img src="media/demo.gif" alt="Demo GIF" width="800">
</p>

## Disclaimer

This software aims to enhance the AI-generated media industry, supporting tasks like animating custom characters or creating digital models. 

**Important Notes:**
- The software has built-in checks to prevent processing inappropriate media (e.g., nudity, war footage).
- Users must respect ethical guidelines and obtain consent when using real people's faces.
- The software may be modified or shut down if legally required.

## Quick Start - Pre-built Versions

**For Windows / NVIDIA GPU:**
  - [Download Pre-built Version (Windows)](https://hacksider.gumroad.com/l/vccdmm)

**For Mac / Apple Silicon:**
  - [Download Pre-built Version (Mac)](https://krshh.gumroad.com/l/Deep-Live-Cam-Mac)

> These pre-built versions are ideal for non-technical users who want a quick setup. Manual installation is also available for advanced users.

## TLDR: Live Deepfake in 3 Easy Steps

1. **Select a face**: Choose the face to swap.
2. **Choose your camera**: Select the camera source.
3. **Press Live!**: See the magic in real-time!

## Features & Uses - Real-time Face Swapping

### 1. **Mouth Mask**
   - Retain original mouth movements for natural realism.
   - ![Mouth Mask](media/ludwig.gif)

### 2. **Face Mapping**
   - Swap faces across multiple subjects in a scene.
   - ![Face Mapping](media/streamers.gif)

### 3. **Movie Mode**
   - Replace faces in movies in real-time.
   - ![Movie Mode](media/movie.gif)

### 4. **Live Shows**
   - Perfect for live performances or streaming.
   - ![Live Show](media/live_show.gif)

### 5. **Memes**
   - Create viral memes with ease.
   - ![Meme Creation](media/meme.gif) 
   - *Created using Deep-Stream-Cam*

## Installation (Manual Setup)

> **Note**: Installation requires technical skills. For easier use, consider the pre-built versions.

<details>
<summary>Click for Installation Instructions</summary>

### Requirements
- Python 3.10 (recommended)
- pip
- git
- [ffmpeg](https://www.youtube.com/watch?v=OlNWCpFdVMA)
- [Visual Studio 2022 Runtimes (Windows)](https://visualstudio.microsoft.com/visual-cpp-build-tools/)

### Steps to Install

1. **Clone the Repository**

```bash
git clone https://github.com/hacksider/Deep-Live-Cam.git
cd Deep-Live-Cam
```

2. **Download Models**

   - [GFPGANv1.4](https://huggingface.co/hacksider/deep-live-cam/resolve/main/GFPGANv1.4.pth)
   - [inswapper_128_fp16.onnx](https://huggingface.co/hacksider/deep-live-cam/resolve/main/inswapper_128_fp16.onnx)

   Place these files in the `models` folder.

3. **Install Dependencies**

```bash
pip install -r requirements.txt
```

4. **Run the Application**

```bash
python run.py
```

### GPU Acceleration (Optional)

For enhanced performance, use GPU acceleration for processing:

**CUDA (NVIDIA GPU)**

1. Install [CUDA Toolkit](https://developer.nvidia.com/cuda-11-8-0-download-archive).
2. Install dependencies:
```bash
pip uninstall onnxruntime onnxruntime-gpu
pip install onnxruntime-gpu==1.16.3
```
3. Run the application:
```bash
python run.py --execution-provider cuda
```

**CoreML (Apple Silicon)**

1. Install dependencies:
```bash
pip uninstall onnxruntime onnxruntime-silicon
pip install onnxruntime-silicon==1.13.1
```
2. Run:
```bash
python run.py --execution-provider coreml
```

</details>

## Usage

### Image/Video Mode
1. Run `python run.py`.
2. Select source and target images/videos.
3. Click "Start" to process.

### Webcam Mode
1. Run `python run.py`.
2. Choose source face image.
3. Click "Live" to start webcam mode and preview.
4. Stream with OBS or any screen capture tool.

## Command-Line Arguments

Here’s a quick overview of the available command-line options:
- `-s SOURCE_PATH`: Select a source image.
- `-t TARGET_PATH`: Choose a target image or video.
- `--mouth-mask`: Use the mouth mask feature.
- `--live-mirror`: Live camera mirror.
- `-v, --version`: Show version info.

For full list, refer to the [CLI documentation](#Command-Line-Arguments).

## Press Coverage

**VisionShift** has garnered attention for its groundbreaking AI-powered face-swapping capabilities:

- [Ars Technica: "Deep-Live-Cam goes viral"](https://arstechnica.com/information-technology/2024/08/new-ai-tool-enables-real-time-face-swapping-on-webcams-raising-fraud-concerns/)
- [PetaPixel: "Deepfake AI Tool Lets You Become Anyone in a Video Call"](https://petapixel.com/2024/08/14/deep-live-cam-deepfake-ai-tool-lets-you-become-anyone-in-a-video-call-with-single-photo-mark-zuckerberg-jd-vance-elon-musk/)
- [NewsBytes: "This free AI tool lets you become anyone during video-calls"](https://www.newsbytesapp.com/news/science/deep-live-cam-ai-impersonation-tool-goes-viral/story)

## Credits

Thanks to the following contributors:
- [ffmpeg](https://ffmpeg.org/): for video processing.
- [deepinsight](https://github.com/deepinsight): for face detection models.
- [havok2-htwo](https://github.com/havok2-htwo): for webcam integration.
- Special thanks to all contributors for their dedication and support.

---
