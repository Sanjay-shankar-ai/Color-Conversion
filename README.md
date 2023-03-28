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
![2023-03-28](https://user-images.githubusercontent.com/94231938/228321513-9687feb1-96f0-4738-828f-95695e1b154e.png)

### ii)  HSV to RGB and BGR
 
![2023-03-28 (1)](https://user-images.githubusercontent.com/94231938/228321868-01faeca6-dd3e-42dc-a24a-70663b2007f8.png)

### iii) RGB and BGR to YCrCb
![2023-03-28 (2)](https://user-images.githubusercontent.com/94231938/228321994-24282304-cd39-419f-9c89-a0073c24df0d.png)


### iv) Split and merge RGB Image

![2023-03-28 (3)](https://user-images.githubusercontent.com/94231938/228322132-eafd4652-fc4d-40d5-98a0-cc3e5ac83195.png)


### v) Split and merge HSV Image

![2023-03-28 (4)](https://user-images.githubusercontent.com/94231938/228322149-32b918c1-58b3-4881-b203-ca472766032d.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
