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

### 6. Baseline CNN Model
- Built a simple CNN with:
  - 4 convolutional layers (`32 → 64 → 128 → 256` filters).  
  - Max pooling after each conv layer.  
  - Flatten + Dense(256) + Dropout(0.3).  
  - Output layer with 7 units (softmax).  
- Compiled with **Adam optimizer** and **sparse categorical crossentropy loss**.  
- Trained with early stopping and checkpointing on 20 epochs.  
- Achieved:
  - **Train Accuracy ~88%**  
  - **Validation Accuracy ~85%**  
  - **Test Accuracy ~86%**  

---

## ⏭️ Next Steps
- Move to **Transfer Learning** (EfficientNet, ResNet, MobileNet) for higher accuracy.  
- Evaluate with confusion matrix and classification report.  
- Optimize hyperparameters further.
