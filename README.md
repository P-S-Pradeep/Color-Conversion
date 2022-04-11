# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:

Import cv2 and save and image as filename.jpg
### Step2:

Use imread(filename, flags) to read the file.

### Step3:

Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:

Split and merge the image using cv2.split and cv2.merge commands.

### Step5:

End the program and close the output image windows.

## Program:
```python
# Developed By:Pradeep.P.S
# Register Number:212220230034

#prerequisites
import cv2
img=cv2.imread("rr.jpg")
cv2.imshow("trade",img)
cv2.waitKey(0)


# i) Convert BGR and RGB to HSV and GRAY
# bgr to hsv and gray
bgr_hsv = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',bgr_hsv)
bgr_gray = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',bgr_gray)
#rgb to hsv and gray
rgb_hsv = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',rgb_hsv)
rgb_gray = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',rgb_gray)
cv2.waitKey(0)


# ii)Convert HSV to RGB and BGR
hsv_rgb = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',hsv_rgb)
hsv_bgr = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',hsv_bgr)
cv2.waitKey(0)


# iii)Convert RGB and BGR to YCrCb
rgb_ycrcb = cv2.cvtColor(img,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',rgb_ycrcb)
bgr_ycrcb = cv2.cvtColor(img,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',bgr_ycrcb)
cv2.waitKey(0)


# iv)Split and Merge RGB Image
#split rgb
blue=img[:,:,0]
green=img[:,:,1]
red=img[:,:,2]
cv2.imshow("B",blue)
cv2.imshow("G",green)
cv2.imshow("R",red)
#merge rgb
Merge_rgb=cv2.merge((blue,green,red))
cv2.imshow("Merge_RGB",Merge_rgb)
cv2.waitKey(0)


# v) Split and merge HSV Image
#split hsv
h,s,v=cv2.split(bgr_hsv)
cv2.imshow("H",h)
cv2.imshow("S",s)
cv2.imshow("V",v)
#merge hsv
Merge_hsv=cv2.merge((h,s,v))
cv2.imshow("Merge_hsv",Merge_hsv)
cv2.waitKey(0)




```
## Output:
### i) BGR and RGB to HSV and GRAY
![Screenshot (58)](https://user-images.githubusercontent.com/102652887/162793093-201bcfc0-defd-49f0-8be9-1fa8c6ec0c99.png)


### ii) HSV to RGB and BGR
![Screenshot (59)](https://user-images.githubusercontent.com/102652887/162793753-0e1283c7-994e-4361-aa45-faff69d48dd6.png)



### iii) RGB and BGR to YCrCb
![WhatsApp Image 2022-04-11 at 11 06 36 PM](https://user-images.githubusercontent.com/102652887/162797728-94737803-4db3-46d0-a1d3-896e6122351c.jpeg)





### iv) Split and merge RGB Image
![Screenshot (61)](https://user-images.githubusercontent.com/102652887/162792965-500437b3-0978-4307-bf10-93565d1c8b94.png)


### v) Split and merge HSV Image
![Screenshot (62)](https://user-images.githubusercontent.com/102652887/162792838-5f8a1265-e4b4-41c8-a96d-c98246ff4a26.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
