# Implementation-of-Erosion-and-Dilation

## Aim:

To implement Erosion and Dilation using Python and OpenCV.

## Software Required:

1. Anaconda - Python 3.7,

2. OpenCV.

## Algorithm:

### Step1:

Load the necessary packages requiured for the implemtation of erosion and dilation on an image.

### Step2:

Create the text image for the implemtation of erosion and dilation using cv2.putText function.

### Step3:

Create the structuring image for the implemtation of erosion and dilation on the text image.

### Step4:

Apply the erosion and dilation to the text image using cv2.erode and cv2.dilate.

### Step5:

Display the images of the erosion and dilation applied using the plt.imshow.
 
## Program:

```python

Developed by : Guru Prasad.B
Register Number: 212221230032
Program to implement Erosion and Dilation using Python and OpenCV.

# Import the necessary packages:

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText:

text_image = np.zeros((100,450),dtype = 'uint8')
font = cv2.FONT_HERSHEY_TRIPLEX = 4
cv2.putText(text_image,"Guru Prasad",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Text Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element:

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image:

image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Text Image")
plt.imshow(image_erode,'magma')
plt.axis('off')

# Dilate the image:

image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Text Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')

```

## Output:

### Display the input text Image:

![i1](https://user-images.githubusercontent.com/95342910/236000615-97998c28-605e-4c1e-b532-5ad860622a2f.png)

### Display the Eroded text Image:

![i2](https://user-images.githubusercontent.com/95342910/236000634-2075e59d-e83b-410e-9823-8415879e7b42.png)

### Display the Dilated text Image:

![i3](https://user-images.githubusercontent.com/95342910/236000660-735ad139-ca7e-4929-bc2b-7ce283d4e352.png)

## Result:

Thus the generated text image is eroded and dilated using python and OpenCV.

