# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:

### Developed By: Vinush.CV
### Register Number: 212222230176
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('football.jpeg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)  # Convert BGR to RGB for Matplotlib
plt.subplot()
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')
```
### i)Image Translation
```python
rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]])  # Translate by (50, 100) pixels
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))
plt.subplot()
plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')
```
### ii) Image Scaling
```python
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR)  # Scale by 1.5x
plt.subplot()
plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')
```
### iii)Image shearing
```python
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  # Shear with factor 0.5
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))
plt.subplot()
plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')
```
### iv)Image Reflection
```python
reflected_image = cv2.flip(image_rgb, 1)  # Horizontal reflection (flip along y-axis)
plt.subplot()
plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')
```

### v)Image Rotation
```python
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1)  # Rotate by 45 degrees
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))
plt.subplot()
plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')
```


### vi)Image Cropping
```python
cropped_image = image_rgb[50:300, 100:400]  # Crop a portion of the image
plt.figure(figsize=(4, 4))
plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()
```
## Output:
### i)Image Translation

![image](https://github.com/user-attachments/assets/4ef15972-8c35-41e2-b8bb-2347b51114de)

### ii) Image Scaling




### iii)Image shearing
![Uploading image.png…]()



### iv)Image Reflection
<br>
<br>
<br>
<br>



### v)Image Rotation
<br>
<br>
<br>
<br>



### vi)Image Cropping
<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
