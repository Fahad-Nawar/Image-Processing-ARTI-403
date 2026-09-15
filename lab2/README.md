# Lab 2 — Digital Image Fundamentals

**Course:** ARTI 403 – Image Processing  
**Outcome:** Explain how digital images are represented and manipulated in a computer.

---

## Overview

This lab explores the fundamental concepts of digital image representation, covering sampling and quantization, arithmetic operations, and set/logical operations on grayscale images.

---

## Topics Covered

### 1. Image Sampling and Quantization
- **Sampling:** Downsampling an image by a given factor using nearest-neighbor interpolation (`cv2.resize`).
- **Quantization:** Reducing the number of grayscale intensity levels to observe banding effects.
- Visualization of original, sampled, and quantized images side by side.

### 2. Arithmetic Operations
- **Image Addition:** Adding two grayscale images pixel-by-pixel.
- **Image Subtraction:** Subtracting one image from another with clipping to [0, 255].
- **Scalar Addition:** Adding a constant value (175) to brighten an image.

### 3. Sets and Logical Operations
- **Union (A | B):** Pixels present in either image A or B.
- **Intersection (A AND B):** Pixels present in both A and B.
- **Set Difference (A - B):** `A AND (NOT B)` — pixels in A but not in B.
- **Symmetric Difference (A XOR B):** Pixels in A or B but not both.

---

## Tasks

### Task 1 — Effect of Sampling and Quantization Parameters
Experimenting with different sampling factors (`2, 4, 8, 16`) and quantization levels (`128, 64, 16, 4, 2`) to observe how resolution and intensity depth affect image quality.

### Task 2 — Arithmetic and Logical Operations on Two Images
| Sub-task | Operation | Description |
|----------|-----------|-------------|
| 2.1 | Subtraction | `I1 - I2` with clipping |
| 2.2 | Scalar addition | `I1 + 175` (brightness increase) |
| 2.3 | Set Difference | `A AND (NOT B)` |
| 2.4 | Symmetric Difference | `A XOR B` |
| 2.5 | Intersection | `A AND B` |

---

## Images Used

| File | Description |
|------|-------------|
| `lena_gray_256.tif` | Standard grayscale test image (256×256) |
| `cameraman.tif` | Classic grayscale benchmark image |
| `A.png` | Binary/grayscale image A for set operations |
| `B.png` | Binary/grayscale image B for set operations |

> Images are located in the shared `../images/` directory.

---

## Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
from PIL import Image
```

---

## How to Run

1. Open `Lab2_Fahad.ipynb` in Jupyter Notebook or JupyterLab.
2. Make sure the `../images/` directory contains the required image files.
3. Run all cells in order.

---

## Author

**Fahad** — ARTI 403, Image Processing Lab
