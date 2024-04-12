# EX 03 Histogram-of-an-images
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


## Program:
```python
# Developed By: THIRISHA.S
# Register Number: 212222230160

```
## Output:

### Input Grayscale Image and Color Image
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("vijay.jpeg")
color_image = cv2.imread("ajith.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Thirisha-s/Histogram-of-an-images/assets/120380280/8115a904-bb00-4ad4-a378-b370fb1464bc)

![Screenshot 2024-04-12 083509](https://github.com/Thirisha-s/Histogram-of-an-images/assets/120380280/15a920ad-9e37-4e68-898f-7384debd6c09)

### Histogram of Grayscale Image and any channel of Color Image
```python
import numpy as np
import cv2
Gray_image = cv2.imread("vijay.jpeg")
Color_image = cv2.imread("ajith.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
![image](https://github.com/Thirisha-s/Histogram-of-an-images/assets/120380280/0fb61e70-cd18-4c20-a249-7c9e4bdb4e63)


## Grayscale Image

![Screenshot 2024-04-12 083609](https://github.com/Thirisha-s/Histogram-of-an-images/assets/120380280/daa59928-a2e0-4a83-92b6-80b2e0ae9b37)

![Screenshot 2024-04-12 083623](https://github.com/Thirisha-s/Histogram-of-an-images/assets/120380280/621a3ae4-d07b-4a00-a96d-de80f24cc96e)

## Colour Image
```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
![image](https://github.com/Thirisha-s/Histogram-of-an-images/assets/120380280/b80ea90a-55e6-4ee8-afe3-a1b24fa20e9d)

![Screenshot 2024-04-12 083651](https://github.com/Thirisha-s/Histogram-of-an-images/assets/120380280/6f37eb07-4a18-4df7-b6b3-24d0b1d1db3f)

![Screenshot 2024-04-12 083726](https://github.com/Thirisha-s/Histogram-of-an-images/assets/120380280/a612d921-4953-4486-b152-ef6500711941)

### Histogram Equalization of Grayscale Image.
```python
import cv2
gray_image = cv2.imread("vijay.png",0)
cv2.imshow('Gray Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/Thirisha-s/Histogram-of-an-images/assets/120380280/cd95c458-86c4-4e12-af89-339584269ee8)


![Screenshot 2024-04-12 083834](https://github.com/Thirisha-s/Histogram-of-an-images/assets/120380280/f2156f52-07a1-485d-ae41-69d4ac86e005)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
