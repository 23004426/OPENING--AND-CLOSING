# OPENING--AND-CLOSING
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

### Step5:
End the program
 
## Program:
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'PUSHPA',(5,70), font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1)
plt.axis('off')


# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Use Opening operation
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")



# Use Closing Operation
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")

### Output:

### Display the input Image
![image](https://github.com/23004426/OPENING--AND-CLOSING/assets/144979327/4d043239-0d73-4aad-9183-35777c5c1160)

### Display the result of Opening
![image](https://github.com/23004426/OPENING--AND-CLOSING/assets/144979327/6ccf0030-8143-471e-9eb2-45cd3c1cc6d0)

### Display the result of Closing
![image](https://github.com/23004426/OPENING--AND-CLOSING/assets/144979327/31a24f85-9655-4aaa-af25-8234171233d7)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
