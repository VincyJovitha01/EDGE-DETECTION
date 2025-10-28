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

### Program : 

## Name: VINCY JOVITHA V
## register number: 212223230242

(i) Display the original image
```
import cv2
import matplotlib.pyplot as plt
# Load the image
image = cv2.imread("rose.jpg")  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Display Original Image
plt.imshow(cv2.cvtColor(gray_image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
plt.show()
```
(ii) Apply Sobel Edge Detection
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
# Display Sobel Edge Detection
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
plt.show()
```
(iii) Apply Laplacian Edge Detection
```
# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
# Display Laplacian Edge Detection
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
plt.show()
```
(iv) Apply Canny Edge Detection
```
canny_edges = cv2.Canny(gray_image, 50, 150)
# Display Canny Edge Detection
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
plt.show()
```

## Output:
### ORIGINAL IMAGE

<img width="693" height="460" alt="image" src="https://github.com/user-attachments/assets/0386503b-1ec4-4b46-a703-421600bf6551" />

### SOBEL EDGE DETECTOR

<img width="681" height="473" alt="image" src="https://github.com/user-attachments/assets/670b7243-4638-4bcb-8895-644ad76c2dc4" />

### LAPLACIAN EDGE DETECTOR

<img width="686" height="467" alt="image" src="https://github.com/user-attachments/assets/76f408ab-90e3-4bd1-9798-da41188baa6d" />

### CANNY EDGE DETECTOR

<img width="652" height="466" alt="image" src="https://github.com/user-attachments/assets/0696ee01-b246-42da-886c-e1d126bf738d" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
