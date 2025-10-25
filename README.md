# OPENING--AND-CLOSING
# NAME : RAMYA.P
# REG NO : 212223240137

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result


 
## Program:

``` Python
#NAME : RAMYA.P
#REG NO : 212223240137
# Import necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt
from google.colab.patches import cv2_imshow

# i) Create the text using cv2.putText
img1 = np.zeros((300, 600), dtype='uint8')
font = cv2.FONT_ITALIC
img2 = cv2.putText(img1, "RAMYA", (5, 200), font, 2, (255), 6, cv2.LINE_AA)

cv2_imshow(img2)

# ii) Create structuring elements
kernel1 = cv2.getStructuringElement(cv2.MORPH_RECT, (11, 11))
kernel2 = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# iii) Use Opening operation (Erosion followed by Dilation)
img_open = cv2.morphologyEx(img2, cv2.MORPH_OPEN, kernel2)
cv2_imshow(img_open)

# iv) Use Closing operation (Dilation followed by Erosion)
img_close = cv2.morphologyEx(img2, cv2.MORPH_CLOSE, kernel1)
cv2_imshow(img_close)



```
## Output:

### Display the input Image
<img width="500" height="264" alt="Screenshot 2025-10-25 155425" src="https://github.com/user-attachments/assets/57096f3c-9b48-49f0-9b91-c2cfbee55abd" />


### Display the result of Opening
<img width="495" height="241" alt="image" src="https://github.com/user-attachments/assets/29e33c7f-698a-42fe-8092-031f79db8527" />


### Display the result of Closing
<img width="496" height="237" alt="image" src="https://github.com/user-attachments/assets/9e0004dc-3ffb-4219-8212-b3aec2aaf855" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
