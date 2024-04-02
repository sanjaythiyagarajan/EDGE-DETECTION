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
DEVELOPED BY: SANJAY T
REGISTER NUMBER: 212222110039
```
## IMPORT PACKAGES AND LOAD IMAGES
  ```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dip6.jpeg",0)
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

![dip6](https://github.com/sanjaythiyagarajan/EDGE-DETECTION/assets/119409242/ecfc9643-d748-48b8-966f-9b099a97a318)

### SOBEL EDGE DETECTOR:

![image](https://github.com/sanjaythiyagarajan/EDGE-DETECTION/assets/119409242/15a6213b-6dfa-4a3b-89f3-f31da7e72606)

![image](https://github.com/sanjaythiyagarajan/EDGE-DETECTION/assets/119409242/ce9cd17a-2f84-41f5-b91a-5fa3a25196ef)

![image](https://github.com/sanjaythiyagarajan/EDGE-DETECTION/assets/119409242/b1948bbc-13f6-4ccc-beb7-180b44f0399b)

### LAPLACIAN EDGE DETECTOR

![image](https://github.com/sanjaythiyagarajan/EDGE-DETECTION/assets/119409242/1a82a8fc-deba-4a70-a9d6-17b19ba37514)

### CANNY EDGE DETECTOR

![image](https://github.com/sanjaythiyagarajan/EDGE-DETECTION/assets/119409242/c56677a4-259c-4eb5-9866-57d264369074)

## Result:

Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
