# Image-Acquisition-using-Web-Camera

## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used

Anaconda - Python 3.7

## Algorithm

### Step 1:
Use cv2.VideoCapture(0) to access web camera.

### Step 2:
Use cv2.imread to read the video or image.

### Step 3:
Use cv2.imwrite to save the image.

### Step 4:
Use cv2.imshow to show the video.

### Step 5:
End the program and close the output video window by pressing 'q'.

## Program:

### Developed By:MOENISH BAALAN G
### Register No:212223220057

## i) Write the frame as JPG file:

```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
captured_image = cv2.imread('captured_frame.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()
```

## ii) Display the video:

```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()

```

## iii) Display the video by resizing the window:

```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```

## iv) Rotate and display the video:

```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```

## Output:

### i) Write the frame as JPG image:

<img width="636" height="510" alt="image" src="https://github.com/user-attachments/assets/95287761-986d-4485-bab4-a40b4c865a89" />

### ii) Display the video:

<img width="617" height="470" alt="image" src="https://github.com/user-attachments/assets/69285b97-b8b2-4af0-a86d-3fd1226eb1a1" />


### iii) Display the video by resizing the window:

<img width="307" height="465" alt="image" src="https://github.com/user-attachments/assets/3b8c72fd-4ef3-43d8-aba2-8b5c5a33d6c8" />

### iv) Rotate and display the video:

<img width="345" height="460" alt="image" src="https://github.com/user-attachments/assets/6b748908-fc56-426f-af4a-b3b74b81ecba" />


## Result:
Thus the image is accessed from webcamera and displayed using openCV.
