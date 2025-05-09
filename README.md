Plant-disease-detection-system-for-sustainable-agriculture

1. Problem Statement -
Agriculture is a cornerstone of many economies, but crop diseases significantly reduce yield and quality, affecting both farmers' income and food security. Traditionally, disease detection has relied on manual inspection, which is often slow, error-prone, and inaccessible in remote regions.
Week - 1 
To address this, we aim to develop a Plant Disease Detection System that leverages machine learning and computer vision techniques. This system will help in early and accurate identification of plant diseases, enabling farmers to take timely preventive or corrective actions. The objective is to create a scalable and user-friendly tool that supports sustainable agriculture by minimizing crop loss and optimizing pesticide usage.
2. Pipeline (as discussed in the lecture)
•	Data Collection:
   - Gathering a diverse dataset of plant leaf images (healthy and diseased) from open-source repositories like PlantVillage.
•	Data Preprocessing:
   - Image resizing, normalization, noise removal, and data augmentation to improve model generalization.
•	Model Selection & Training:
   - Using Convolutional Neural Networks (CNNs) or pre-trained models like ResNet or MobileNet for image classification.
•	Model Evaluation:
   - Performance metrics: accuracy, precision, recall, and F1-score using validation/test datasets.
•	Deployment:
   - Creating a web or mobile application where users can upload plant images and get real-time disease diagnosis.
•	Continuous Improvement:
   - Incorporating user feedback and continuously updating the model with new disease data.
Week - 2
 Summary of Improvisations in our CNN Model
Increased Depth and Complexity

Added four convolutional layers with progressively increasing filters: 32 → 64 → 128 → 256.

This helps the model capture features at multiple levels of abstraction, improving its ability to distinguish complex patterns.

Use of Larger Kernel Sizes Initially

Used a 7×7 kernel in the first Conv layer and a 5×5 kernel in the second.

Larger kernels at early stages help capture broader features; smaller kernels (3×3) in deeper layers fine-tune details.

Multiple Pooling Layers

Strategically placed MaxPooling layers after some Conv layers to reduce spatial dimensions and computational load.

Two Fully Connected (Dense) Layers

Introduced Dense layers (128 and 64 units) before the output, enabling complex feature interaction before classification.

Dropout Regularization (partially implemented)

Added Dropout(0.5) layers after Dense layers (though not applied correctly initially).

Helps prevent overfitting by randomly disabling neurons during training.

Softmax Output for Multi-Class Classification

Correctly used Dense(38, activation='softmax') for 38-class classification.

