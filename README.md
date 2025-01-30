# RailGuard
Enhanced Railway Track Fault Detection Using Hybrid Deep Learning Approach with CNN and Transfer Learning
# RailGuard: Railway Track Fault Detection 🚆🔍

## 📌 Overview
RailGuard is a deep learning-based railway track fault detection system. It utilizes **CNNs** and **Transfer Learning** (InceptionV3) to classify various track defects, ensuring **efficient and automated railway maintenance**. This model significantly reduces manual inspection time while enhancing detection accuracy.

## 🚀 Features
- **Automated Fault Detection**: Identifies track defects like cracks, flakes, grooves, joints, etc.
- **Deep Learning-Based**: Uses **CNN + Transfer Learning (InceptionV3)** for high precision.
- **Optimized Performance**: Fine-tuned with **custom layers** for accurate classification.
- **Robust Evaluation**: Validated using **confusion matrix, precision, recall, F1-score**.

## 🔬 Methodology
1. **Dataset Preparation**:
   - Convert images to **grayscale**, apply **ROI cropping, denoising, thresholding**.
   - Split into **80% train, 16% validation, 4% test**.
   - Resize images to **(224, 224)**.
   - Augment training set (random flips, rotations, zoom).

2. **Model Construction**:
   - Load **pretrained InceptionV3** (without top layers).
   - Add **GlobalAveragePooling2D, Dense(1024, ReLU), Dropout(0.5), and Softmax Output Layer**.
   - Compile with **Adam optimizer** and **Categorical Crossentropy loss**.

3. **Training & Evaluation**:
   - Train model using **`model.fit()`** with early stopping.
   - Evaluate using **accuracy, precision, recall, F1-score**.
   - Visualize performance using **accuracy vs. epochs, loss vs. epochs graphs**.

## 📊 Results
- **Final Accuracy**: **94%**
- **Precision**: **97%**, **Recall**: **96%**, **F1-Score**: **98%**
- **Well-Generalized**: No overfitting, consistent validation loss.

## 🛠 Installation
```bash
git clone https://github.com/yourusername/RailGuard.git
cd RailGuard
pip install -r requirements.txt
```
##🏃 Usage
python train.py  # Train the model
python test.py   # Run inference on test images

##📝 Dataset
The dataset contains labeled railway track defect images.
Categories: Cracks, Flakes, Grooves, Joints, Shellings, Spallings, Squats.
Preprocessed & Augmented before training.

##💡 Contributing
Feel free to fork this repo and contribute via pull requests. Any improvements or suggestions are welcome!
