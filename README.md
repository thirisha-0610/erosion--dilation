# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages

### Step2:
create the text using cv2.put Text

### Step3:
create the structuting element

### Step4:
Erodde the image

### Step5:
Dilate the image

 
## Program:

```
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Create the Text using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'T.ROSHINI', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)


# Create the structuring element
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Input Image with Text")
plt.axis('off')
kernel = np.ones((3, 3), np.uint8)

# Erode the image
eroded_image = cv2.erode(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')


# Dilate the image
dilated_image = cv2.dilate(image, kernel, iterations=1)
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')


```
## Output:

### Display the input Image

<img width="389" height="409" alt="36daa935-d155-4c45-b825-56d4ed7e207c" src="https://github.com/user-attachments/assets/5636c86a-47c8-4ff0-970f-7051bfabd5f5" />

### Display the Eroded Image
<img width="389" height="409" alt="c53a91a2-3b54-4ecc-bdaa-291718838008" src="https://github.com/user-attachments/assets/3e5e5fcd-d869-45ab-a5d7-6c9fe2c0a128" />


### Display the Dilated Image
<img width="389" height="409" alt="94ea56ae-d2fe-49b9-9f01-7b030a2ce3b8" src="https://github.com/user-attachments/assets/aba86c96-e481-47bf-88a6-e30149367af6" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
