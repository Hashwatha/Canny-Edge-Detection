# Canny-Edge-Detection
## PROGRAM:
```
import cv2
import matplotlib.pyplot as plt
# Load image in grayscale
image = cv2.imread('boy.jpeg', cv2.IMREAD_GRAYSCALE)
# Apply GaussianBlur to reduce noise
blurred = cv2.GaussianBlur(image, (5, 5), 1.4)
# Apply Canny edge detection
edges = cv2.Canny(blurred, threshold1=50, threshold2=150)
# Display results
plt.figure(figsize=(10,5))
plt.subplot(1,2,1)
plt.title("Original Grayscale Image")
plt.imshow(image, cmap='gray')
plt.axis('off')
plt.subplot(1,2,2)
plt.title("Canny Edge Detection")
plt.imshow(edges, cmap='gray')
plt.axis('off')
plt.show()

```

## OUTPUT:

![image](https://github.com/user-attachments/assets/8b696926-69e9-49ae-b3e5-198983bbd4a3)

# ii)
## PROGRAM :
import cv2
import matplotlib.pyplot as plt
# Load image in grayscale
image = cv2.imread('boy.jpg', cv2.IMREAD_GRAYSCALE)
# Apply GaussianBlur to reduce noise
blurred = cv2.GaussianBlur(image, (5, 5), 1.4)
# Apply Canny edge detection
edges = cv2.Canny(blurred, threshold1=50, threshold2=150)
# Display results
```
plt.figure(figsize=(10,5))
plt.subplot(1,2,1)
plt.title("Original Grayscale Image")
plt.imshow(image, cmap='gray')
plt.axis('off')
plt.subplot(1,2,2)
plt.title("Canny Edge Detection")
plt.imshow(edges, cmap='gray')
plt.axis('off')
plt.show()

```
## Discuss the Detected Edges

## Canny edge detection is a multi-stage algorithm that includes:

1. Noise reduction (Gaussian blur).
2. Gradient calculation using Sobel filters.
3. Non-maximum suppression to thin out edges.
4. Hysteresis thresholding using two thresholds to detect and link edges.
## Interpretation:

• Edges are detected where intensity changes rapidly.

• This helps in detecting object boundaries, corners, and outlines.

## iii) Impact of Parameter Settings
The two primary parameters for Canny:

• threshold1 (low threshold)

• threshold2 (high threshold)

## Effects of changing them:
## Threshold1 Threshold2 Result
Low Low Detects more edges including noise.
High High Detects fewer, more prominent edges.
Balanced Balanced Detects clean, well-defined edges.

