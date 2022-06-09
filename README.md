# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
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
 
## Program:

``` Python
# Developed by: P. Siva Naga Nithin.
# Register no.: 212221240037
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_ITALIC
im=cv2.putText(img,' P. Siva Naga Nithin ',(5,70),font,1.5,(255),5,cv2.LINE_AA)
plt.imshow(cv2.cvtColor(im, cv2.COLOR_BAYER_GB2RGB))

# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(img,cv2.MORPH_OPEN,Kernel)
plt.imshow(cv2.cvtColor(image1,cv2.COLOR_BAYER_GB2RGB))

# Use Closing Operation
image1=cv2.morphologyEx(img,cv2.MORPH_CLOSE,Kernel)
plt.imshow(cv2.cvtColor(image1,cv2.cv2.COLOR_BAYER_GB2RGB))
plt.axis('off')

```
## Output:

### Display the input Image
![11 1](https://user-images.githubusercontent.com/94154780/172907381-58ad28b4-a83e-4ab2-8b5c-05286da8545a.png)

### Display the result of Opening
![11 2](https://user-images.githubusercontent.com/94154780/172907421-1a157b43-9396-4dd8-8a3e-55b765c42d02.png)


### Display the result of Closing
![11 3](https://user-images.githubusercontent.com/94154780/172907434-f020d06b-000b-40d2-a905-744ae7cdd4f4.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
