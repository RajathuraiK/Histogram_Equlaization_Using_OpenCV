# Histogram_Equlaization_Using_OpenCV

---

## Aim
Display original color image, histogram, enhanced image, and enhanced histogram.

---

## Program
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
img = cv2.imread('racoon.jpg',cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap='gray')
plt.title('original_image')
plt.show()

plt.hist(img.ravel(),256,range = [0, 256]);
plt.title('Original Image')
plt.show()

img_eq = cv2.equalizeHist(img)
plt.hist(img_eq.ravel(), 256, range = [0, 256]); 
plt.title('Equalized Histogram')

plt.imshow(img_eq, cmap='gray')
plt.title('original image')
plt.show()

img = cv2.imread('racoon.jpg', cv2.IMREAD_COLOR)
img_hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
img_hsv[:,:,2] = cv2.equalizeHist(img_hsv[:, :, 2])
img_eq = cv2.cvtColor(img_hsv, cv2.COLOR_HSV2BGR)
plt.subplot(121); plt.imshow(img[:, :, ::-1]); plt.title('Original Color Image')
plt.subplot(122); plt.imshow(img_eq[:, :, ::-1]); plt.title('Equalized Image')

plt.figure(figsize = [12,10])
plt.subplot(221); plt.imshow(img[:, :, ::-1]); plt.title('Original Color Image')
plt.subplot(222); plt.imshow(img_eq[:, :, ::-1]); plt.title('Equalized Image')
plt.subplot(223); plt.hist(img.ravel(),256,range = [0, 256]); plt.title('Original Image')
plt.subplot(224); plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized')

```

### Developed By:
**Name:** Rajathurai K
**Register No:** 212225100036

##  Output

### ORIGINAL IMAGE:

![original image](<racoon.jpg>)

### Grayscale Histogram Equalization

![output-01](<output-01.png>)

### Color Image Equalization

![output-02](<output-02.png>)



Histogram Equalization of Grayscale Image:

<img width="1106" height="808" alt="image" src="https://github.com/user-attachments/assets/064ad82a-3630-4530-93d5-2a2395055c5f" />

---

## Result

Footer
© 2026 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Community
Docs
Contact
Manage cookies
Do not share my personal information
