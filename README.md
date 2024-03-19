# Frames-To-Video Converter
Python program that transforms a file containing base 64 encoded images into video.

## Description

This project provides a Python script that converts a series of base64-encoded images into a single MP4 video file. It's designed to be easy to use, allowing for customization of the frame rate and the option to skip the first image. This tool is perfect for projects where images are dynamically generated or received in base64 format and need to be compiled into a video format for easier viewing or distribution.

## Prerequisites

Before you can use this script, you must have Python installed on your system. The script has been tested with Python 3.7 and above. Additionally, you'll need to install OpenCV, a library used for image and video processing.

## Installation

1. **Clone the Repository**

   Start by cloning the repository to your local machine. You can do this by running the following command in your terminal:

   ```bash
   git clone git@github.com:Fohz67/Frames-To-Video.git
   ```

2. **Install Dependencies**

   This script requires `opencv-python` to run. Install it using pip:

   ```bash
   pip install opencv-python
   ```

## Usage

To use the script, navigate to the directory where you've cloned the repository and ensure the script is executable:

```bash
chmod +x framesToMp4
```

Then, you can run the script with the following command:

```bash
./framesToMp4 <input_file> <fps> <separator> <skip_first>
```

- `input_file`: Path to the file containing the base64-encoded images.
- `fps`: Number of frames per second for the video.
- `separator`: Character used to separate the base64-encoded images in the input file.
- `skip_first`: `true` or `false` indicating whether to skip the first frame.

### Example

```bash
./framesToMp4 myImages.txt 30 "@" true
```

This command reads base64-encoded images from `myImages.txt`, uses `@` as a separator, skips the first image, and compiles the rest into a video at 30 FPS.
