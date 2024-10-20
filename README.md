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
### Developed By: Viswanadham venkata sai sruthi
### Register Number: 212223240069
### Input Grayscale Image and Color Image
## Gray Image:

```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread('1.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('on')

```

## OUTPUT:

![image](https://github.com/user-attachments/assets/d1439135-bc14-44ca-b5a2-53a116b32c30)


### Histogram of Grayscale Image and any channel of Color Image
## Histrogram:

```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0,256])
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/f0cd40bb-3f24-4d96-98d8-7b960fc2e8b7)



### Histogram Equalization of Grayscale Image.

## Equalized Image:

```
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('on')
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/f59ff199-4d89-4dbe-969e-2ea2a48b2792)

## Histrogram:

```
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/fd9d1dc4-8edf-4c5d-b984-853132b06ec0)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
