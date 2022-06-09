# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
1. Step1:
Import the necessary packages

2. Step 2:
Create the Text using cv2.putText

3. Step 3:
Create the structuring element

4. Step 4:
Use Opening operation

5. Step 5:
Use Closing Operation

6. Step 6:
End the program.
 
## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,300),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
im=cv2.putText(img1,'VINCENT',(5,65),font,2,(255),5,cv2.LINE_AA)
plt.imshow(im)

# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)

# Use Closing Operation
image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image1)

```
## Output:

### Display the input Image
![output4](https://user-images.githubusercontent.com/75235150/172891147-b603b3bd-940b-434b-a650-b2a2cc352c1a.png)


### Display the result of Opening
![output5](https://user-images.githubusercontent.com/75235150/172891157-50ab3e8c-d086-4cdd-82a5-8d65fbd7fa46.png)



### Display the result of Closing

![output6](https://user-images.githubusercontent.com/75235150/172891175-c3a95c03-af27-460d-8406-239e64e70264.png)


## Result:
Thus the Opening and Closing operation is used in the image using python and OpenCV.
