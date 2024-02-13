# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:Choose an image and save it as a filename.jpg ,
### Step2:Use imread(filename, flags) to read the file.
### Step3:Use imshow(window_name, image) to display the image.
### Step4:Use imwrite(filename, image) to write the image.
### Step5:End the program and close the output image windows.
### Step6:Convert BGR and RGB to HSV and GRAY
### Step7:Convert HSV to RGB and BGR
### Step8:Convert RGB and BGR to YCrCb
### Step9:Split and Merge RGB Image
### Step10:Split and merge HSV Image

##### Program:
```
### Developed By:Sivaram R
### Register Number: 212222100050
```
<table>
  <tr>
    <td width=50%>


### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('moun.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('moun',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td>
    
#### OUTPUT:
![Deepika](https://github.com/deepikasrinivasans/COLOR_CONVERSIONS_OF-IMAGE/assets/119393935/beba183b-6b80-4254-a5ac-c0a9c0ed29be)
</td>
</tr>



<tr>
  <td width=50%>


### ii)Write the image
```Python
    import cv2
    image=cv2.imread('moun.jpg',0)
    cv2.imwrite('mini.jpg',image)
```
  </td>
  <td>

#### OUTPUT:

![deepikasinivasandipt](https://github.com/deepikasrinivasans/COLOR_CONVERSIONS_OF-IMAGE/assets/119393935/f79b52d6-f77d-4ede-8b90-7ffe48d4efaa)
</td>
</tr> 
<tr> 
  <td width=50%>

### iii)Shape of the Image
```Python
     import cv2
    image=cv2.imread('moun.jpg',1)
    print(image.shape)
```
  </td> 
  <td>

#### OUTPUT:
![deepikasrinivasandipt2](https://github.com/deepikasrinivasans/COLOR_CONVERSIONS_OF-IMAGE/assets/119393935/a2a41755-ec98-4916-8b10-ce4029169c76)
  </td>
  </tr> 
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
     import random
     import cv2
     image=cv2.imread('moun.jpg',1)
     image=cv2.resize(image,(400,400))
     for i in range (150,200):
       for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

#### OUTPUT:

![deepikasrinivasan DIPT](https://github.com/deepikasrinivasans/COLOR_CONVERSIONS_OF-IMAGE/assets/119393935/ffd8934a-d95d-4e6f-b50d-d5c9c5024c46)

 </td>
 </tr>
 <tr>
  <td width=50%>

### v)Cut and paste portion of image
```Python
     import cv2
     image=cv2.imread('moun.jpg',1)
     image=cv2.resize(image,(400,400))
     tag =image[150:200,110:160]
     image[110:160,150:200] = tag
     cv2.imshow('partimage1',image)
     cv2.waitKey(0)
     cv2.destroyAllWindows()
```
  </td>
  <td>

#### OUTPUT:

![deepikasrinivasanDIPT1](https://github.com/deepikasrinivasans/COLOR_CONVERSIONS_OF-IMAGE/assets/119393935/4c37d6dd-4392-4b61-abcc-b7dfe50a886f)
 </td>
 </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
    import cv2
    img = cv2.imread('moun.jpg',1)
    img = cv2.resize(img,(300,200))
    cv2.imshow('Original Image',img)

    hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
    cv2.imshow('BGR2HSV',hsv1)

    hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
    cv2.imshow('RGB2HSV',hsv2)

    gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
    cv2.imshow('BGR2GRAY',gray1)

    gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
    cv2.imshow('RGB2GRAY',gray2)

    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
#### OUTPUT:

![deepikasrinivasan DIPT2](https://github.com/deepikasrinivasans/COLOR_CONVERSIONS_OF-IMAGE/assets/119393935/6e7474d1-141a-49c7-9af5-d04eadaa4c69)

### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('moun.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT:

![deepikasrinivasan DIPT3](https://github.com/deepikasrinivasans/COLOR_CONVERSIONS_OF-IMAGE/assets/119393935/47eeed19-b91a-4099-87c2-ad9be38a474a)

### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('moun.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT:

![deepikasrinivasan DIPT4](https://github.com/deepikasrinivasans/COLOR_CONVERSIONS_OF-IMAGE/assets/119393935/5d881349-8569-4831-a6ca-ea4740691579)


### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('moun.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT:

![deepikasrinivasan DIPT5](https://github.com/deepikasrinivasans/COLOR_CONVERSIONS_OF-IMAGE/assets/119393935/50393780-01e4-4523-840d-f7282e980faf)


### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("moun.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
#### OUTPUT:

![deepikasrinivasan DIPT6](https://github.com/deepikasrinivasans/COLOR_CONVERSIONS_OF-IMAGE/assets/119393935/1b066b61-0ee9-45c5-abd4-b8df5e8966dd)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







