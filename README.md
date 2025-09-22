# Image_Acqusition-_using_Web_Camera
# register number:212223240161
# name:subikshan p
## Aim:
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.

i) Write the frame as JPG 

ii) Display the video 

iii) Display the video by resizing the window

iv) Rotate and display the video

## Software Used:
Anaconda - Python 3.7

## Algorithm:
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
``` Python
### Developed By:Subikshan P
### Register No: 212223240161

## i) Write the frame as JPG file
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

## ii) Display the video
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

## iii) Display the video by resizing the window
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

## iv) Rotate and display the video
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

### i) Write the frame as JPG image
![nn](https://github.com/user-attachments/assets/e2956128-c946-4443-9753-3ae9b631edf6)


### ii) Display the video
![nn](https://github.com/user-attachments/assets/b2db8345-be1f-4b0f-8c0b-9663d202c9b0)


### iii) Display the video by resizing the window
![WIN_20250908_10_58_58_Pro](https://github.com/user-attachments/assets/5e86a451-da94-49fc-9993-b6b9dc2b15cb)

### iv) Rotate and display the video
<img width="433" height="907" alt="Screenshot 2025-09-08 105926" src="https://github.com/user-attachments/assets/3f9499bd-fc3d-42de-a2d4-37a05f034d82" />


## Result:
Thus the image is accessed from webcamera and displayed using openCV.
