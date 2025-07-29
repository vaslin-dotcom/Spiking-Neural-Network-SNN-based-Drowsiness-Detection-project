# 🚗 Driver Drowsiness Detection System using CNN and SNN



---

## 📌 Overview

This project presents an **AI-powered Driver Drowsiness Detection System** designed to prevent road accidents caused by driver fatigue. It uses image-based deep learning techniques to detect the state of a driver's eyes (open or closed) and alerts when drowsiness is detected.

Two neural network architectures were developed and compared:
- **CNN (Convolutional Neural Networks)** for high accuracy
- **SNN (Spiking Neural Networks)** for low-power, real-time edge deployment

---

## 🎯 Objectives

- Classify driver’s eye state (open/closed) using camera feed
- Compare CNN and SNN based on accuracy, latency, FLOPs, and storage
- Achieve real-time processing on edge devices (e.g., Raspberry Pi)

---

## 🛠️ System Architecture

1. **Facial Detection**: Face landmarks extracted using Dlib (focus on eyes)
2. **Eye Region Extraction**: Cropped and resized to 24×24 grayscale images
3. **Model Inference**:
   - **CNN** for traditional inference
   - **SNN** (Rate & Temporal coding) for efficient, brain-inspired detection
4. **Drowsiness Logic**: Eye state history tracked over a window to detect prolonged closure
5. **Alert System**: Triggers buzzer or push notification (via Pushbullet)

---

## 🧠 Models Used

### 1. CNN Model
- Input: 64×64 grayscale images
- Layers: Conv → ReLU → Pool → Dense → Sigmoid
- Accuracy: **99.2%**
- Precision, Recall, F1-Score: **0.99**
- Latency: **137ms**
- Model Size: **1.78 MB**

### 2. SNN Models
- **Rate Coding**:
  - Accuracy: **94.3%**
  - Latency: **28ms**
  - Model Size: **827KB**
- **Temporal (Latency) Coding**:
  - Accuracy: **96.8%**
  - Latency: **41ms**
  - Model Size: **827KB**

---

## 📊 Evaluation Metrics

| Metric       | CNN      | SNN (Rate) | SNN (Temporal) |
|--------------|----------|------------|----------------|
| Accuracy     | 99.2%    | 94.3%      | 96.8%          |
| Precision    | 0.99     | 0.93       | 0.97           |
| Recall       | 0.99     | 0.93       | 0.97           |
| F1 Score     | 0.99     | 0.93       | 0.97           |
| FLOPs        | 12M      | 4M         | 4M             |
| Latency      | 137 ms   | 28 ms      | 41 ms          |
| Model Size   | 1.78 MB  | 827 KB     | 827 KB         |

---

## ⚙️ Tools and Libraries

- Python
- TensorFlow (for CNN)
- PyTorch + Norse (for SNN)
- OpenCV
- Dlib (Facial landmark detection)
- Pushbullet (for mobile alerts)

---

## 🔍 Key Takeaways

- **CNNs** offer superior accuracy but require higher computation and memory
- **SNNs** are suitable for **real-time low-power deployment** on edge devices
- Temporal coding in SNNs shows a great trade-off between performance and efficiency

---

## 🚀 Future Work

- Integrate with ADAS for enhanced road safety
- Expand dataset diversity (gender, ethnicity, lighting)
- Develop hybrid CNN-SNN models for better generalization
- Test deployment on neuromorphic chips (Intel Loihi, IBM TrueNorth)

---

## 📚 References

All core references are IEEE publications. Notable ones include:

- Fujiwara et al., *IEEE Trans. on Biomedical Engineering*, 2019  
- Jebraeily et al., *IEEE Access*, 2021  
- Venkateswarlu & Reddy, *DrowsyDetectNet*, *IEEE Access*, 2024  
- Others listed in the full documentation/report.

---

> 👨‍💻 Built with the mission to make roads safer using intelligent, real-time, and efficient AI systems.  
> 📬 Feel free to reach out for collaboration or full demo access.

