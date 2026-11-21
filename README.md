# EXP. 9 – MORPHOLOGICAL OPERATIONS USING OPENCV

**NAME:** THARSHINI.M  
**REG NO:** 212224230287

## Aim

To implement morphological operations such as Erosion and Dilation using OpenCV and Python to study their effects on an image.

## Software Requirements

- Python
- Anaconda
- Jupyter Notebook
- OpenCV
- NumPy
- Matplotlib

## Morphological Operations

- Erosion
- Dilation

## Algorithm

1. Import the required libraries: OpenCV, NumPy, and Matplotlib.
2. Create a blank image of size 500 × 500 with three colour channels.
3. Add the text "Hello World" to the image using `cv2.putText()`.
4. Display the input image with text.
5. Create a 3 × 3 kernel using `np.ones()`.
6. Apply Erosion using `cv2.erode()` to shrink the foreground regions.
7. Display the eroded image.
8. Apply Dilation using `cv2.dilate()` to expand the foreground regions.
9. Display the dilated image.

## Implementation

### 1. Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### 2. Create a Blank Image

```python
image = np.zeros((500, 500, 3), dtype=np.uint8)
```

### 3. Add Text on the Image

```python
font = cv2.FONT_HERSHEY_SIMPLEX

cv2.putText(
    image,
    'Hello World',
    (100, 250),
    font,
    1,
    (255, 255, 255),
    2,
    cv2.LINE_AA
)
```

### 4. Display the Input Image

```python
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image with Text")
plt.axis('off')
```

**OUTPUT:**

<img width="287" height="303" alt="{9391245C-05FD-41A3-888F-D1D11EB4F2A7}" src="https://github.com/user-attachments/assets/2c67c935-d225-40c0-88b4-3a0d9cf1e5d9" />


### 5. Create a Kernel

```python
kernel = np.ones((3, 3), np.uint8)
```

### 6. Apply Erosion

```python
eroded_image = cv2.erode(image, kernel, iterations=1)

plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
```

**OUTPUT:**

<img width="283" height="307" alt="{256928DA-2F3A-412F-BDE7-02BBC13DF1DF}" src="https://github.com/user-attachments/assets/38900d89-d33c-40ab-867f-daf46abf3890" />


### 7. Apply Dilation

```python
dilated_image = cv2.dilate(image, kernel, iterations=1)

plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))
plt.title("Dilated Image")
plt.axis('off')
```

**OUTPUT:**

<img width="283" height="302" alt="{F4105232-85CD-430E-8CEA-B0E42D62C472}" src="https://github.com/user-attachments/assets/45d2e829-8900-4727-8084-12dd8487fd34" />


## Result

Thus, morphological operations such as Erosion and Dilation were successfully implemented using OpenCV and Python. Erosion reduces the foreground regions, whereas Dilation expands the foreground regions in the image.
