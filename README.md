
# AIP

## Setup Instructions

### Install SAM2
Follow the installation guide from [SAM2 GitHub Repository](https://github.com/facebookresearch/sam2) and install all required dependencies.

### Install FFmpeg
Make sure `ffmpeg` is installed on your system.

Example for Ubuntu:
```bash
sudo apt update
sudo apt install ffmpeg
```

## Frame Extraction from Video

- Create a directory inside sam2/notebooks/videos to store extracted frames:
  ```bash
  mkdir -p 18
  ```
- Extract every 10th frame from the input video:
  ```bash
  ffmpeg -i input_video.mp4 -vf "select=not(mod(n\,10))" -vsync vfr -q:v 2 18/%06d.jpg
  ```

## Running the Code

- Download the `mouse.ipynb` notebook from this repository into sam2/notebooks.
- Open and run the `mouse.ipynb` notebook to proceed with the analysis.

## Pose Estimation

- Install and set up Pose Estimation tools by following this [YouTube Tutorial](https://www.youtube.com/watch?v=ofFx0vTMSxE).
- Adjust parameters according to your project's requirements.
