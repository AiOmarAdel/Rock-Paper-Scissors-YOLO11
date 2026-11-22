# Rock Paper Scissors Detection using YOLO11

A Computer Vision project that detects and classifies hand gestures representing **Rock, Paper, and Scissors** using the YOLO11 object detection model.

The project focuses on custom dataset preparation, model training, evaluation, and visualizing object detection results.

## Project Overview

Rock Paper Scissors is a hand gesture recognition problem. In this project, YOLO11 is used to detect and classify three different hand gestures:

- **Rock**
- **Paper**
- **Scissors**

The model was trained on a custom dataset to recognize these gestures from images.

## Technologies & Tools

- Python
- YOLO11 (Ultralytics)
- PyTorch
- OpenCV
- NumPy
- Matplotlib
- Google Colab

## Dataset

The dataset contains images representing the three hand gesture classes:

| Class | Description |
|---|---|
| Rock | Closed fist |
| Paper | Open hand |
| Scissors | Two fingers extended |

The dataset was prepared in YOLO format, including images and corresponding annotation files.

## Model Training

The YOLO11 model was trained using the prepared dataset.

The training process included:

- Dataset preparation and organization.
- Model configuration.
- Training and validation.
- Performance evaluation.
- Saving the trained model weights.

## Model Evaluation

The model was evaluated using standard object detection metrics:

- Precision
- Recall
- mAP@50
- mAP@50-95
- Confusion Matrix

## Project Structure

```text
Rock-Paper-Scissors-YOLO11/
│
├──  best.pt
│
├── notebooks/
│   └── main.ipynb
│   └── Notebook.ipynb
│
├── requirements.txt
├── .gitignore
└── README.md
```

*Note: The structure above is a suggested organization. Adjust it to match the files uploaded to the repository.*

## Installation

Clone the repository:

```bash
git clone https://github.com/AiOmarAdel/Rock-Paper-Scissors-YOLO11.git
cd Rock-Paper-Scissors-YOLO11
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

Load the trained YOLO11 model:

```python
from ultralytics import YOLO

model = YOLO("best.pt")
```

Run prediction on an image:

```python
results = model.predict(
    source="test_image.jpg",
    conf=0.25,
    save=True
)
```

Run real-time detection using a webcam:

```python
results = model.predict(
    source=0,
    show=True,
    conf=0.25
)
```

Press `Q` to stop the webcam detection.

## Future Improvements

- Improve detection accuracy with more diverse training images.
- Test the model under different lighting conditions and backgrounds.
- Optimize real-time inference performance.
- Experiment with different YOLO model sizes.

## Author

**Omar Adel Abdul Hakam**

AI Student | Computer Vision | Machine Learning & Deep Learning

GitHub: [@AiOmarAdel](https://github.com/AiOmarAdel)

---

If you find this project useful, feel free to ⭐ the repository!
