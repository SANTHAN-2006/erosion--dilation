# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image
 
## Program:
### Developed by : K SANTHAN KUMAR
### Register Number : 212223240065
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Create the Text using cv2.putText
img = np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,'SANTHAN',(40,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

# Display the input Image :
![image](https://github.com/SANTHAN-2006/erosion--dilation/assets/80164014/0178461f-40c5-4784-bacf-e6fbeba518d5)


# Display the Eroded Image :
![image](https://github.com/SANTHAN-2006/erosion--dilation/assets/80164014/cd240c3b-829b-44a9-8314-bff1cd271686)


# Display the Dilated Image :
![image](https://github.com/SANTHAN-2006/erosion--dilation/assets/80164014/060096fd-675f-41ac-b118-f608cd0759c1)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
