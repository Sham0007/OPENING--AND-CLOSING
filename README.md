# EXP-10 OPENING--AND-CLOSING
# NAME SARAVANAN SHAM PRAKASH
# REF NO 212224230254
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation

### Step5:
Use Closing Operation
 
## Program:
## DEVELOPED BY:SARAVANAN SHAM PRAKASH
## REG NO:212224230254 


# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```



# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'SHAM PRAKASH', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```



# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```



# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```




# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```








## Output:

### Display the input Image
<img width="856" height="217" alt="image" src="https://github.com/user-attachments/assets/f55a248c-bb1a-4714-beb0-363facd38a74" />


### Display the result of Opening
<img width="884" height="230" alt="image" src="https://github.com/user-attachments/assets/8b26123d-0fdf-41b0-96f5-169e29623be5" />


### Display the result of Closing
<img width="874" height="226" alt="image" src="https://github.com/user-attachments/assets/fb6659c1-0671-49c3-9c6c-30658938fc67" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
