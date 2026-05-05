# Birds Species Image Classification

A deep learning web application that identifies **525 bird species** from images using a Convolutional Neural Network (CNN) trained with TensorFlow/Keras.

## Demo

Upload a photo or paste an image URL and the model will predict the bird species with a confidence score.

## Model

| Metric | Value |
|---|---|
| Architecture | CNN (Conv → Pool × 3 layers) |
| Training accuracy | ~96% |
| Validation accuracy | ~49% |
| Number of classes | 525 bird species |
| Training images | 84 635 |
| Validation images | 2 625 |
| Test images | 2 625 |
| Input size | 224 × 224 px |

## Dataset

[525 Birds Species — Image Classification](https://www.kaggle.com/datasets/gpiosenka/100-bird-species) from Kaggle.

> The dataset is **not** included in this repository due to its size (≈ 2.1 GB).  
> Download it from Kaggle and place it in `dataset/`.

## Project Structure

```
├── app.py                                   # Streamlit web app
├── birds-pics-classification-model.ipynb   # Training notebook
├── model.keras         # Trained model weights
├── requirements.txt                         # Python dependencies
├── schemaCNN.svg                            # CNN architecture diagram
├── dataset/                                 # Dataset (not tracked by Git)
│   ├── birds.csv
│   ├── train/
│   ├── valid/
│   └── test/
├── Images/                                  # Sample test images
└── POC/                                     # Feature-map visualizations "Proof Of Concept"
```

## Getting Started

### Prerequisites

- Python 3.10

### Installation

```bash
# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate          # Linux / macOS
# venv\Scripts\activate           # Windows

# Install dependencies
pip install -r requirements.txt
```

### Run the app

```bash
streamlit run app.py
```

Then open [http://localhost:8501](http://localhost:8501) in your browser.
