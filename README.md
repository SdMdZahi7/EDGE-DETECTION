# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program:

### SOBEL X:
~~~
import cv2
import matplotlib.pyplot as plt
image=cv2.imread("Imagee.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel-X")
plt.xticks([])
plt.yticks([])
plt.show()
~~~

### SOBEL Y:
~~~
import cv2
import matplotlib.pyplot as plt
image=cv2.imread("image.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Purples')
plt.title('Purples')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap='Purples')
plt.title("Sobel-Y")
plt.xticks([])
plt.yticks([])
plt.show()
~~~
### SOBEL XY:
~~~
import cv2
import matplotlib.pyplot as plt
image=cv2.imread("imagee.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Oranges')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap='Oranges')
plt.title("Sobel-XY")
plt.xticks([])
plt.yticks([])
plt.show()
~~~
### LAPLACIAN EDGE DETECTOR
~~~
import cv2
import matplotlib.pyplot as plt
image=cv2.imread("image1.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='Blues')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap='Blues')
plt.title("Laplacian")
plt.xticks([])
plt.yticks([])
plt.show()
~~~
### CANNY EDGE DETECTOR
~~~
import cv2
import matplotlib.pyplot as plt
image=cv2.imread("image.jpg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
img=cv2.GaussianBlur(gray_img,(3,3),0)
canny_edges = cv2.Canny(image, 120, 150)
plt.figure(figsize=(16,16))
plt.subplot(1,2,1)
plt.imshow(img,cmap='gray')
plt.title('Gray')
plt.subplot(1,2,2)
plt.imshow(canny_edges,cmap='gray')
plt.title("Canny_edges")
plt.xticks([])
plt.yticks([])
plt.show()

~~~


## Output:
## SOBEL EDGE DETECTOR
### SOBEL X:
![322561356-38a08663-8768-45ff-9010-62185266ee06](https://github.com/SdMdZahi7/EDGE-DETECTION/assets/94187572/b4b5b0f9-902d-41d4-a225-272bc53b33de)
### SOBEL Y:
![168266673-c39197fe-91bc-4f05-9552-f3944bbd3291](https://github.com/SdMdZahi7/EDGE-DETECTION/assets/94187572/2815592b-4043-4732-b783-45f87fc85397)
### SOBEL XY:
![168266699-03ec2f7a-f60c-4f35-84bf-5ae112ba3a33](https://github.com/SdMdZahi7/EDGE-DETECTION/assets/94187572/0a0df70a-0bc4-4ac5-8090-5d8e6a2b1a02)


## LAPLACIAN EDGE DETECTOR
![168266764-76cd8ffe-e403-4bf8-b9ba-db04fe71114c](https://github.com/SdMdZahi7/EDGE-DETECTION/assets/94187572/4aef82e0-0801-46d8-a7ff-3814035e45f0)



## CANNY EDGE DETECTOR

![168266795-8c9db5d8-90d2-42aa-917c-8ef147357cdb](https://github.com/SdMdZahi7/EDGE-DETECTION/assets/94187572/ea44ba5c-a43d-425e-a4ca-51f0981d326c)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
