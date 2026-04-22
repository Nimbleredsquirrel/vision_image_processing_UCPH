# Vision and Image Processing — UCPH

Computer vision assignments from the University of Copenhagen.

## Assignments

### Assignment 2: Image Filtering and Edge Detection
Applies multi-scale Gaussian filtering, Sobel gradient computation, Laplacian of Gaussian, and Canny edge detection to a test image. Analyzes how scale parameter affects feature detection.

**Libraries:** `opencv-python`, `numpy`, `matplotlib`

### Assignment 3: Photometric Stereo
Reconstructs 3D surface geometry from multiple images taken under different illumination directions. Implements Woodham's method and RANSAC-based estimation, normal field smoothing via Riemannian geometry, and depth integration via Poisson solving. Tests robustness on both matte and specular objects.

**Libraries:** `numpy`, `ps_utils` (custom), `matplotlib`

### Assignment 4: Image Retrieval with Bag of Words
Builds a content-based image retrieval system on the Caltech-101 dataset. Extracts SIFT features, clusters them into a visual vocabulary (k=700, selected via 5-fold cross-validation), and ranks results using TF-IDF weighted histograms with cosine similarity. Achieves test MRR of 0.51 and 59% top-3 accuracy.

**Libraries:** `opencv-python`, `numpy`, `scikit-learn`, `matplotlib`

## Utility

- `ps_utils.py`: shared library for Assignment 3 with RANSAC, Poisson integration, normal field regularization, and 3D surface rendering
- `beethoven_run.py`: minimal standalone script demonstrating the photometric stereo pipeline on the Beethoven dataset

## Data

| File | Used in | Description |
|------|---------|-------------|
| `mandrill.jpg` | Assignment 2 | Test image for filtering |
| `Beethoven.mat` | Assignment 3 | Photometric stereo dataset (3 images, sculpture) |
| `mat_vase.mat` | Assignment 3 | Matte vase dataset (3 images) |
| `shiny_vase.mat` | Assignment 3 | Specular vase dataset (3 images) |
| `shiny_vase2.mat` | Assignment 3 | Specular vase dataset (22 images) |
| `Buddha.mat` | Assignment 3 | Buddha dataset (10 images) |
| `face.mat` | Assignment 3 | Face dataset (27 images) |
| `table.npz` | Assignment 4 | NumPy archive for retrieval task |

## Requirements

```
numpy
opencv-python
matplotlib
scikit-learn
scipy
```
