# AI-Basketball-Shot-Analysis
Final year Computer Science project: AI-powered basketball shot analysis using pose estimation and ball tracking.
# 🏀 AI-Powered 3D Basketball Shot Analysis System

This repository contains my final year university computing project — an AI-powered system that analyzes basketball free throw performance using pose estimation, ball tracking, and trajectory comparison. Implemented entirely in a Jupyter Notebook, the system provides rapid feedback through cloud deployment (Google Colab).

## 🎯 Project Overview

The system processes video footage of basketball free throws and performs:
- **2D and 3D human pose estimation** with MMPose
- **Ball detection** using a custom-trained YOLOv11 model
- **Trajectory analysis** to estimate release angle and motion
- **Similarity evaluation** using Dynamic Time Warping (DTW)

All processing is done within a single Google Colab-compatible notebook.

## 🧪 Technologies Used

- Python · Jupyter Notebook · PyTorch · Roboflow
- MMPose (HRNet) · YOLOv11
- Google Colab · FFmpeg
- Gradio (for visual feedback interface)

## 🚀 How to Use in Google Colab

1. **Open Google Colab**  
   - Set Runtime: `Runtime > Change runtime type > GPU`

2. **Upload Project Files**  
   - Place the entire `ComputingProject` folder inside `/content/` in Colab.

3. **Install Dependencies**  
   - At the top of `FreethrowAnalysisStableFinal.ipynb`, run the provided install cells.
   - These automatically install: Ultralytics YOLO, Gradio, and all required libraries.
   - install mmpose into the ComputingProject Folder
     ```bash
git clone https://github.com/open-mmlab/mmpose.git
cd mmpose
pip install -v -e .  # Editable install
      ```

4. **Run the System**  
   - Execute the notebook cells in sequence.
   - After all functions are defined, interact either via code blocks or using the Gradio interface at the bottom.

📌 _No additional setup is needed. All pretrained weights, teacher keypoints, and assets are included for cloud execution._

⚠️ _Note: While the interface lists two teacher sequences, only **"SGA"** is functional (based on `FT_Train1.mp4`). For testing, use `FT_Train2.mp4` or `ButlerFT_Full2.mp4`._

## 📝 Files Included

- `FreethrowAnalysis.ipynb` — Final cleaned notebook
- `Basketball_shot-Analysis_Report.pdf` — Full written dissertation/report
- `requirements.txt` — Python dependency list for local setup
- `inputVideos/` — Videos used for testing and training of models and full pipeline, can be used for demo purposes

## ⚙️ Setup for Local Use (Optional, Requires compatible Nvidia GPU)

If you want to run outside Colab:

```bash
pip install -r requirements.txt
```
