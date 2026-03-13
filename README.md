🫁 Lung Cancer Classification via VGG16 Transfer Learning Final Accuracy: 95.7% | Malignant Sensitivity: 99% This repository contains a Deep Learning pipeline for the automated classification of lung CT scans into three categories: Benign, Malignant, and Normal. The project focuses on scientific integrity, specifically addressing the common pitfall of "Data Leakage" in medical datasets to ensure real-world clinical reliability.

🔬 Project Overview The primary goal was to move beyond simple "black-box" models and develop a high-precision diagnostic tool.

The "Data Leakage" Discovery During initial development, the model achieved a suspicious 100% accuracy. Upon manual audit, 43 duplicate images were identified across the training and validation sets. This project explicitly documents the removal of these duplicates, resulting in a 95.7% accuracy that is scientifically valid and generalizes to new patient data.

🛠️ Technical Stack Language: Python 3.x

Deep Learning: TensorFlow / Keras

Architecture: VGG16 (Transfer Learning)

Visualization: Matplotlib, Seaborn

Dataset: IQ-OTH/NCCD Lung Cancer Dataset

📈 Model Evolution & Performance

Baseline vs. Specialist Initial Custom CNN: Struggled with complex textures, achieving only ~45% accuracy after data cleaning.
VGG16 Transfer Learning: Utilized pre-trained weights from ImageNet, allowing the model to identify subtle pulmonary nodules immediately.

Training Results The model stabilized rapidly, with the training and validation curves converging by Epoch 8, indicating no significant overfitting.

Clinical Reliability (Confusion Matrix) The most critical metric in medical AI is Sensitivity (not missing a positive case).

Malignant Cases: 101 / 102 Correctly Identified.

False Negatives: < 1%

🚀 Future Scope Explainable AI (XAI): Integrating Grad-CAM heatmaps to highlight the specific regions of interest (tumors) for radiologists.

Deployment: Developing a Flask/FastAPI wrapper to allow for real-time scan uploads in a clinical setting.

📄 How to Use Clone the repository.

Ensure the IQ-OTH/NCCD dataset is structured into Benign, Malignant, and Normal folders.
Here's the dataset link: https://www.kaggle.com/datasets/hamdallak/the-iqothnccd-lung-cancer-dataset

Run the Jupyter Notebook to train the model or load the provided .h5 specialist file.

