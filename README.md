# ✂️ ai-clipping-comfyui - Create viral short videos from long clips

[![Download AI Clipping](https://img.shields.io/badge/Download-Visit_Repository-blue.svg)](https://github.com/dyanatonsured315/ai-clipping-comfyui)

ai-clipping-comfyui allows you to transform long videos into short clips for TikTok, Instagram Reels, and YouTube Shorts. You use this tool within the ComfyUI platform to automate the clipping process. It tracks faces, calculates video quality, and crops footage to a vertical format automatically.

## 🖥️ System Requirements

Before you install this software, confirm your computer meets these requirements:

- Operating System: Windows 10 or 11
- Processor: Modern multi-core CPU (Intel i5 or AMD Ryzen 5 or higher)
- Memory: 16GB RAM minimum
- Graphics Card: NVIDIA GPU with at least 8GB of VRAM
- Storage Space: 5GB available disk space
- Software: You must have a working ComfyUI installation

## 📥 Installation Steps

Follow these steps to install the tool on your machine.

1. Visit this page to download: [https://github.com/dyanatonsured315/ai-clipping-comfyui](https://github.com/dyanatonsured315/ai-clipping-comfyui)
2. Locate the "Code" button on the top right side of the page.
3. Click "Download ZIP" to save the files to your computer.
4. Extract the contents of the ZIP folder to your ComfyUI custom nodes directory. This folder is usually located at `ComfyUI/custom_nodes/`.
5. Open your ComfyUI environment.
6. Restart ComfyUI to load the new nodes.
7. Confirm that the new nodes appear in your node list by right-clicking in the workflow area.

## 🛠️ How to Use the Tool

This tool uses a node-based system to clip your videos. Follow this manual process to start generating short clips:

1. Load your long-form video or podcast file into the input loader node.
2. Connect the output of the loader to the Whisper transcription node. This node generates the text for your video.
3. Link the transcription node to the virality ranking node. This node identifies the most engaging parts of your video based on content quality.
4. Connect the ranking output to the deduplication node. This step removes visual noise and keeps only unique segments.
5. Send the result to the face-tracked auto-crop node. This node keeps your target subject in the center of the vertical video frame.
6. Select your output format and resolution.
7. Click "Queue Prompt" to begin the automation.

The software processes the video on your server. You can monitor progress through the ComfyUI terminal window.

## ⚙️ Configuration Details

You can change how the software functions using the settings panel in the node.

Virality Ranking:
The software ranks segments based on energy and speech patterns. You can adjust the sensitivity setting if you want to find more clips. A higher sensitivity value results in more granular clips, while a lower value provides longer, broader clips.

Face Tracking:
The face tracker follows individuals in the frame. You can specify a "target subject" if the video features multiple people. The software will prioritize the face of the person you select.

Deduplication:
This feature identifies repetitive segments and overlapping timestamps. It removes duplicate frames to ensure your final export contains only fresh content.

## ⚡ Performance Tips

AI video processing requires significant computer power. To ensure smooth performance, follow these recommendations:

- Close all other resource-heavy programs, such as web browsers or photo editors, while running the clipping process.
- Keep your NVIDIA drivers updated to the latest version to ensure compatibility with the clipping nodes.
- Ensure your GPU is not busy with other tasks like gaming.
- Process videos in batches if your computer runs out of memory. Start with one 10-minute video to test your system limits before trying a full two-hour podcast.

## ❓ Frequently Asked Questions

What file types does this tool support?
The software supports standard video formats like MP4, MOV, and AVI. 

Where do my videos save?
You can set your output directory in the output save node. By default, the software saves clips to the `ComfyUI/output/` folder.

Does this tool require an internet connection?
The nodes run locally on your machine. You only need an internet connection to download the required software and initial model files.

What if the face tracking misses?
The face tracker relies on standard identification models. If the lighting is poor or the subject moves too quickly, the tracker might lose focus. Adjust the smoothing setting in the node to help the camera transition more gracefully between positions.

Can I change the video aspect ratio?
The tool is built for vertical video formats common for Shorts and Reels. You can adjust the crop area in the auto-crop node settings to suit different platform requirements.

Keywords: ai-clipping, ai-video-clipper, auto-crop, comfyui, comfyui-custom-nodes, comfyui-nodes, face-tracking, highlight-extraction, instagram-reels, muapi, opus-clip, opus-clip-alternative, podcast-clipper, short-form-video, tiktok, vertical-video, video-clipping, viral-clips, whisper, youtube-shorts