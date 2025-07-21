# U-Transformer for Underwater Image Restoration

This repository contains the implementation of a Vision Transformer (ViT)-based U-Transformer architecture for restoring degraded and biofouled underwater images. The model combines the global contextual power of ViT with a CNN-based decoder for high-fidelity image reconstruction.

---

##  Repository Contents

| File/Folder | Description |
|-------------|-------------|
| `UIR.ipynb` | Training notebook for underwater image restoration using paired clear and degraded images. |
| `Biofouling_restored.ipynb` | Inference notebook that processes a large dataset of biofouled underwater images and restores them using the trained U-Transformer. |
| `requirements.txt` | Python dependencies required to run the notebooks. |
| `README.md` | This documentation file. |
| `train_grid.png` | Grid of sample training images from the clear underwater dataset. |
| `test_grid.png` | Grid of test image examples showing restoration performance. |
| `biofouled_grid.png` | Representative samples from the biofouled image dataset. |
| `OriginalBiofouled_Restored.png` | Visual result of applying the model on real-world biofouled surfaces. |
| `Degraded_restored_GroundTruth.png` | Side-by-side comparison of degraded input, model output, and ground truth clear image. |

---

## Model Overview

- **Encoder:** `vit_base_patch8_224` from [TIMM](https://github.com/rwightman/pytorch-image-models)
- **Decoder:** Transposed convolutions with skip connections (U-Net-like design)

