# EX-6 EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.
### Step2:
Load a image using imread() from cv2 module.
### Step3:
Convert the image to grayscale
### Step4:
Using Sobel operator from cv2,detect the edges of the image.
### Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## PROGRAM:
```
DEVELOPED BY:SWATHI D
REGISTER NUMBER: 212222230154
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("edge.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## SOBEL EDGE DETECTOR:
**SOBEL X:**
  ```python
  sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y:**
```python
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY:**
  ```python
  sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
## LAPLACIAN EDGE DETECTOR:
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
## CANNY EDGE DETECTOR:
```python
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## ORIGINAL IMAGE:
![edge](https://github.com/deepikasrinivasans/EDGE-DETECTION/assets/119393935/918b52c9-7b38-49ec-83a8-ce40b9a0495d)
### SOBEL EDGE DETECTOR:
![d1](https://github.com/deepikasrinivasans/EDGE-DETECTION/assets/119393935/9b9cddf5-2c94-44fe-927a-5d3e3eeee552)
![d2](https://github.com/deepikasrinivasans/EDGE-DETECTION/assets/119393935/e5b0318a-c102-4f90-a76d-4f61b9321035)
![d3](https://github.com/deepikasrinivasans/EDGE-DETECTION/assets/119393935/bc5ede85-aabf-4b7f-8b2f-191d78911b9e)
### LAPLACIAN EDGE DETECTOR
![d4](https://github.com/deepikasrinivasans/EDGE-DETECTION/assets/119393935/1e91aada-fe49-4789-8d4e-1f02e2fc0965)
### CANNY EDGE DETECTOR
![d5](https://github.com/deepikasrinivasans/EDGE-DETECTION/assets/119393935/c0df0b60-34b9-45bb-aec3-0a6e9380499b)
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
