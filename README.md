# Dual-Stream-Emotion-Detection-with-YOLOv10
🌐 Interactive Dashboard (Figma):
https://cloth-violet-19391596.figma.site

Overview

This project presents a robust, explainable, and calibrated Facial Expression Recognition (FER) framework built on YOLOv10. It integrates a dual-stream preprocessing pipeline, interpretability tools, and confidence calibration to ensure stability under real-world visual degradations such as occlusion, blur, and noise.

Key Features

Dual-Stream Input Pipeline

Clean Stream: flip, color jitter, scaling

Perturbation Stream: occlusion, blur, noise → denoise

YOLOv10 FER Model

Precision 0.90, Recall 0.89, mAP@50 0.93, mAP@50–95 0.77

Outperforms YOLOv8 and Faster R-CNN on a balanced AffectNet subset

Interpretability

RISE, SHAP-CAM, Sliding Patch Occlusion

Saliency Divergence (KL, SymKL, JS)

Calibration & Reliability

Temperature Scaling

ECE, MCE, Brier Score, NLL, Risk–Coverage curves

Architecture (Text Diagram)
Input Images → Dual-Stream Augmentation
     |               |
     |               +→ Perturbation Stream (occlusion/blur/noise)
     |               
     +→ Clean Stream
          |
          v
   YOLOv10 Training (Clean & Corrupted)
          |
          v
   Evaluation → Robustness → Interpretability → Calibration
          |
          v
     Final FER Output

Live Prototype

The full dashboard—including architecture, metrics, robustness tests, saliency maps, and calibration plots—is available in Figma.

👉 https://cloth-violet-19391596.figma.site

Citation

If you use this work, please cite:

Robust and Explainable Facial Expression Recognition Using YOLOv10 under Real-World Visual Degradations (2025).

License

This project is licensed under the MIT License — see the LICENSE file for details.

Author Gazi Jahin CSE Graduate | Bangladesh.
