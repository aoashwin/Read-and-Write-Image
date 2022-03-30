# READ AND WRITE AN IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.
i) Read, display, and write an image.
ii) Access the rows and columns in an image.
iii) Cut and paste a small portion of the image.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
## Program:
```
python
# Developed By: ASHWIN A O
# Register Number: 212220230005
# To Read,display the image

```
import cv2
pic=cv2.imread("mj.jpg",1)
cv2.imshow(pic)

cv2.waitKey(0)


# To write the image

cv2.imwrite("newimage.jpeg",pic)



# Find the shape of the Image

print(pic.shape)


# To access rows and columns

import random
for i in range(100):
    for j in range(pic.shape[1]):
        pic[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2.imshow(pic)
cv2.waitKey(0)

# To cut and paste portion of image

pic2=cv2.imread("mj.jpg",1)
pic2 = cv2.resize(pic2, (300, 430))
pic2[500:550,500:550]=[0,0,0]


cut= pic2[37:111,108:195]
pic2[0:74,0:87]=cut

cv2.imshow(pic2)








## Output:

### i) Read and display the image

<br>
![dip-ss](https://user-images.githubusercontent.com/75235601/160893838-c009e32d-a0b1-4d23-ae33-6ce5abc345c8.jpg)
<br>

### ii)Write the image

<br>
![dip-ss2](https://user-images.githubusercontent.com/75235601/160893786-6cd41f4c-b166-4dcd-bbc2-f62c6b44beac.jpg)
<br>

### iii)Shape of the Image

<br>
![dip-ss5](https://user-images.githubusercontent.com/75235601/160894096-7fd3a5c7-f1b3-4e6f-8922-c1b1ff1596e3.jpg)
<br>

### iv)Access rows and columns
<br>
![dip-ss3](https://user-images.githubusercontent.com/75235601/160894128-baaba772-979f-409a-b975-bbf1071fcfb4.jpg)
<br>

### v)Cut and paste portion of image
<br>
![dip-ss4](https://user-images.githubusercontent.com/75235601/160894163-5763409b-07af-42d1-920c-8f38574dc14d.jpg)
<br>

## Result:
Thus the images are read, displayed, and written successfully using the python program.

