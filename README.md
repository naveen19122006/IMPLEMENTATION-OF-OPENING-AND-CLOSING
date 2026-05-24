# IMPLEMENTATION OF OPENING AND CLOSING

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages


### Step2:
Read the image

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

### Step6:
Display all the output images

 
## Program:
```
Developed By: NAVEEN KUMAR E
Register NO: 212224230181
```
``` Python
# Import the necessary packages
import cv2
import numpy as np

# Create the Text using cv2.putText
img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'NAVEEN KUMAR E', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)

# Create the structuring element
struct_ele = np.ones((9, 9), np.uint8)

# Use Opening operation
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)

# Use Closing Operation
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)

# Close all windows
cv2.destroyAllWindows()
```
## Output:

### Display the input Image
<img width="589" height="469" alt="image" src="https://github.com/user-attachments/assets/29445512-2a51-42e2-87a2-4bbd6d6fa8de" />


### Display the result of Opening
<img width="644" height="458" alt="image" src="https://github.com/user-attachments/assets/eeb7f4e8-79f8-4ca0-97af-79f0354418e8" />


### Display the result of Closing
<img width="586" height="483" alt="image" src="https://github.com/user-attachments/assets/76644d2a-805b-4e25-a7fd-adfd8688a74d" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
