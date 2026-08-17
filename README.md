# 🌙 Lunar – PSR Image Enhancer

Lunar is a desktop-based **PSR image enhancement application** built with Python and PyQt5. It provides an interactive interface for loading PSR images and improving their visual quality using a multi-stage image enhancement pipeline.

## ✨ Features

* 🖼️ Load PNG, JPG, and BMP images
* 🔇 Noise reduction using Non-Local Means Denoising
* 🎨 Contrast enhancement using CLAHE
* ☀️ Adjustable gamma correction
* 🔍 Adjustable image sharpening
* 🎚️ Interactive Gamma and Sharpen controls
* 🖥️ PyQt5-based desktop graphical user interface
* 📊 Real-time display of the enhanced image
* 💾 Image enhancement using OpenCV and NumPy

## 🛠️ Technologies Used

* **Python**
* **PyQt5** – Desktop GUI
* **OpenCV** – Image processing
* **NumPy** – Numerical operations
* **scikit-image** – Image processing utilities

## 🔬 Image Enhancement Pipeline

Lunar applies multiple image-processing techniques sequentially:

```text
Input PSR Image
      ↓
Grayscale Conversion
      ↓
Noise Reduction
      ↓
CLAHE Contrast Enhancement
      ↓
Gamma Correction
      ↓
Image Sharpening
      ↓
Sharpened + Gamma Corrected Image Blending
      ↓
Final CLAHE Enhancement
      ↓
Enhanced PSR Image
```

### 1. Noise Reduction

OpenCV's `fastNlMeansDenoising()` is used to reduce noise while preserving image details.

### 2. Contrast Enhancement

CLAHE (Contrast Limited Adaptive Histogram Equalization) is applied to improve local contrast.

### 3. Gamma Correction

Gamma can be adjusted interactively through the GUI.

The available range is:

```text
0.50 – 2.00
```

The default value is:

```text
1.20
```

### 4. Sharpening

A sharpening kernel is applied to enhance image details.

The sharpening strength can be adjusted through the GUI from:

```text
0% – 100%
```

### 5. Final Enhancement

The sharpened image is blended with the gamma-corrected image and CLAHE is applied again to produce the final enhanced image.

## 📁 Project Structure

```text
Lunar/
│
├── assets/
│   └── psr_image.png
│
├── app.py
├── psr_image_enhancer.py
├── requirements.txt
├── README.md
├── .gitignore
│
└── venv/                  # Local virtual environment (not uploaded)
```

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/Alla658/Lunar.git
cd Lunar
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

#### Windows

```bash
venv\Scripts\activate
```

If PowerShell prevents activation, you can directly use the Python executable inside the environment:

```bash
venv\Scripts\python.exe
```

### 4. Install dependencies

```bash
pip install -r requirements.txt
```

## ▶️ Run the Application

Start the application with:

```bash
python app.py
```

The **PSR Image Enhancer** desktop application will open.

## 🖥️ How to Use

1. Launch the application.
2. Click **Load Image**.
3. Select a PSR image.
4. Adjust the **Gamma** slider if required.
5. Adjust the **Sharpen** slider.
6. Click **Enhance Image**.
7. The enhanced grayscale image will be displayed in the application.

## 📦 Requirements

The project dependencies are listed in `requirements.txt`:

```text
numpy
opencv-python
PyQt5
scikit-image
```

## 📌 Future Improvements

Possible future improvements include:

* Support for additional image formats
* Side-by-side original and enhanced image comparison
* Save enhanced images directly from the GUI
* Additional enhancement techniques
* Preset enhancement configurations
* Before/after image quality metrics
* Batch image enhancement
* Improved GUI controls and visualization

## 👨‍💻 Project

**Lunar – PSR Image Enhancer**

GitHub: https://github.com/Alla658/Lunar
