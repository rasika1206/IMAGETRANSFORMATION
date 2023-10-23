# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.

### Step2:
Write a code to translation of the image.

### Step3:
Write a code for scaling of the image.

### Step4:
Write a code for shearing of the image.

### Step5:
Write a code for reflection of the image.

### Step6:
Write a code to rotation of the image.

### Step7:
Write a code to cropping of the image.

### Step8:
Display all the Transformed images.

## Program:
```python
Developed By:RASIKA.M
Register Number:212222230117
```
### i)Image Translation
```
import numpy as np
import matplotlib.pyplot as plt 
import cv2 as cv
```
### plotting of an image :
```
image = cv.imread("emily.jpg")
image = cv.cvtColor(image, cv.COLOR_BGR2RGB)

plt.axis("off")
plt.imshow(image)
plt.show()
```

### translation of an image :
```
rows,cols,dim = image.shape

M = np.float32([[1,0,100], [0,1,50],[0,0,1]])
translated_image= cv.warpPerspective(image, M, (cols, rows))

plt.axis("off")
plt.imshow(translated_image)
plt.show()
```

### ii) Image Scaling
```
rows,cols,dim = image.shape

M_scale = np.float32([[1,0,0], [0,1.5,0],[0,0,1]])
scale_image= cv.warpPerspective(image, M_scale, (cols, rows))

plt.axis("off")
plt.imshow(scale_image)
plt.show()
```


### iii)Image shearing
```
M_x = np.float32([[1,1,0], [0,1,0],[0,0,1]])

M_y = np.float32([[1,0,0], [0.4,1,0],[0,0,1]])

shear_imagex= cv.warpPerspective(image, M_x, (cols, rows))
shear_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(shear_imagex)
plt.show()

plt.axis("off")
plt.imshow(shear_imagey)
plt.show()

```


### iv)Image Reflection
```

M_x = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])

M_y = np.float32([[-1,0,cols], [0,1,0],[0,0,1]])

ref_imagex= cv.warpPerspective(image, M_x, (cols, rows))
ref_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(ref_imagex)
plt.show()

plt.axis("off")
plt.imshow(ref_imagey)
plt.show()
```



### v)Image Rotation
```

angle=np.radians(10)

matrix=np.float32([[np.cos(angle),-np.sin(angle),0],
                                [np.sin(angle),np.cos(angle),0],
                                [0,0,1]])

Rotated_image=cv.warpPerspective(image,matrix,(cols,rows))

plt.axis("off")
plt.imshow(Rotated_image)
```



### vi)Image Cropping
```

crop_img = image[150:600 ,350:900]

plt.axis("off")
plt.imshow(crop_img)
plt.show()




```
## Output:
### i)Image Translation
<br>![Screenshot from 2023-10-23 16-10-05](https://github.com/rasika1206/IMAGETRANSFORMATION/assets/124434806/c343e730-a7db-48bd-9d89-95c9ce89410a)


![Screenshot from 2023-10-23 16-10-14](https://github.com/rasika1206/IMAGETRANSFORMATION/assets/124434806/ee3f7ec8-9a3e-41de-917c-73f457934822)

<br>

<br>
<br>

### ii) Image Scaling
<br>


<br>![Screenshot from 2023-10-23 16-13-04](https://github.com/rasika1206/IMAGETRANSFORMATION/assets/124434806/266e7c8b-36fe-42fd-a036-3562a20ec2c2)

<br>
<br>


### iii)Image shearing
<br>

![Screenshot from 2023-10-23 16-14-50](https://github.com/rasika1206/IMAGETRANSFORMATION/assets/124434806/d89c2142-c7bd-4ce1-86b7-07feab32f149)

<br>

<br>
<br>


### iv)Image Reflection
<br>![Screenshot from 2023-10-23 16-15-41](https://github.com/rasika1206/IMAGETRANSFORMATION/assets/124434806/b00efad4-430a-4b83-b96a-27ffa4a793c1)



<br>

<br>
<br>



### v)Image Rotation
<br>![Screenshot from 2023-10-23 16-16-54](https://github.com/rasika1206/IMAGETRANSFORMATION/assets/124434806/4c9402a8-bb3a-4c6b-ab48-1710dd37f222)


<br>
<br>



### vi)Image Cropping

![Screenshot from 2023-10-23 16-20-03](https://github.com/rasika1206/IMAGETRANSFORMATION/assets/124434806/e1c5b597-422b-42da-8677-52984d7266d1)

<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
