# OPENING--CLOSING
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
Use Opening operation.

### Step5:
Use Closing Operation.
 
## Program:
```
DEVELOPED BY: DINESH KUMAR R
REGISTER NO: 212222110010
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'DINESH', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```
### Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
### Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```
### Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image

![Untitled](https://github.com/DINESH18032004/OPENING--AND-CLOSING/assets/119477784/41691341-b1bb-4fea-b3a3-81cf459a21e3)


### Display the result of Opening

![Untitled-1](https://github.com/DINESH18032004/OPENING--AND-CLOSING/assets/119477784/e5ac8680-d45f-44df-81d2-91e5e74e814c)



### Display the result of Closing

![Untitled](https://github.com/DINESH18032004/OPENING--AND-CLOSING/assets/119477784/45e3c9bb-513d-4536-acc2-d39203f67c17)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
