# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** Madhan M

**Register No:** 212225040213


## Output

### Original Image
```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("cricket.jpg")

if img is None:
    print("Error: Image not found. Check the file path.")
else:
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    plt.imshow(img_rgb)
    plt.title("Original Image")
    plt.axis("off")
    plt.show()
```
<img width="691" height="402" alt="Screenshot 2026-09-16 162936" src="https://github.com/user-attachments/assets/3d2a87dc-6241-43be-bad3-035c5ca91e7f" />



### ORIGINAL grayscale image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("cricket.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```
<img width="682" height="399" alt="Screenshot 2026-09-16 162943" src="https://github.com/user-attachments/assets/b9b8115b-8209-4e0c-b157-fc51597d6c99" />


### Global Thresholding

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("cricket.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```

<img width="671" height="419" alt="Screenshot 2026-09-16 162951" src="https://github.com/user-attachments/assets/883307a5-acec-43d7-afa6-7b394c9c31a8" />

### Adaptive Thresholding

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("cricket.jpg", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()
```
<img width="700" height="403" alt="Screenshot 2026-09-16 162957" src="https://github.com/user-attachments/assets/e28e9c57-8c81-4cbe-8426-8c19ee8a8fce" />


### Otsu's Thresholding

```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("cricket.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```
<img width="680" height="398" alt="Screenshot 2026-09-16 163819" src="https://github.com/user-attachments/assets/aaab884c-47df-41e7-b4b6-6b0580332328" />


### Original Grayscale Image

- The grayscale version of the input image is displayed.
- Serves as the input for thresholding operations.

### Global Thresholding

- Original image is displayed.
- Thresholded image is displayed.
- A fixed threshold value is used for segmentation.
- Pixels are classified as foreground or background.

### Adaptive Thresholding

- Original image is displayed.
- Adaptive Mean Thresholded image is displayed.
- Adaptive Gaussian Thresholded image is displayed.
- Threshold values vary across different regions of the image.
- Suitable for images with uneven illumination.

### Otsu's Thresholding

- Original image is displayed.
- Otsu segmented image is displayed.
- Optimal threshold value is calculated automatically.
- Produces improved segmentation for bimodal histograms.


## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
