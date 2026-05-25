# Implementation-of-Erosion-and-Dilation

## Aim
To perform erosion and dilation operations on a text image using Python and OpenCV.

---

## Software Required
- Anaconda – Python 3.7
- OpenCV
- NumPy
- Matplotlib

---

## Algorithm

### Step 1
Import the required libraries such as OpenCV, NumPy, and Matplotlib.

### Step 2
Create a text image using the `cv2.putText()` function.

### Step 3
Generate a structuring element for morphological operations.

### Step 4
Apply the erosion operation to the text image.

### Step 5
Apply the dilation operation and display the output images.

---

# Program

## Import the Necessary Packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline
```

## Create the Text using cv2.putText
```python
# Replace 'ABCDE' with your name (only the first 5 characters)

def load_img():

    blank_img = np.zeros((600,600))

    font = cv2.FONT_HERSHEY_SIMPLEX

    cv2.putText(blank_img,
                text='JAGAN',
                org=(50,300),
                fontFace=font,
                fontScale=5,
                color=(255,255,255),
                thickness=25,
                lineType=cv2.LINE_AA)

    return blank_img
```

## Display the Image
```python
def display_img(img):

    fig = plt.figure(figsize=(12,10))

    ax = fig.add_subplot(111)

    ax.imshow(img, cmap='gray')

    plt.show()
```

## Load and Display the Original Image
```python
img = load_img()

display_img(img)
```

## Create the Structuring Element
```python
kernel = np.ones((5,5), dtype=np.uint8)

kernel
```

## Erode the Image
```python
erosion1 = cv2.erode(img, kernel, iterations=1)

display_img(erosion1)
```

## Dilate the Image
```python
dilation1 = cv2.dilate(img, kernel, iterations=1)

display_img(dilation1)
```

---

# Output

## Original Image
<img width="847" height="812" alt="image" src="https://github.com/user-attachments/assets/fd9b2843-a55e-4d65-94a8-eb8955c6c0bd" />


## Eroded Image
<img width="862" height="821" alt="image" src="https://github.com/user-attachments/assets/94390a04-f5c7-4568-8121-d52418acc26c" />


## Dilated Image
<img width="815" height="796" alt="image" src="https://github.com/user-attachments/assets/9de0a6a7-f2a8-4125-b1f3-1d8e1684ddad" />

---

# Result
Thus, erosion and dilation operations were successfully performed on the generated text image using Python and OpenCV.

---
