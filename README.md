# Implementation-of-Erosion-and-Dilation->
## Aim:
To implement Erosion and Dilation using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
```
Developed By : Roselin mary jovita s
Reg No : 212222230122
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
image = np.zeros((300, 900, 3), dtype="uint8")
text = "ROSELIN MARY JOVITA S"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
### Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```
### Erode the image
```
eroded_image = cv2.erode(image, kernel, iterations=1)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")
```
### Dilate the image
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
```
## Output:

### Display the input Image

![Screenshot 2024-10-26 110639](https://github.com/user-attachments/assets/c5568d5d-9ece-4de1-ab77-7d049f78f30e)

### Display the Eroded Image

![Screenshot 2024-10-26 110648](https://github.com/user-attachments/assets/4d041c36-c5c4-4330-82b3-df07f9f689b3)

### Display the Dilated Image

![Screenshot 2024-10-26 110657](https://github.com/user-attachments/assets/3b454dad-478b-46eb-85d1-7a2f19ab7423)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
