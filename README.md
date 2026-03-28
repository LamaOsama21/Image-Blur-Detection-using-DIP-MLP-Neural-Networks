# 📸 Image Blur Detection using DIP & MLP Neural Networks

An advanced Computer Vision project that combines **Digital Image Processing (DIP)** for feature extraction with a **Multi-Layer Perceptron (MLP)** neural network to classify images as Sharp or Blurry.

## Project Architecture
This project follows a hybrid approach:
1. **Feature Extraction (DIP):** Instead of raw pixels, we feed the network specific mathematical features that describe image clarity.
2. **Classification (MLP):** A fully connected Neural Network trained to weigh these features and make a final prediction.

### 🔬 Extracted Features
The model analyzes the following characteristics of each image:
* **Laplacian Variance:** Captures the intensity of edges (Sharp images have higher variance).
* **Tenengrad:** Measures the gradient magnitude to determine focus level.
* **FFT (Fast Fourier Transform):** Analyzes the frequency spectrum. Blurry images lack high-frequency components.
* **Edge Density:** Calculates the ratio of edge-pixels to the total surface area.



## The Model: Multi-Layer Perceptron (MLP)
We utilized a **Scikit-Learn MLPClassifier** with the following configuration:
* **Hidden Layers:** [e.g., 100, 50] neurons to capture non-linear relationships.
* **Activation Function:** `ReLU` for efficient gradient propagation.
* **Optimizer:** `Adam` for robust weight updates.



## Results
* **Dataset:** Trained on the [Blur Dataset](https://www.kaggle.com/datasets/kwentar/blur-dataset) (Motion, Defocused, and Sharp images).
* **Accuracy:** Over **94%**

## How to Run
1. Clone the repository.
2. Install dependencies: `pip install -r requirements.txt`.
3. Run the script
*(Note: The script auto-downloads the dataset using kagglehub).*
