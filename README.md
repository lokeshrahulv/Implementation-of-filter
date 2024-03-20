# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.
### Step2
Convert the image from BGR to RGB.
### Step3
Apply the required filters for the image separately.
### Step4
Plot the original and filtered image by using matplotlib.pyplot.
### Step5
End the program.

## Program:
### Developed By   :LOKESH RAHUL V V
### Register Number:212222100024

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("dog2.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters
i) Using Averaging Filter
![Screenshot 2024-03-20 210440](https://github.com/lokeshrahulv/Implementation-of-filter/assets/118423842/af51fd00-fae1-4d85-892f-2059e1d1828d)

ii) Using Weighted Averaging Filter
![Screenshot 2024-03-20 210447](https://github.com/lokeshrahulv/Implementation-of-filter/assets/118423842/cc1b713a-2be3-4b5e-9821-b5595e02262d)

iii) Using Gaussian Filter
![Screenshot 2024-03-20 210453](https://github.com/lokeshrahulv/Implementation-of-filter/assets/118423842/8afcc29a-034c-4ce3-af8f-50b29fe28ea2)

iv) Using Median Filter
![Screenshot 2024-03-20 210500](https://github.com/lokeshrahulv/Implementation-of-filter/assets/118423842/72125faa-fd70-45ff-bef6-895edf08803d)

### 2. Sharpening Filters
i) Using Laplacian Kernal
![Screenshot 2024-03-20 210506](https://github.com/lokeshrahulv/Implementation-of-filter/assets/118423842/4be8cd6c-097b-49c2-8c30-af80aaf4df46)

ii) Using Laplacian Operator
![Screenshot 2024-03-20 210510](https://github.com/lokeshrahulv/Implementation-of-filter/assets/118423842/82976bae-0850-4402-b520-381ed801b961)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
