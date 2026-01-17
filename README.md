# Motion Transfer: Animating Still Images from Video

**Georgia Tech CS8803LS - Machine Learning with Limited Supervision**

A generative deep learning model that transfers motion from a driving video to a static source image, creating realistic animations of the source subject performing the motions in the video.

![Framework](Framework.png)

## Project Overview

Given:
- A **source image** (e.g., a photo of a person)
- A **driving video** (e.g., someone talking or moving)

The model generates a video where the person in the source image performs the motions from the driving video.

### Applications
- Video conferencing avatars
- Digital content creation
- Animation from single images
- Face reenactment

## Architecture

The model consists of:
1. **Motion Estimation Module** - Extracts motion representations from the driving video
2. **Generation Module** - Synthesizes the output video by applying extracted motion to the source image
3. **Reconstruction Loss** - Ensures visual fidelity to the source appearance

## Project Structure

```
├── train.py              # Training script
├── demo.py               # Run inference on new images/videos
├── transfer.py           # Motion transfer pipeline
├── motion.py             # Motion extraction module
├── prediction.py         # Prediction utilities
├── reconstruction.py     # Image reconstruction
├── augmentation.py       # Data augmentation
├── frames_dataset.py     # Dataset loader
├── modules/              # Neural network modules
├── config/               # Model configurations
├── data/                 # Training data
└── requirements.txt      # Dependencies
```

## Usage

### Training
```bash
python train.py --config config/your_config.yaml
```

### Demo
```bash
python demo.py --source path/to/image.png --driving path/to/video.mp4
```

## Tech Stack

- Python
- PyTorch
- OpenCV
- NumPy

## References

Based on advances in:
- First Order Motion Model for Image Animation
- Generative Adversarial Networks
- Keypoint-based motion estimation

## Course

CS8803LS: Machine Learning with Limited Supervision
Georgia Institute of Technology

---

**Keywords**: Generative Models, Motion Transfer, Computer Vision, Deep Learning, GANs, Video Synthesis
