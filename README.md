# Pancreatic-Cancer-Detection-using-Deep-Learning 🧠🩺

An experimental deep-learning project to detect or classify pancreatic cancer (or abnormalities) from medical image / data inputs.  
This repository contains the code, data pipeline and instructions needed to run the detection model locally (or retrain if needed).

---

## 🔎 Project Overview

Many forms of pancreatic cancer (like pancreatic ductal adenocarcinoma) are difficult to diagnose at early stage, and imaging-based detection using deep learning can potentially help in early detection and decision support for clinicians. :contentReference[oaicite:1]{index=1}

This project aims to build a prototype deep-learning system that:

- Ingests medical imaging data (e.g. CT scans) or appropriately preprocessed dataset  
- Trains a neural-network model to classify or detect presence/absence of pancreatic tumor  
- Provides evaluation metrics (accuracy, sensitivity, specificity, AUC etc.) — helping compare with standard diagnostic baselines  
- Is organized for further extension, experimentation, and research  

---

## 📂 Repository Structure

```text
Pancreatic-Cancer-Detection-using-Deep-Learning-main/
│   analyze_cnn_performance.py     # Script to analyze CNN model performance
│   app.py                         # Flask web application for prediction
│   main.py                        # Main entry point for the project
│   run_experiment.py              # Script to run experiments
│   LICENSE                        # Project license
│   README.md                      # Project documentation
│
├── dataset/                       # Raw image dataset
│   ├── 1-001.jpg
│   ├── 1-002.jpg
│   ├── ...
│   └── 1-239.jpg
│
├── experiment_results/           # Saved experiment outputs and visualizations
│   │   cancer_type_predictions.json
│   │   comparison_chart.png
│   │   experiment_results.json
│   │   experiment_summary.md
│   │   generate_visualizations.py
│   │   metrics_comparison.png
│   │   random_forest_confusion_matrix.png
│   │   rule_based_confusion_matrix.png
│   │   time_comparison.png
│   │
│   ├── test/                      # Test images
│   └── train/                     # Training images
│
├── static/                        # Static files for web app
│   ├── css/
│   │   └── custom.css
│   └── js/
│       └── main.js
│
├── templates/                     # HTML templates for Flask app
│   ├── about.html
│   ├── index.html
│   ├── layout.html
│   └── process.html
│
├── utils/                         # Utility functions and helper scripts
│   │   cnn_performance.py
│   │   dataset_utils.py
│   │   image_processing.py
│   │   model_utils.py
│   │   visualize_model.py
│   └── __pycache__/
│
└── __pycache__/                   # Compiled Python cache files



## 🛠️ Tech Stack & Tools

- **Programming Language:** Python  
- **Deep Learning:** Convolutional Neural Networks (CNN)  
- **Web Framework:** Flask  
- **Image Processing:** OpenCV  
- **Data Handling:** NumPy  
- **Frontend:** HTML, CSS, JavaScript  
- **Visualization:** Matplotlib  
- **Development Tools:** VS Code / PyCharm  


## 🧠 Model & Workflow

1. **Dataset Loading**
   - Medical images are loaded from the `dataset/` folder.
   - Images are preprocessed (resizing, normalization, noise removal).

2. **Preprocessing**
   - Images are converted to a suitable format for CNN input.
   - Data is split into training and testing sets.

3. **Model Training**
   - A Convolutional Neural Network (CNN) is used for feature extraction and classification.
   - The model is trained using the training dataset.

4. **Model Evaluation**
   - The trained model is evaluated using test images.
   - Performance is measured using accuracy, confusion matrix, and comparison charts.

5. **Prediction via Web App**
   - The trained model is integrated with a Flask web application.
   - Users can upload a medical image through the web interface.
   - The model predicts whether cancer is detected or not.

6. **Result Visualization**
   - Graphs and comparison charts are generated and stored in `experiment_results/`.


## 📊 Results & Outputs

- The model generates predictions on test images to identify the presence of pancreatic cancer.
- Experimental results are saved inside the `experiment_results/` folder.
- The following outputs are generated:
  - **Accuracy comparison charts**
  - **Confusion matrices** for different models
  - **Time comparison graphs**
  - **JSON files** containing prediction results and performance metrics
- A detailed experiment summary is available in:

