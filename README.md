# IMAGE-TRANSFORMATIONS
# Developed By:Daniel C
# Reg no:212223240023

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.


### Step2:
Load the image file in the program.



### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.


### Step4:
Display the modified image output.


### Step5:
End the program.


## Program:
```python
Developed By:Daniel C
Register Number:212223240023
i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(in_img)
plt.show()


ii) Image Scaling
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1,0,50],
              [0,1,50],
              [0,0,1]])
trans_img=cv2.warpPerspective(in_img, M, (cols,rows))
plt.axis('off')
plt.imshow(trans_img)
plt.show() 


iii)Image shearing
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()


iv)Image Reflection

import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  



v)Image Rotation

import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("cat.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()



vi)Image Cropping

import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("cat.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[10:150 ,10:250]
plt.imshow(cropped_img)
plt.show()



```
## Output:
### i)Image Translation
<img width="775" height="437" alt="image" src="https://github.com/user-attachments/assets/e6764d92-3ee5-48e6-bc69-827edb62a84b" />

### ii) Image Scaling
<img width="772" height="438" alt="image" src="https://github.com/user-attachments/assets/f7860d4e-9935-4e1f-b8ce-3b7c2f4793b1" />



### iii)Image shearing
<img width="698" height="397" alt="image" src="https://github.com/user-attachments/assets/d24b8d32-5c2b-4f8a-9be9-22f2dc790342" />

<img width="692" height="397" alt="image" src="https://github.com/user-attachments/assets/27894024-6f09-40a3-b9cb-5302c0c70062" />


### iv)Image Reflection
<img width="686" height="396" alt="image" src="https://github.com/user-attachments/assets/39dea14e-a797-44b1-b4b9-b8704f312f2c" />

<img width="691" height="398" alt="image" src="https://github.com/user-attachments/assets/1bd36490-cf7a-46ea-947e-1d3aa63f1337" />



### v)Image Rotation
<img width="692" height="392" alt="image" src="https://github.com/user-attachments/assets/90a416ec-a228-4a7a-9951-b0e46ff7a177" />



### vi)Image Cropping
<img width="772" height="450" alt="image" src="https://github.com/user-attachments/assets/ceb2364f-ab7e-4451-b322-f00e443f89c3" />

<img width="785" height="487" alt="image" src="https://github.com/user-attachments/assets/58fa6ce9-3483-422a-aa54-e129ecb8d7e3" />



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
