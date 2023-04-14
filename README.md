# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the required packages for further process.

### Step2:

Read the image and convert the bgr image to gray scale image.


### Step3:
Use any filters for smoothing the image to reduse the noise.


### Step4:
Apply the respective filters -Sobel,Laplacian edge dectector and Canny edge dector.

### Step5:
Display the filtered image using plot and imshow.

 
## Program:

Developed by : K.Jhansi

Ref No : 212221230045

``` Python

# Import the packages

import cv2

import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise

img=cv2.imread("taj.jpg")

img1=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)

plt.imshow(img1)

plt.title("Original Image")

plt.show()

gray1=cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)

plt.imshow(gray1)

plt.imshow(gray1,cmap="gray")

plt.title("Gray image")

plt.show()

# SOBEL EDGE DETECTOR

## SOBELx

sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)

plt.figure(figsize=(15,15))

plt.subplot(1,2,1)

plt.imshow(gray)

plt.title("Original Image")

plt.axis("off")

plt.subplot(1,2,2)

plt.imshow(sobelx)

plt.title("Sobel X axis")

plt.axis("off")

plt.show()

## SOBEly

sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)

plt.figure(figsize=(15,15))

plt.subplot(1,2,1)

plt.imshow(gray)

plt.title("Original Image")

plt.axis("off")

plt.subplot(1,2,2)

plt.imshow(sobely)

plt.title("Sobel Y axis")

plt.axis("off")

plt.show()

## SOBELxy

sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)

plt.figure(figsize=(15,15))

plt.subplot(1,2,1)

plt.imshow(gray)

plt.title("Original Image")

plt.axis("off")

plt.subplot(1,2,2)

plt.imshow(sobelxy)

plt.title("Sobel XY axis")

plt.axis("off")

plt.show()



# LAPLACIAN EDGE DETECTOR

lap=cv2.Laplacian(gray,cv2.CV_64F)

plt.figure(figsize=(15,15))

plt.subplot(1,2,1)

plt.imshow(gray)

plt.title("Original Image")

plt.axis("off")

plt.subplot(1,2,2)

plt.imshow(lap)

plt.title("Laplacian Edge Detector")

plt.axis("off")

plt.show()


# CANNY EDGE DETECTOR

canny=cv2.Canny(gray,120,150)

plt.figure(figsize=(15,15))

plt.subplot(1,2,1)

plt.imshow(gray)

plt.title("Original Image")

plt.axis("off")

plt.subplot(1,2,2)

plt.imshow(canny)

plt.title("Canny Edge Detector")

plt.axis("off")

plt.show()



```
## Output:

### GRAY IMAGE
![output]()
### SOBEL EDGE DETECTOR
![output]()

### LAPLACIAN EDGE DETECTOR
![output]()


### CANNY EDGE DETECTOR
![output]()
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
