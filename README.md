# EX-3 Histogram of an images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


#### Program:
```
### Developed By: SRINIDHI SENTHIL
### Register Number: 212222230148
```
```
      
import cv2
import numpy as np
from matplotlib import pyplot as plt
```
```
# Load the color image
image = cv2.imread('Bright.tif')
```
```
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
```
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
```
```
# Plotting the original grayscale image, equalized image, and histograms
plt.figure(figsize=(10, 7))
```
```
# Show original grayscale image
plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
```
# Show equalized grayscale image
plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
```
# Plot histogram of the original grayscale image
plt.subplot(2, 2, 3)
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
```
# Plot histogram of the equalized image
plt.subplot(2, 2, 4)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
```
plt.tight_layout()
plt.show()
```
```
import cv2
import numpy as np
from matplotlib import pyplot as plt
```
```
# Load the color image
image = cv2.imread('Dark.tif')
```
```
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
```
```
# Plotting the original grayscale image, equalized image, and histograms
plt.figure(figsize=(10, 7))
```
```
# Show original grayscale image
plt.subplot(2, 2, 1)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
```
# Show equalized grayscale image
plt.subplot(2, 2, 2)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
```
```
# Plot histogram of the original grayscale image
plt.subplot(2, 2, 3)
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
```
# Plot histogram of the equalized image
plt.subplot(2, 2, 4)
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])

plt.tight_layout()
plt.show()
````
### Output:
![image](https://github.com/user-attachments/assets/4bd05778-3ede-46fb-b88b-1c761fe3e04e)

![image](https://github.com/user-attachments/assets/23c43b25-2d13-482b-92b0-60e7ba597c2b)


### Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
