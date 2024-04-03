# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image using a function warpPerpective()

### Step3:
Scale the image by multiplying the rows and columns with a float value.

### Step4:

Shear the image in both the rows and columns.

### Step5:

Find the reflection of the image.
### Step6:

Rotate the image using angle function.
## Program:
```
Developed By: Karnan K
Register Number:212222230062
```
### i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("book.jpeg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

### ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("obj.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```


### iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("obj.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```



### iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("obj.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```




### v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("obj.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```


### vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("obj.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation
![image](https://github.com/karnankasinathan/IMAGE-TRANSFORMATIONS/assets/118787064/9117e6c6-4a67-4d77-9025-e79fcd978470)
### ii) Image Scaling
![image](https://github.com/karnankasinathan/IMAGE-TRANSFORMATIONS/assets/118787064/dcd25e11-2aba-45d4-9e0c-7ec5a0450413)


### iii)Image shearing
![image](https://github.com/karnankasinathan/IMAGE-TRANSFORMATIONS/assets/118787064/ad5ad1b1-577f-4d7c-90a1-d977f5b23932)

### iv)Image Reflection

![image](https://github.com/karnankasinathan/IMAGE-TRANSFORMATIONS/assets/118787064/0fb5281c-d0e5-4d2f-b662-5cb0873e0226)


### v)Image Rotation
![image](https://github.com/karnankasinathan/IMAGE-TRANSFORMATIONS/assets/118787064/92b69315-cc3b-4a23-92d3-978c68ef7902)


### vi)Image Cropping

![image](https://github.com/karnankasinathan/IMAGE-TRANSFORMATIONS/assets/118787064/2c87999a-7e75-42c4-ad61-88024d563c00)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
