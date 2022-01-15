***Data structure***
numpy stores array in row-major order, that means the linear index of the element (i,j,k) of the 3d array of shape (2,3,4) is computed as follows
```l = (i*3 + j)*4 + k```
So, the data is laid out a long the plane yz first, then along the x direction. On the yz-plane, the data is laid out along the y-axis first then

***PIL for image processing***
from PIL import Image
arr = np.array of shape (x,y,3)
img = Image.fromarray(arr)
numpy has the method numpy.moveaxis(array, src, dst) which is very helpful.
