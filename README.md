# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
Display the histograms with their respective images.

### Step4:
Equalize the grayscale image.

### Step5:
Display the grayscale image.

## Program:

# Developed By: S. Sanjna Priya
# Register Number: 212220230043

# Write your code to find the histogram of gray scale image and color image channels.
```
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('ts 1.jpg')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
```

# Display the histogram of gray scale image and any one channel histogram from color image
```
Color_image=cv2.imread('t2.PNG')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```

# Write the code to perform histogram equalization of the image. 
```
Gray_image=cv2.imread('ts 1.jpg',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![EXPT 3 A1](https://user-images.githubusercontent.com/75234965/165235447-33a00aa9-77ae-40fa-9d8d-9b054d641e5e.PNG)

![EXPT 3 A2](https://user-images.githubusercontent.com/75234965/165235470-9d2a08b6-f573-4cbc-9810-9f69ff5f3572.PNG)

### Histogram of Grayscale Image and any channel of Color Image

![EXPT 3 B1](https://user-images.githubusercontent.com/75234965/165235507-88165bdf-689c-49f2-b320-f9a7fad8b12a.PNG)

![EXPT 3 B2](https://user-images.githubusercontent.com/75234965/165235524-e38b6c0b-5608-48ef-a536-d7a61419da06.PNG)

### Histogram Equalization of Grayscale Image

![EXPT 3 C1](https://user-images.githubusercontent.com/75234965/165235555-88b36952-8f81-4912-88c3-b8740b08d85e.PNG)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
