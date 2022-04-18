# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg
<br>

### Step2:
Use imread(filename, flags) to read the file.
<br>

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.
<br>

### Step4:
Split and merge the image using cv2.split and cv2.merge commands.
<br>

### Step5:
End the program and close the output image windows.
<br>

## Program:
```python
# Developed By: Srinivasan S
# Register Number: 212220230048

# i) Convert BGR and RGB to HSV and GRAY

import cv2
color_image = cv2.imread('ee.jpg')
cv2.imshow('Original image',color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# ii)Convert HSV to RGB and BGR

import cv2
color_image = cv2.imread('ee.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

import cv2
color_image = cv2.imread('ee.jpg')
cv2.imshow('Original image',color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()

# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('ee.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

# v) Split and merge HSV Image

import cv2
image = cv2.imread('ee.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot 2022-04-18 203550](https://user-images.githubusercontent.com/103049243/163828719-2af928e8-0019-4aec-9845-e05c096cb47e.png)


### ii) HSV to RGB and BGR
![Screenshot 2022-04-18 203608](https://user-images.githubusercontent.com/103049243/163828744-b43f2435-8428-4aad-a9ee-2b0b42e6006c.png)


### iii) RGB and BGR to YCrCb

![Screenshot 2022-04-18 203634](https://user-images.githubusercontent.com/103049243/163828769-766f3b04-1d60-4661-bb65-7c0c6428eccc.png)

### iv) Split and merge RGB Image

![Screenshot 2022-04-18 203654](https://user-images.githubusercontent.com/103049243/163828790-a233fdaa-d323-4662-8e85-9e98c528bb4c.png)

### v) Split and merge HSV Image

![Screenshot 2022-04-18 203709](https://user-images.githubusercontent.com/103049243/163828824-59e867cb-8668-4c1c-9b09-60e881973a89.png)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
