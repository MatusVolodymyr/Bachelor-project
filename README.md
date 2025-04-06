# Drivable Area Segmentation using DeepLabV3+

This project presents a semantic segmentation model designed to identify drivable zones in road images using the **DeepLabV3+** architecture with various CNN backbones. Developed as part of a Bachelor’s thesis at **Taras Shevchenko National University of Kyiv**, this work was also showcased at the [university research conference (page 202)](https://ir.library.knu.ua/entities/publication/536acc65-001e-476b-ad3e-4658ac0614d4).

## Project Overview

The goal of this project is to improve the accuracy of **semantic segmentation** for autonomous driving applications by identifying road areas that are safe for vehicle navigation.

### Key Features:
- Uses **DeepLabV3+** with backbones like:
  - YOLOv8_m
  - EfficientNetV2_s
  - MobileNet_v3
- Trained and evaluated on the **BDD100K** dataset
- Achieved almost state-of-the-art results:
  - **EfficientNetV2_s:** 92.69% IoU
  - **YOLOv8_m:** 92.59% IoU
  - **MobileNet_v3:** 91.26% IoU

These results outperform benchmark models like **YOLOP (91.5%)** and **HybridNets (90.5%)**.

## Methodology

- **Architecture**: DeepLabV3+ with transfer learning
- **Libraries**: TensorFlow, KerasCV
- **Training Details**:
  - Input size: 640x384
  - Optimizer: AdamW
  - Loss function: Categorical Cross-Entropy
  - Batch size: 12
  - Data augmentation applied for generalization

## Dataset

- **BDD100K**: A large-scale driving dataset containing 100,000 images labeled for tasks like semantic segmentation across various conditions (urban/highway, day/night, weather changes).

## Results

Models were evaluated based on **Intersection over Union (IoU)**. EfficientNetV2_s and YOLOv8_m backbones achieved the highest accuracy while maintaining computational efficiency for real-time application potential.

## Future Work

- Explore newer or hybrid CNN/Transformer backbones
- Optimize inference speed for deployment on edge devices
- Extend to multi-class segmentation or panoptic perception

## Authors

**Volodymyr Matus**, **Andriy Konovalov** 
Bachelor’s Thesis @ Taras Shevchenko National University of Kyiv  
Faculty of Radiophysics, Electronics and Computer Systems  
