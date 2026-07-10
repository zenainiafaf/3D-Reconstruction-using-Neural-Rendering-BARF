# 3D Reconstruction using Bundle-Adjusting Neural Radiance Fields (BARF)

## Overview

This project presents the implementation and evaluation of **Bundle-Adjusting Neural Radiance Fields (BARF)** for 3D scene reconstruction and camera pose optimization.

The work investigates BARF on both a synthetic dataset (Blender Lego) and a real-world dataset reconstructed from smartphone images. The experiments include training, checkpoint evaluation, quantitative analysis, and comparison of different optimization strategies.

---

## Project Objectives

- Implement BARF for neural 3D reconstruction.
- Optimize camera poses jointly with scene representation.
- Evaluate reconstruction quality on synthetic and real datasets.
- Analyze training convergence and model stability.
- Compare different training configurations.

---

## Datasets

### Blender Synthetic Dataset (Lego)

- 100 training images
- 200 testing images
- Ground-truth camera poses
- Artificial pose perturbation for BARF evaluation

### Real Dataset

- 93 smartphone images
- Camera poses estimated with COLMAP
- Real-world indoor scene
- Training, validation, and testing split

---

## Repository Structure

```
Vision_Project/
│
├── notebooks/
│   ├── vision_data_public_training_evaluation.ipynb
│   ├── vision_data_reel_training.ipynb
│   └── vision_data_reel_evaluation.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Experiments

### Experiment 1 – Blender Lego

- BARF training
- Checkpoint evaluation
- Camera pose optimization
- PSNR, SSIM and LPIPS analysis
- Detection of catastrophic collapse after 20k iterations

### Experiment 2 – Optimized Training

Comparison of optimized hyperparameters to improve training stability.

### Experiment 3 – Real Dataset

Training and evaluation using a real dataset reconstructed from smartphone images.

---

## Results

### Blender Lego

| Metric | Best Value |
|---------|-----------:|
| PSNR | 21.81 dB |
| SSIM | 0.800 |
| LPIPS | 0.230 |
| Best Checkpoint | 20,000 iterations |

### Real Dataset

| Metric | Best Value |
|---------|-----------:|
| PSNR | 24.78 dB |
| SSIM | 0.990 |
| Best Checkpoint | 36,000 iterations |

---

## Evaluation

The implementation evaluates each checkpoint using:

- PSNR
- SSIM
- LPIPS
- Rotation Error
- Translation Error

The project also analyzes the convergence behavior and the catastrophic collapse phenomenon observed during long training on the synthetic dataset.

---

## Technologies

- Python
- PyTorch
- BARF
- COLMAP
- Jupyter Notebook
- NumPy
- OpenCV
- Matplotlib

---

## Kaggle Resources

Due to GitHub storage limitations, the following resources are available on Kaggle:

- Pretrained checkpoints
- Complete evaluation outputs
- Reconstruction videos
- Camera poses
- Quantitative evaluation files

**Kaggle Dataset**

```
https://www.kaggle.com/datasets/your-username/vision-project-data
```

---

## References

- NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis (ECCV 2020)
- BARF: Bundle-Adjusting Neural Radiance Fields (ICCV 2021)

---

## Author

**Afaf Farah Zenaini**

Master's Student in Information Systems Engineering