# Record-IMPLEMENTATION-OF-EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
Anaconda - Python 3.7
OpenCV

## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
#### Name:  Vignesh S
#### Reg.No: 212223230240

### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```

### Add Text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'NAME : VIGNESH S', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```

### Display the input image
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/d0ddd4f0-2906-4d5d-af17-f23bc3eeda87" />



### Create a simple square kernel (3x3)
```
kernel = np.ones((3, 3), np.uint8)
```
### Apply erosion (shrinking effect)
```
eroded_image = cv2.erode(image, kernel, iterations=1)
```

### Display the eroded image
```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/968c0a74-274e-470c-bbe2-ffe6bc363551" />



### Apply dilation (expanding effect)
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```

### Display the dilated image
```
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```
<img width="389" height="411" alt="image" src="https://github.com/user-attachments/assets/6512b8af-97aa-4501-9e4e-4983094790e7" />



## Result
Thus the generated text image is eroded and dilated using python and Op
