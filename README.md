# 🌱 Crop Row Segmentation Using a Lightweight UNet-Based Architecture

This project focuses on building an efficient deep learning model for **crop row segmentation** using a tailored version of U-Net enhanced with lightweight modules. The objective is to enable real-time row detection in agricultural fields, especially under resource constraints such as edge devices and drones.

---

## 📌 Problem Statement

Precision agriculture relies on identifying crop rows accurately to:

- Guide autonomous tractors and drones  
- Optimize targeted spraying and irrigation  
- Analyze plant health and yield patterns  
- Improve resource utilization across large farms  

Manual methods are slow, error-prone, and infeasible at scale — hence the need for an automated solution.

---

## 🚀 Model Overview

We designed a **compact U-Net variant** that integrates:

- 🔥 **Fire Modules** (adapted from SqueezeNet) for reducing parameters and computational overhead  
- 🔄 **Transposed Fire Blocks** for effective upsampling in the decoder  
- 🔗 **Skip Connections** for retaining spatial precision  
- 🧠 **Binary Segmentation Output**: 1 = crop row, 0 = background  

This architecture balances performance with efficiency, making it suitable for **real-time inference on drones and embedded systems**.

---

## 🛠️ Tools & Technologies

- **Python**
- **TensorFlow / Keras**
- **OpenCV, NumPy** for preprocessing
- **IoU, Dice Coefficient** for evaluation
- **Data Augmentation** (flip, rotation, noise) to improve robustness

---

## 📊 Results

- Achieved **accurate row segmentation** under various field conditions including:
  - Uneven lighting
  - Partial occlusion
  - Gaps and overlaps in planting
- Model generalizes well to unseen field images and multiple crop types
- Lightweight footprint suitable for deployment on devices like NVIDIA Jetson or Raspberry Pi

---

## 📷 Sample Output

Below is an example of model prediction:

- **Left**: Original image of a crop field  
- **Right**: Predicted binary segmentation map with crop rows highlighted

- ![image](https://github.com/user-attachments/assets/b2ea43ff-3076-41e4-9b65-e739fb160333)

---

## ⚙️ What's Next

- Integrating this model with navigation systems for autonomous robots  
- Extending it to multiclass segmentation (e.g., weeds vs. crops)  
- Experimenting with pruning and quantization for further optimization
