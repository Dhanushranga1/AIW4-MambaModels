# AIW4-MambaModels
# Week 4: Mamba Model for Image Segmentation

## Objective
Adapt and train a Mamba (state space model) for image segmentation tasks. This includes:
- Understanding state space modeling and the Mamba architecture.
- Applying it to segmentation and comparing with traditional models like UNet.

## Progress So Far

- Implemented a basic Mamba-style architecture (`CobraBlock` and `Cobra`).
- Tested with dummy token inputs to verify model flow and tensor dimensions.
- Verified the forward pass and model structure using `torchinfo.summary`.

## Learning Resources

### Books
- Hands-On LLMs by Maarten Grootendorst

### Videos
- [Intuition Behind Mamba and State Space Models](https://www.youtube.com/watch?v=BDTVVlUU1Ck)
- [Mamba and S4 Explained: Architecture, Parallel Scan, Kernel Fusion, Recurrent, Convolution, Math (Umar Jamil)](https://www.youtube.com/watch?v=8Q_tqwpTpVU&t=2976s)

## Next Steps

- Adapt the model to accept image data (patch-based or pixel-wise).
- Train on a segmentation dataset (e.g., medical images or Pascal VOC).
- Visualize outputs and compute metrics like Dice coefficient and IoU.
- Compare results against UNet (from Week 1).
