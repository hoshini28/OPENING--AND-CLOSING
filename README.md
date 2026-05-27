# IMPLEMENTATION-OF-OPENING-AND-CLOSING
## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
**Step-1:**

Import the necessary packages

**Step-2:**

Create the Text using cv2.putText

**Step-3:**

Create the structuring element

**Step-4:**

Use Opening operation

**Step-5:**

Use Closing Operation

 
## Program:
```
Developed by: Hoshini S
Reg.No: 2305003006
```

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Load the image using cv2.imread()
image = cv2.imread("Fish.jpg")  

# Step 2: Create a structuring element (5x5 rectangular)
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# Plot the original, opening, and closing images using Matplotlib
plt.figure(figsize=(10, 5))

plt.subplot(1, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

```

### Display the input Image:
<img width="504" height="407" alt="image" src="https://github.com/user-attachments/assets/78dcda97-e70c-4877-8789-c191e50bf1ca" />

<br>
```python
# Step 3: Use Opening operation (erosion followed by dilation)
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
opening_image_rgb = cv2.cvtColor(opening_image, cv2.COLOR_BGR2RGB)

plt.subplot(1, 3, 2)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```

### Display the result of Opening:
<img width="514" height="408" alt="image" src="https://github.com/user-attachments/assets/ced287dd-b688-4646-ae17-7415d1ba5cf0" />

<br>
```python
# Step 4: Use Closing operation (dilation followed by erosion)
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
# Convert images from BGR to RGB for Matplotlib
closing_image_rgb = cv2.cvtColor(closing_image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 3, 3)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")

plt.tight_layout()
plt.show()

```
### Display the result of Closing:
<img width="497" height="406" alt="image" src="https://github.com/user-attachments/assets/274ec559-c5a7-40d5-ae37-004afbdcfc44" />

<br>
## Result:
Thus,the Opening and Closing operation is used in the image using python and OpenCV.
