# Bearing Fault Detection Using Machine Learning

This project leverages **Convolutional Neural Networks (CNNs)** to classify the condition of bearings based on vibration data. The model predicts one of three classes:
- **Normal**
- **Inner Race Fault**
- **Outer Race Fault**

## Dataset
The dataset consists of vibration features extracted from bearings, including:
- **Basic Statistics**: Max, Min, Mean, RMS
- **Distribution Measures**: Skewness, Kurtosis
- **Fault Indicators**: Crest Factor, Form Factor

### Data Structure
The data is split into:
- **Training Set**: 80% of the dataset.
- **Testing Set**: 20% of the dataset.

---

## Project Workflow
1. **Data Preprocessing**:
   - Combined datasets for all bearing conditions.
   - Normalized features to ensure consistent scale.
   - Split data into training and testing sets with stratification.

2. **Model Building**:
   - Built a CNN model with:
     - Conv1D layers for pattern extraction.
     - MaxPooling layers for dimensionality reduction.
     - Dense layers for classification.
   - Used dropout to prevent overfitting.

3. **Training**:
   - Trained the model over 20 epochs.
   - Used the Adam optimizer and sparse categorical crossentropy loss.

4. **Evaluation**:
   - Achieved ~96.9% test accuracy.
   - Confusion matrix and classification report showed strong performance across all classes.

---

## Results
- **Test Accuracy**: ~96.9%
- **Class Performance**:
  - High precision, recall, and F1-scores across all classes.
- **Confusion Matrix**:
  - Minimal misclassifications, with most predictions correct.

---

## How to Run the Project

### Clone the Repository
```bash
git clone https://github.com/yourusername/bearing-fault-detection.git
cd bearing-fault-detection
