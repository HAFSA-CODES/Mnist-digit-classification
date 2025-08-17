

## Project Title:  
MNIST Handwritten Digit Classification and Analysis  

---

## Introduction  
This project focuses on building, training, and testing machine learning models using the **MNIST dataset** of handwritten digits (0–9). The purpose of this work is to explore various classification techniques, analyze misclassifications, and demonstrate model predictions. Additionally, an interactive **Gradio web application** has been created to allow users to upload or draw digits for real-time predictions.  

---

## Code Discussion  

### 1. Loading and Preparing Data  
- The dataset used is **MNIST**, a large set of handwritten digits.  
- The images are flattened into vectors of 28x28 = 784 features.  
- The dataset is split into training and testing sets for evaluation.  

### 2. Misclassification Analysis  
- Models often confuse digits that look similar (e.g., `5` and `8`).  
- The code filters test samples where:  
  - The actual digit is `5`.  
  - The model incorrectly predicts `8`.  
- A custom function `plot_digits` is used to visualize these errors.  
- This analysis helps understand model weaknesses.  

### 3. Models Trained  
- **SGDClassifier (Stochastic Gradient Descent):**  
  - A linear classifier useful for large-scale datasets.  
- **RandomForestClassifier:**  
  - An ensemble model using multiple decision trees.  
- Both models are trained and stored using **joblib** for later use.  

### 4. Interactive Gradio Application  
- An interactive **Gradio app** was created to test the models.  
- Features:  
  - Users can upload or draw a digit.  
  - The image is preprocessed (grayscale, resized, inverted if needed).  
  - The model then predicts the digit.  
- Output:  
  - **SGDClassifier**: Shows a single digit prediction.  
  - **RandomForestClassifier**: Displays top-3 predictions with probabilities.  

---

## Example Results  
- Misclassification example: Digit `5` incorrectly classified as `8`.  
- Gradio prediction:  
  ```
  SGD Prediction: 3
  RF Top 3 Predictions: { '3': 98.7%, '8': 1.1%, '5': 0.2% }
  ```  

---

## Conclusion  
This project demonstrates:  
- How different classifiers perform on the MNIST dataset.  
- How to analyze and visualize misclassifications.  
- The integration of an interactive **Gradio app** for practical usage.  

Future work could include adding **deep learning models (CNNs)** for better accuracy and deploying the app to platforms like **Hugging Face Spaces**.  

-------------------------------------------------------------------------------------------------------------------------
