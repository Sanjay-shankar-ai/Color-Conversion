# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg.

### Step2:
Use imread(filename, flags) to read the file.

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:
Split and merge the image using cv2.split and cv2.merge commands.

### Step5:
End the program and close the output image windows.

## Program:
```
# Developed By: Sanjay.s
# Register Number: 212221230086
```
# i) Convert BGR and RGB to HSV and GRAY
```
import cv2
color_image = cv2.imread('out.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```
# ii)Convert HSV to RGB and BGR
```
import cv2
color_image = cv2.imread('out.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```

# iii)Convert RGB and BGR to YCrCb
```
import cv2
color_image = cv2.imread('out.jpg')
cv2.imshow('Original image', color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```

# iv)Split and Merge RGB Image
```
import cv2
image = cv2.imread('out.jpg')
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
```

# v) Split and merge HSV Image
```
import cv2
image = cv2.imread('out.jpg')
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

![2023-03-28 (1)](https://user-images.githubusercontent.com/94231938/228320778-01c4898e-53c3-481f-a3ed-2e2bd9a73a5a.png)

### ii) HSV to RGB and BGR

![2023-03-28 (2)](https://user-images.githubusercontent.com/94231938/228320786-a77e0fa1-c8f3-4f23-a42a-f9a075d8cfa0.png)

### iii) RGB and BGR to YCrCb

![Uploading 2023-03-28 (3).png…]()

### iv) Split and merge RGB Image
![2023-03-28 (4)](https://user-images.githubusercontent.com/94231938/228320798-5279df80-1948-4d9d-8b28-91e7fca598ca.png)


### v) Split and merge HSV Image
![2023-03-28](https://user-images.githubusercontent.com/94231938/228320825-0ab38d0b-e732-4493-a0a3-408434350dd7.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
