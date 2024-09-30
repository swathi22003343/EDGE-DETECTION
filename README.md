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
```
Developed by : SWATHI D
Register No  : 212222230154
```

``` Python
# Import the packages

import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise

image = cv2.imread("tow.png")
gimage = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
image = cv2.GaussianBlur(gimage,(3,3),0)

# SOBEL EDGE DETECTOR

#SOBEL X:

sobelx = cv2.Sobel(image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image,cmap = 'RdPu')
plt.title('Rdpu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()

# SOBEL Y:

sobely = cv2.Sobel(image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()

# SOBEL XY:

sobelxy = cv2.Sobel(image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()

# LAPLACIAN EDGE DETECTOR

laplacian = cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()

# CANNY EDGE DETECTOR

canny_edge = cv2.Canny(image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(image,cmap = 'gray')
plt.title('gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
#### SOBEL X
![](sx.png)
#### SOBEL Y
![](sy.png)
#### SOBEL XY
![](sy.png)

### LAPLACIAN EDGE DETECTOR
![](lap.png)

### CANNY EDGE DETECTOR
![](can.png)
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
