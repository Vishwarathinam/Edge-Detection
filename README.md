### Edge-Detection
### Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

### Software Required:
Anaconda - Python 3.7

### Algorithm:
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

 
### Program:


```

# Import the packages and load the image, Convert to grayscale and remove noise:

import cv2
import matplotlib.pyplot as plt
image = cv2.imread("robin.jpg")
plt.imshow(image)
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
```

```
# SOBEL-X:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("robin.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel-X")
plt.xticks([])
plt.yticks([])
plt.show()
```

```
# SOBEL-Y:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("robin.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel-Y")
plt.xticks([])
plt.yticks([])
plt.show()
```
```
# SOBEL-XY:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("robin.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelxy=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel-XY")
plt.xticks([])
plt.yticks([])
plt.show()
```
```

# LAPLACIAN EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("robin.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Blues')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='Blues')
plt.title("Laplacian")
plt.xticks([])
plt.yticks([])
plt.show()

```
```
# CANNY EDGE DETECTOR:

import cv2
import matplotlib.pyplot as plt
image=cv2.imread("robin.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
canny_edges = cv2.Canny(image, 120, 150)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("Canny_edges")
plt.xticks([])
plt.yticks([])
plt.show()
```
### Output:
### input image:
![r1](https://user-images.githubusercontent.com/95266350/232485775-26d52e23-2fc1-4b78-ba58-1f92742ff493.png)

### SOBEL EDGE DETECTOR:
### Sobel-x
![r2](https://user-images.githubusercontent.com/95266350/232485970-f047cd3c-da15-477e-abea-a814bb8d3984.png)
### Sobel-y
![r3](https://user-images.githubusercontent.com/95266350/232486240-9bf9ad7f-f734-4704-9e2e-28d32de3e070.png)
### Sobel-xy
![r4](https://user-images.githubusercontent.com/95266350/232486317-3cff6afc-3d5d-4154-aea5-91f8b43f937d.png)


### LAPLACIAN EDGE DETECTOR
![r5](https://user-images.githubusercontent.com/95266350/232486370-c9071654-00ca-4288-b3cd-566cf677efea.png)



### CANNY EDGE DETECTOR
![r6](https://user-images.githubusercontent.com/95266350/232486408-e7da694c-118f-4ed7-a21b-fad1c183c95c.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
