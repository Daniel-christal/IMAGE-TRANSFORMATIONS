# IMAGE-TRANSFORMATIONS
# Developed By:Daniel C
# Reg no:212223240023

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.


### Step2:
Load the image file in the program.



### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.


### Step4:
Display the modified image output.


### Step5:
End the program.


## Program:
```python
Developed By:Daniel C
Register Number:212223240023


from google.colab import files
import cv2
import numpy as np
import matplotlib.pyplot as plt

# 🔹 Step 1: Upload image (choose a .jpg or .png file)
uploaded = files.upload()

# 🔹 Step 2: Automatically detect the uploaded filename
filename = next(iter(uploaded))
print("✅ Uploaded file:", filename)

# 🔹 Step 3: Read and convert the image
image = cv2.imread(filename)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)  # Convert BGR → RGB for Matplotlib

# -----------------------------
# 🔹 1. Image Translation
rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]])  # Shift right 50px, down 100px
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))

# 🔹 2. Image Scaling
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR)

# 🔹 3. Image Shearing
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]])
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))

# 🔹 4. Image Reflection (Horizontal Flip)
reflected_image = cv2.flip(image_rgb, 1)

# 🔹 5. Image Rotation (45°)
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1)
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))

# 🔹 6. Image Cropping
cropped_image = image_rgb[50:300, 100:400]  # Crop region (y1:y2, x1:x2)

# -----------------------------
# 🔹 Step 4: Display all images neatly

plt.figure(figsize=(12, 8))

plt.subplot(2, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image\n Developed BY: Daniel C    Reg no: 212223240023")
plt.axis('off')

plt.subplot(2, 3, 2)
plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')

plt.subplot(2, 3, 3)
plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off')

plt.subplot(2, 3, 4)
plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')

plt.subplot(2, 3, 5)
plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')

plt.subplot(2, 3, 6)
plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')

plt.tight_layout()
plt.show()

# -----------------------------
# 🔹 Step 5: Display cropped image separately
plt.figure(figsize=(4, 4))
plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()




```
## Output:

# original Image:
<img width="532" height="394" alt="image" src="https://github.com/user-attachments/assets/315d22c1-824d-4915-a724-03f13e8c1102" />

### Image Translation
<img width="479" height="392" alt="image" src="https://github.com/user-attachments/assets/3941dc6d-8b02-4291-8f08-aa9091a11922" />

### Image Scaling
<img width="544" height="441" alt="image" src="https://github.com/user-attachments/assets/cc2e641f-b90c-499f-b32f-b1f3534e4e05" />



### Image shearing
<img width="507" height="421" alt="image" src="https://github.com/user-attachments/assets/db65a8f6-8e8a-47a2-a0f3-2a8ebbacbc6c" />



### Image Reflection

<img width="456" height="437" alt="image" src="https://github.com/user-attachments/assets/61f52e7b-b3b3-45c2-b9a8-f4d2c6dfea63" />




### Image Rotation

<img width="551" height="422" alt="image" src="https://github.com/user-attachments/assets/f9860bdb-b103-4ddf-8126-43ba850c1fed" />



### Image Cropping

<img width="410" height="327" alt="image" src="https://github.com/user-attachments/assets/9345335c-f98e-4f26-8630-36a1f0ce9c31" />



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
