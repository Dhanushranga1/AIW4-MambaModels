# AIW4-MambaModels

## Week 4: Mamba Model for Image Segmentation

### Objective

Adapt and train a Mamba (state space model) for image segmentation tasks. This includes:
- Understanding state space modeling and the Mamba architecture.
- Applying it to segmentation and comparing with traditional models like UNet.

---

## Progress So Far

- Implemented a Mamba-based image segmentation model using patch-based embeddings and deep Mamba encoder blocks.
- Successfully trained the model on brain tumor MRI segmentation data.
- Evaluated using Dice Coefficient and IoU metrics.
- Compared with traditional UNet implementation from Week 1.

---

## Performance Comparison

| Metric         | UNet (TensorFlow)     | MambaUNet (PyTorch)   |
|----------------|------------------------|------------------------|
| Dice Score     | 0.7409                 | **0.8470**             |
| IoU Score      | 0.7097                 | **0.7422**             |
| Total Params   | **7,708,609**          | **473,953**            |
| Model Size     | ~29.41 MB              | ~1.81 MB               |
| Framework      | TensorFlow             | PyTorch                |
| Core Design    | Conv-Deconv + Skip     | Patch + Mamba          |

---

## Key Differences (Explained)

1. **Architecture Type**:
   - UNet uses a traditional encoder-decoder setup with CNNs.
   - MambaUNet replaces most of the CNNs with a newer state-space model (Mamba) that works more efficiently on sequences.

3. **Parameter Efficiency**:
   - UNet has over 7 million parameters, making it heavy on memory.
   - MambaUNet achieves higher accuracy with **~16x fewer parameters**, proving the efficiency of SSMs.

4. **Feature Learning**:
   - UNet is good at capturing small image details.
   - MambaUNet is better at understanding overall patterns across the whole image.

---

## Learning Resources

### Books
- *Hands-On Large Language Models* by Maarten Grootendorst

### Videos
- [Intuition Behind Mamba and State Space Models](https://www.youtube.com/watch?v=BDTVVlUU1Ck)
- [Mamba and S4 Explained (Umar Jamil)](https://www.youtube.com/watch?v=8Q_tqwpTpVU)

---

## References

1. Efficient Brain Tumor Segmentation with Mamba  [paper](https://ieeexplore.ieee.org/document/10748085)

2. State Space Models: Mamba  
   - [Mamba: Linear-Time Sequence Modeling with Selective State Spaces](https://arxiv.org/abs/2312.00752)  


3. Beyond Attention: Mamba in Vision  
   - [Vision Models with Mamba](https://arxiv.org/abs/2410.21872)  

---
