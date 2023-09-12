# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.
</br> 

### Step2
Convert the image from BGR to RGB.
</br> 

### Step3
Apply the required filters for the image separately.
</br> 

### Step4
Plot the original and filtered image by using matplotlib.pyplot
</br> 

### Step5
End the program.
</br> 

## Program:
```
### Developed By   : GURUMOORTHI R
### Register Number: 212222230042
</br>
```


### 1. Smoothing Filters

1.Smoothing Filters
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("a.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```

i) Using Averaging Filter
```
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
plt.show())




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


</br>

i) Using Averaging Filter

![1](https://github.com/gururamu08/IMPLEMENTATION-OF-FILTERSS/assets/118707009/da50130c-1879-4805-88ea-4f6e5db68603)

</br>

ii) Using Weighted Averaging Filter

![2](https://github.com/gururamu08/IMPLEMENTATION-OF-FILTERSS/assets/118707009/7a7ccc6a-841a-4f98-9c04-ca32aab71676)

</br>

iii) Using Gaussian Filter

![3](https://github.com/gururamu08/IMPLEMENTATION-OF-FILTERSS/assets/118707009/e69d2fc3-d4a3-40c5-80c7-f3312599147d)

</br>

iv) Using Median Filter

![4](https://github.com/gururamu08/IMPLEMENTATION-OF-FILTERSS/assets/118707009/8feca4a2-ec4b-4549-bb5e-945514628b8e)

</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

![5](https://github.com/gururamu08/IMPLEMENTATION-OF-FILTERSS/assets/118707009/48462c28-269b-45e1-8dc5-eb6e08635966)


</br>

ii) Using Laplacian Operator

![6](https://github.com/gururamu08/IMPLEMENTATION-OF-FILTERSS/assets/118707009/c831dabb-bc9d-47ac-97d5-fae087260b48)

</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
