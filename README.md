# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1:Read the Image:
Load the input color image from a specified path.

### Step-2:Convert to Grayscale:
Transform the color image into a grayscale format for easier processing.

### Step-3:Edge Detection:
Apply an edge detection technique to identify the prominent edges in the grayscale image.

### Step-4:Create Structuring Element:
Define a kernel (structuring element) for use in morphological operations, typically a matrix of ones.
### Step5:Morphological Operations:
Perform morphological operations:
Opening: Remove small objects from the edges to clean up the image.
Closing: Fill small holes in the detected edges to enhance the structure.
### step-6:Display Results:
Show the original grayscale image, along with the results of the opening and closing operations for visual comparison.

## Program:
```
Developed by:VEDHASHREE.G
Reg.no:212223240171
```
# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
image = cv2.imread("FISH.jpg")  
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(10, 5))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```

# Create the structuring element
```
image = cv2.imread("FISH.jpg")  
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.figure(figsize=(10, 5))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
![373865761-c6772ac7-5d88-46ba-9c06-f63c15e3c7ed](https://github.com/user-attachments/assets/dcc1c0d6-f1de-4511-bb00-ac2a5c46583e)

# Use Opening operation
```
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```
![373865786-1dc47e42-1357-449e-9d9b-6984ddb666a6](https://github.com/user-attachments/assets/4b90425d-c295-408f-a7f4-12f1af3b54e8)

# Use Closing Operation
```
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
```
![373865805-4f0cd2c5-bbdd-4cbc-bf99-ab1bc25001be](https://github.com/user-attachments/assets/d2514086-71a5-45ff-9f2c-74e379873545)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
