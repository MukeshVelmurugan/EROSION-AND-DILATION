# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary libraries (OpenCV and NumPy).
<br>
### Step2:
Use cv2.putText to add the text to the img1 image at specific coordinates.
<br>

### Step3:
Define two kernels (kernel and kernel1) for morphological operations.
<br>

### Step4:
Display the eroded image using cv2.imshow.
<br>

### Step5:
Use cv2.waitKey(0) to wait for a key press indefinitely.
<br>

## Program:
```
Developed by:MUKESH V
Register Number:212222230086
```
### Import the necessary packages
``` Python
import cv2
import numpy as np
```
### Create the Text using cv2.putText
```python
img1=np.zeros((100,400),dtype="uint8")
font=cv2.FONT_HERSHEY_PLAIN
cv2.putText("MUKESH V",(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Mukesh output",img1)
cv2.waitKey(0)
```
### Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```


### Erode the image
```python
cv2.erode(img1, kernel)
image_erode = cv2.erode(img1,kernel1)
cv2.imshow("Erode image",image_erode)
cv2.waitKey(0)
```
### Dilate the image
```python
image_dilatel=cv2.dilate(img1,kernel1)
cv2.imshow("Dilate image",image_dilatel)
cv2.waitKey(0)
```
## Output:

### Display the input Image

![image](https://github.com/MukeshVelmurugan/EROSION-AND-DILATION/assets/118707363/4292f720-cb48-43e7-a84c-08be0f01660b)


### Display the Eroded Image
![image](https://github.com/MukeshVelmurugan/EROSION-AND-DILATION/assets/118707363/7a3b9875-f2c4-4c60-95d7-96404e1a5072)





### Display the Dilated Image

![image](https://github.com/MukeshVelmurugan/EROSION-AND-DILATION/assets/118707363/f9e579eb-8d3d-4a87-ac1e-cab3170119ae)




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
