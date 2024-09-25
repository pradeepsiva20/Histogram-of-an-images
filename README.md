# Histogram of an image
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
```python
# Developed By: Pradeep S
# Register Number: 212222100034

import cv2
import matplotlib.pyplot as plt

# Histogram for Gray scale and Color image
 
gray_image = cv2.imread('gray.jpg')
color_image = cv2.imread('color.jpg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()
hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()



# Equalized Image
import cv2
Gray_image=cv2.imread('gray.jpg',0)
equalized = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equalized)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:

### Input Grayscale Image and Color Image
Grayscale Image

![gray](https://github.com/user-attachments/assets/ed2d66f0-913e-406f-b956-192d9c4c3fdb)



Color Image


![color](https://github.com/user-attachments/assets/d2b54805-77c6-429b-9bc7-035968dd2edf)



### Histogram of Grayscale Image and any channel of Color Image
Grayscale Image

![grayscaleimage](https://github.com/user-attachments/assets/f25fee92-8f08-4093-a0d2-0b66d00d7d6d)


![grayscale histo](https://github.com/user-attachments/assets/01dc1996-170c-436f-a7c3-6b496d01561a)



Color Image


![color image](https://github.com/user-attachments/assets/23966119-6982-4f37-b61d-a88588a97e54)


![colorhisto](https://github.com/user-attachments/assets/4b4fe851-a5e7-4251-8f7a-bd213bf7efc9)



### Histogram Equalization of Grayscale Image.

![Screenshot 2024-09-25 233934](https://github.com/user-attachments/assets/67264be4-bfd6-4510-a8da-e7e8a9d5cc07)
![Screenshot 2024-09-25 234010](https://github.com/user-attachments/assets/f9045119-8e05-4c3c-ab76-647c129bef1a)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
