# 2.Preprocessing-and-Contour-Based-Tumor-Detection-from-Brain-MRI

> A classical computer vision pipeline to preprocess, segment, and visualize brain tumor regions from MRI images using OpenCV techniques like Gaussian Blur, Thresholding, Morphological Filtering, and Contour Detection.

---

## 📌 Overview

This project demonstrates an end-to-end brain tumor segmentation pipeline using traditional computer vision techniques. It focuses on:

* Image preprocessing
* Threshold-based segmentation
* Morphological filtering
* Contour extraction for tumor boundary visualization

---

## 🛠️ Tech Stack

* **Language:** Python 3
* **Libraries:** OpenCV, NumPy, Matplotlib
* **Dataset:** [Brain MRI Images for Brain Tumor Detection (Kaggle)](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)

---

## 🧪 Pipeline Steps

| Step | Name                    | Description                                 |
| ---- | ----------------------- | ------------------------------------------- |
| 1    | Load MRI Image          | Read from file using `cv2.imread()`         |
| 2    | Grayscale Conversion    | Convert to single-channel for processing    |
| 3    | Gaussian Blur           | Remove noise using blurring                 |
| 4    | Otsu’s Thresholding     | Segment foreground (tumor) from background  |
| 5    | Morphological Filtering | Clean the binary mask using opening/closing |
| 6    | Contour Detection       | Detect tumor region boundaries              |
| 7    | Visualization           | Draw contours on original image             |

---

## 📂 Folder Structure

```
BrainTumorSeg/
├── brain_tumor_data/         # Downloaded Kaggle dataset
├── segmentation_pipeline.py  # Main Python file
├── results/                  # Output images with contours
├── README.md                 # Project documentation
└── requirements.txt          # Python dependencies
```

---

## ▶️ Run Instructions

1. ✅ Install required libraries:

```bash
pip install opencv-python numpy matplotlib
```

2. ✅ Run the pipeline:

```bash
python segmentation_pipeline.py
```

3. ✅ OR use Colab:

```python
# Upload kaggle.json and mount drive
from google.colab import drive
drive.mount('/content/drive')
```

---

## 🔍 Example Result

| Original MRI              | Thresholded                | Segmented Tumor          |
| ------------------------- | -------------------------- | ------------------------ |
| ![](results/original.jpg) | ![](results/threshold.jpg) | ![](results/contour.jpg) |

---

## 📈 Future Improvements

* Add deep learning-based segmentation (U-Net/CNN)
* Evaluate segmentation with Dice Coefficient / IoU
* Annotate and save masks as PNG files
* Deploy with Streamlit or Flask for real-time use

---

## 🤝 Acknowledgments

* Kaggle dataset by [Navoneel Chakrabarty](https://www.kaggle.com/navoneel)
* OpenCV for classical CV operations
* You! for exploring medical imaging solutions 💙

---

## 📜 License

MIT License. Feel free to use, modify, and share with credits.


