# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.
<br>
### Step2:
Create the Text using cv2.putText.
<br>
### Step3:
Create the structuring element.
<br>
### Step4:
Use Opening operation
<br>
### Step5:
Use Closing Operation
<br>
## Program:
```
Developed by : PRAKASH R
Register Number:212222240074
```

# Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
``` Python
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
cv2.putText(img1,'PRAKASH R',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
plt.title('Input Text'), plt.xticks([]), plt.yticks([])
plt.show()
```
# Create the structuring element
``` Python
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
``` Python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('OPENING'), plt.xticks([]), plt.yticks([])
plt.show()
```

# Use Closing Operation

``` Python
image1=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
plt.imshow(image1,cmap='gray')
plt.title('CLOSING'), plt.xticks([]), plt.yticks([])
plt.show()
```
## Output:

### Display the input Image

![1](https://github.com/prakash22004108/OPENING--CLOSING/assets/113497032/d87fc4b2-f565-4d55-82dc-da62f99d3675)

### Display the result of Opening

![2](https://github.com/prakash22004108/OPENING--CLOSING/assets/113497032/0d10cd4f-322f-4a3e-93ec-7fca464042af)

### Display the result of Closing

![3](https://github.com/prakash22004108/OPENING--CLOSING/assets/113497032/cc9e80e1-04eb-488c-8532-6d89a3cf43c0)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
