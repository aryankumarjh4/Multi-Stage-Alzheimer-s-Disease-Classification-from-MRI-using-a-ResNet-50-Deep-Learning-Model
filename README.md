# Multi-Stage Alzheimer’s Disease Classification from MRI using a ResNet-50 Deep Learning Model

This is a deep learning project with the goal of detecting and classifying the stages of Alzheimer's disease from brain MRI scans. The project uses a ResNet50 model to automatically analyze MRI images and classify them into four categories: Non-Demented, Very Mild Demented, Mild Demented, and Moderate Demented.

### Project Description

Alzheimer's disease (AD) is a progressive neurodegenerative disorder, and early detection is crucial for timely intervention. Traditional diagnostic methods are often subjective and time-consuming, requiring expert interpretation of MRI scans. This project explores an AI-powered approach to address these challenges.

A deep learning model based on the **ResNet50 architecture** was implemented to automatically analyze MRI images. The model was developed using a well-structured pipeline that included data preprocessing, augmentation, stratified data splitting, and transfer learning.

### Technical Details

* **Model Architecture:** A pre-trained **ResNet50** model was fine-tuned for this multi-class classification task. This approach leverages the model's strong foundational understanding of visual features, which it gained from being trained on the large ImageNet dataset.
* **Dataset:** The "Best Alzheimer's MRI Dataset" from Kaggle was used. It contains over 6,200 MRI images, systematically grouped into four classes to reflect different stages of Alzheimer's disease.
* **Methodology:**
    * **Data Preprocessing:** Images were converted to RGB format, resized to 224x224 pixels, and normalized using ImageNet mean and standard deviation.
    * **Training:** The model was trained using the PyTorch framework with the Adam optimizer and a Cross-Entropy loss function. A learning rate scheduler was applied to refine the learning process.
    * **Evaluation:** The model's performance was rigorously evaluated on an unseen test set using a variety of metrics, including accuracy, precision, recall, F1-score, and AUC.
* **Results:**
    * The model achieved a high accuracy on the unseen test data.
    * Visual tools such as confusion matrices, ROC curves, and sample prediction displays further illustrated the model's effectiveness.

### Conclusion

This project demonstrates that deep learning, specifically a ResNet50 model, can be effectively applied to the problem of Alzheimer's disease detection and staging using MRI scans. While the results are encouraging, the project acknowledges the need for clinical validation on broader datasets before real-world deployment. The model is intended to serve as a supportive tool for clinicians, assisting in early and accurate diagnosis.

### Future Work

* Clinical validation on real-world datasets.
* Implementation of interpretability methods (e.g., Grad-CAM) to explain the model's decisions.
* Optimization for deployment on web or mobile interfaces.
* Integration with multi-modal data (e.g., genetic markers, cognitive test scores) for enhanced diagnostic accuracy.
