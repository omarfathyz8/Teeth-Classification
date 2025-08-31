# 🦷 Teeth Classification Project

This project aims to classify dental images into **7 classes** using deep learning.  
The dataset is organized into **Training**, **Validation**, and **Testing** folders, each containing one subfolder per class.  

---

## 📂 Steps Completed

### 1. Dataset Setup
- Uploaded `TeethDataset.zip` to Google Drive.  
- Mounted Google Drive in Colab.  
- Extracted dataset into `Training`, `Validation`, and `Testing` directories.  
- Cleaned test directory by removing unwanted files/folders.  

### 2. Dataset Preparation in TensorFlow
- Loaded train, validation, and test sets with `image_dataset_from_directory`.  
- Configured image size `(256, 256)` and batch size.  

### 3. Data Preprocessing
- Applied normalization (scaled pixel values to `[0,1]`).  
- Defined augmentation pipeline (horizontal flips, rotation, zoom).  
- Applied augmentation only on the training set.  

### 4. Class Distribution
- Counted the number of images in each class for train, validation, and test splits.  
- Visualized distribution with bar plots to check dataset balance.  

### 5. Augmentation Visualization
- Compared original vs augmented images side by side to verify transformations.  

---

## ⏭️ Next Steps
- Build a CNN model architecture (TensorFlow/Keras).  
- Train the model using the preprocessed dataset.  
- Evaluate on validation and test sets.  
- Optimize with different architectures and hyperparameters.  
- Document performance metrics and results.  
