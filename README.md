# 📸 Image Processing Library (v1.1.4)
![image](https://github.com/user-attachments/assets/6082f8ed-18b4-4a6a-97f0-3b0eeb1813bc)

**📅 Date:** May 26, 2020  

---

## 🎯 Objective  
Develop a library in C language to perform image processing operations.  
![image](https://github.com/user-attachments/assets/e96f3fb1-9db4-456c-b5a5-9ba2b4165ce7)
![image](https://github.com/user-attachments/assets/b801f8bf-d9f8-4ace-8064-44789b3f7d5f)
![image](https://github.com/user-attachments/assets/0c286a61-3351-48b5-9229-b6cf92d4397e)

### 🔍 Project Overview  
The project is divided into three main parts:  
1️⃣ **Matrix Handling:** Implement methods for handling 3D matrices, including mathematical operations and memory management.  
2️⃣ **Image Processing:** Develop methods for operations like grayscale conversion and image corruption.  
3️⃣ **Convolution & Filters:** Implement convolution and apply filters to create visual effects.

*To achieve maximum points, correctly implement all methods in the file **ip_lib.h***.  

---

## 🌟 Introduction  

### 🖼️ Images in Computers  
- Images are grids of pixels, each representing a color at a specific point.  
- **Grayscale Images:** Single channel (brightness).  
- **Color Images:** Three channels (red, green, blue). Each pixel consists of three values, forming a 3D matrix: **width × height × 3**.  
- These are called 24-bit images (8 bits per channel × 3 channels).

### 📂 Provided Bitmap Library  
- A C library for reading and writing BMP images is included in the project files.  
- Library source: [GitHub](https://github.com/wernsey/bitmap)  
- Documentation: [Bitmap Library](http://wstoop.co.za/bitmap.php)

**Steps to Get Started:**  
1️⃣ Compile `bmp.c` into `bmp.o` using the `-Wall` flag.  
2️⃣ Add `-lm` to include math libraries.  
3️⃣ Compile `test_bmp.c` with `bmp.o` and execute.  
4️⃣ The output file `mandelbrot.bmp` should contain a fractal image!  

---

## 📋 Project Details  

### 🖌️ Image Processing  
Image processing applies transformations to images. Applications include:  
- 🎨 Noise Removal  
- 🌈 Format Conversion  
- ✂️ Scaling & Cropping  
- 🔍 Edge Detection  

---

### 1️⃣ **Part 1: Matrix Operations and Memory Management**  

#### 🛠️ Data Structure: ip_mat  
The custom `ip_mat` type represents a 3D matrix (height × width × channels) for image pixel values. Pixel values are stored as floats for more precision.  

**Structure Definition:**  
- **Fields:**  
  - `w`: Width  
  - `h`: Height  
  - `k`: Channels (3 for color images)  
  - `data`: 3D matrix of float values  
  - `stat`: Channel-specific statistics (min, max, mean).  

**Statistics Structure:**  
- `stats` contains:  
  - `min`: Minimum value  
  - `max`: Maximum value  
  - `mean`: Average value  

---

### 2️⃣ **Part 2: Basic Image Operations**  

#### ✨ Brightening  
Increase image brightness by adding a constant to all pixel values.  

#### 🖤 Grayscale Conversion  
Convert a color image into grayscale by averaging the red, green, and blue channels.  

#### 🎲 Noise Addition  
Add Gaussian noise to simulate imperfections in images.  

#### 🎨 Blending  
Combine two images using a weighted average.  

---

### 3️⃣ **Part 3: Convolution & Filtering**  

#### 🔄 Convolution  
Convolution applies filters to images using weighted averages. Filters include sharpening, blurring, and edge detection.  

#### 🖼️ Padding  
Add borders to images to maintain size after filtering.  

#### 🌀 Gaussian Blur  
- **Effect:** Smoothens the image, reducing noise.  
- Larger kernels and higher sigma values create stronger blur effects.  

---

### 🛠️ Filters to Implement  

- **Sharpen Filter:** Enhance image details.  
- **Edge Detection:** Highlight edges.  
- **Emboss Filter:** Add depth perception.  
- **Average Filter:** Smooth image by averaging neighboring pixels.  
- **Gaussian Filter:** Apply a blur effect.  

---

### 📊 Expected Results  
Apply these filters to an example image (e.g., `flower.bmp`) and observe the effects, such as:  
- **Edge Detection:** Highlights object boundaries.  
- **Blurring:** Smoothens noise and details.  
- **Sharpening:** Enhances sharpness for clarity.  

---

Let me know if you’d like me to adjust or expand any section! 🚀
