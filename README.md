# 🖼️ **Image Transformation Toolkit with PyTorch** 🛠️  
*Advanced Image Processing and Visualization using PyTorch and TorchVision*

---

## 🚀 **Project Overview**  
This project demonstrates **advanced image transformations** using PyTorch and TorchVision. It includes a Jupyter Notebook (`Ornella_Gigante_Lab4_Sprint2.ipynb`) that applies various photometric and geometric adjustments to images, such as brightness, contrast, gamma correction, and hue/saturation shifts. The toolkit also visualizes the effects of these transformations, enabling users to compare original and modified images side-by-side.

**Key Use Cases**:  
- Data augmentation for deep learning models.  
- Image preprocessing for computer vision tasks.  
- Educational tool for understanding transformation effects.  

---

## 🌟 **Core Features**  
| Transformation          | Description                                                                 | Example Use Case                 |  
|--------------------------|-----------------------------------------------------------------------------|-----------------------------------|  
| **Brightness Adjustment**| Modifies image illumination (`adjust_brightness`).                          | Simulate low-light conditions.    |  
| **Contrast Enhancement** | Adjusts difference between light and dark areas (`adjust_contrast`).        | Improve feature visibility.       |  
| **Gamma Correction** 🌓  | Non-linear adjustment for perceptual brightness (`adjust_gamma`).          | Correct underexposed images.     |  
| **Hue/Saturation** 🎨    | Alters color tones and intensity (`adjust_hue`, `adjust_saturation`).       | Artistic style transfer.          |  
| **Sharpness Optimization** 🔍 | Enhances edge clarity (`adjust_sharpness`).                          | Improve OCR readability.          |  
| **Visual Comparison**    | Side-by-side display of original vs. transformed images.                    | Quality assessment.               |  

---

## 🛠️ **Tech Stack**  
- **PyTorch**: Tensor operations and GPU acceleration.  
- **TorchVision**: Prebuilt transformations and image utilities.  
- **PIL/Pillow**: Image loading and preprocessing.  
- **Matplotlib**: Visualization of results.  
- **Jupyter Notebook**: Interactive experimentation.  

---

## 📥 **Installation**  
1. **Clone Repository**:  
   ```bash  
   git clone https://github.com/yourusername/image-transformation-toolkit.git  
   cd image-transformation-toolkit  
   ```

2. **Install Dependencies**:  
   ```bash  
   pip install torch torchvision pillow matplotlib  
   ```

3. **Launch Jupyter Notebook**:  
   ```bash  
   jupyter notebook Ornella_Gigante_Lab4_Sprint2.ipynb  
   ```

---

## 🖌️ **Code Examples**  
### **1. Image Loading & Tensor Conversion**  
```python  
from PIL import Image  
from torchvision.transforms import functional as F  

img = Image.open('path/to/image.jpg')  
img_tensor = F.to_tensor(img)  # Convert to PyTorch tensor  
```

### **2. Applying Transformations**  
```python  
# Adjust brightness (50% reduction)  
brightness_adjusted = F.adjust_brightness(img_tensor, brightness_factor=0.5)  

# Increase contrast by 150%  
contrast_enhanced = F.adjust_contrast(img_tensor, contrast_factor=1.5)  
```

### **3. Visualization**  
```python  
import matplotlib.pyplot as plt  

fig, axes = plt.subplots(1, 2, figsize=(12, 6))  
axes[0].imshow(F.to_pil_image(img_tensor))  
axes[0].set_title("Original Image")  
axes[1].imshow(F.to_pil_image(brightness_adjusted))  
axes[1].set_title("Brightness Adjusted")  
plt.show()  
```

---

## 📊 **Transformation Matrix**  
| Parameter             | Typical Range | Effect Visualization |  
|-----------------------|---------------|-----------------------|  
| `brightness_factor`   | 0.0 (black) to 1.0+ | Brightness |  
| `contrast_factor`     | 0.0 (gray) to 1.0+ | Contrast |  
| `hue_factor`          | -0.5 to 0.5    | Hue |  

---

## 📜 **License**  
MIT License 

---

👩💻 **Author**: Ornella Gigante  

🔗 **GitHub**: [@yourusername](https://github.com/yourusername)  

*"Transform images like a pro with PyTorch's powerful vision toolkit!"* 🚀  

