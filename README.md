### EX NO : 11
### DATE  : 03.06.2022
# <p align="center">Opening and Closing</p>


## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.

<br/><br/><br/><br/><br/>

## PROGRAM:
```
/*
Developed by   : Graham Stanes
Register Number: 212220230020
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,450),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Vijayaragavan',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>

## OUTPUT:

### Display the input Image
![1](https://user-images.githubusercontent.com/75235488/172897744-565ee9b1-22e4-48ba-9134-50d2ce90dd0c.png)

### Display the result of Opening
![2](https://user-images.githubusercontent.com/75235488/172897776-5ce5e28a-6442-43c4-9649-3cb34f13d285.png)

### Display the result of Closing

![3](https://user-images.githubusercontent.com/75235488/172897813-d30e7b2a-eaf1-4f2e-ae51-62ddf1cc404c.png)

## RESULT:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
