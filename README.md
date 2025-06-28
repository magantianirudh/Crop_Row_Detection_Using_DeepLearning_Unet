🌱 Crop Row Segmentation Using a Lightweight UNet-Based Architecture

This project focuses on building an efficient deep learning model for crop row segmentation using a tailored version of U-Net enhanced with lightweight modules. The objective is to enable real-time row detection in agricultural fields, especially under resource constraints such as edge devices and drones.

📌 Problem Statement

 Precision agriculture relies on identifying crop rows accurately to:
 Guide autonomous tractors and drones
 Optimize targeted spraying and irrigation
 Analyze plant health and yield patterns
 Improve resource utilization across large farms

Manual methods are slow, error-prone, and infeasible at scale — hence the need for an automated solution.

🚀 Model Overview

 We designed a compact U-Net variant that integrates:
 Fire Modules (adapted from SqueezeNet) for reducing parameters and computational overhead
 Transposed Fire Blocks for effective upsampling in the decoder
 Skip Connections for retaining spatial precision
 Binary Segmentation Output: 1 = crop row, 0 = background
 This architecture balances performance with efficiency, making it suitable for real-time inference on drones and embedded systems.

🛠️ Tools & Technologies

 Python
 TensorFlow / Keras
 OpenCV, NumPy for preprocessing
 IoU, Dice Coefficient for evaluation
 Data Augmentation (flip, rotation, noise) to improve robustness

📊 Results

Achieved accurate row segmentation under various field conditions including:
 Uneven lighting
 Partial occlusion
 Gaps and overlaps in planting

Model generalizes well to unseen field images and multiple crop types
Lightweight footprint suitable for deployment on devices like NVIDIA Jetson or Raspberry Pi

--> Sample Output

Below is an example of model prediction:

  Original image of a crop field

![image](https://github.com/user-attachments/assets/d4425904-370c-47d7-8a6b-791ae4f86c68)


  Predicted binary segmentation map with crop rows highlighted

![image](https://github.com/user-attachments/assets/b5da65b6-df6c-4215-9b22-746041cfee5d)


⚙️ What's Next

Integrating this model with navigation systems for autonomous robots
Extending it to multiclass segmentation (e.g., weeds vs. crops)
Experimenting with pruning and quantization for further optimization
