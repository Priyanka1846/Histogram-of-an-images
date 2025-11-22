# Histogram-of-an-images

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
```
# Developed By: PRIYANKA K
# Register Number: 212223230162
```



## Histogram of Grayscale Image

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
img = cv2.imread('parrot.jpg', cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.show()plt.hist(img.ravel(),256,range = [0, 256]);
plt.title('Original Image')
plt.show()
plt.hist(img.ravel(),256,range = [0, 256]);
plt.title('Histogram of Original Image')
plt.show()
img_eq = cv2.equalizeHist(img)
plt.hist(img_eq.ravel(), 256, range = [0, 256])
plt.title('Equalized Histogram')

```









## Output:
<img width="705" height="501" alt="image" src="https://github.com/user-attachments/assets/137eda2d-069b-4430-bba7-301a88dbc951" />

<img width="752" height="540" alt="image" src="https://github.com/user-attachments/assets/08e32189-3e4c-4410-970e-a90e8bc1a847" />
<img width="747" height="561" alt="image" src="https://github.com/user-attachments/assets/15b7382c-2c8a-4dcc-968c-1fda218b442a" />

## Histogram of Color Image
``` python
img = cv2.imread('parrot.jpg', cv2.IMREAD_COLOR)
img_hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
img_hsv[:,:,2] = cv2.equalizeHist(img_hsv[:, :, 2])
img_eq = cv2.cvtColor(img_hsv, cv2.COLOR_HSV2BGR)
plt.imshow(img_eq[:,:,::-1]); 
plt.title('Equalized Image');
plt.show()
plt.hist(img_eq.ravel(),256,range = [0, 256]);
plt.title('Histogram Equalized');
plt.show()

```

## OUTPUT
<img width="578" height="433" alt="image" src="https://github.com/user-attachments/assets/84606b2f-2a7d-4d11-b4f2-1d38f571d9e8" />


## Histogram Equilization of GrayScale Image
``` python
import cv2
import numpy as np
import matplotlib.pyplot as plt
img = cv2.imread('parrot.jpg', cv2.IMREAD_GRAYSCALE)
plt.subplot(221); plt.imshow(img[:, :, ::-1]); plt.title('Original Color Image')
plt.subplot(222); plt.imshow(img_eq[:, :, ::-1]); plt.title('Equalized Image')
plt.subplot(223); plt.hist(img.ravel(),256,range = [0, 256]); plt.title('Original Image')
plt.subplot(224); plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized');plt.show()
plt.figure(figsize = [15,4])
plt.subplot(121); plt.hist(img.ravel(),256,range = [0, 256]); plt.title('Original Image')
plt.subplot(122); plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized')
```

## OUTPUT
<img width="578" height="433" alt="image" src="https://github.com/user-attachments/assets/adf4e597-3403-4170-9157-3f751b1b36a2" />



## RESULT
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
