# Black and White to Colorized Image Conversion

This project implements an image colorization model inspired by the paper *Colorful Image Colorization* by Zhang et al., using TensorFlow.

---

## Model Overview

Like Zhang et al., we treat colorization as a classification problem, predicting discrete color classes instead of directly estimating color values per pixel. We preprocess images from RGB to LAB color space, which has a single grayscale lightness channel (L) and two color channels (A and B). We also quantize the whole AB space into 40 discrete color bins, allowing us to treat the task as a classification problem. For training, each pixel's color values are mapped to the nearest of these 40 "classes" and encoded as a one-hot vector. Our model is then trained using the below architecture and categorical cross-entropy loss to predict color classes for inputted grayscale images. 
  
---

## Results

Examples of colorized images generated by the model:  
![building_artifact](https://github.com/user-attachments/assets/a52e2587-58f1-4deb-b229-33aa44375119)

---

## Model  

Our Model Architecture:
<img width="921" alt="IMG_7999" src="https://github.com/user-attachments/assets/49df5919-9969-48b7-9f27-ca936f31f53b">

---

## References
*Zhang, R., Isola, P., & Efros, A. A. (2016). Colorful Image Colorization.*  
[Paper Link](https://arxiv.org/abs/1603.08511)

---

## Instructions for Use

1. Upload the files that you would like to train the model on.
2. Choose the amount of files to be trained.
3. Choose which images you would like modified.
4. Run the Jupyter Notebook provided.
