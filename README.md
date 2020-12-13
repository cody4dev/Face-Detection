# Face-Detection
Detect Faces in an image

STEP 1 :
Install OpenCV
````pip install opencv-python````

STEP 2 :
Download Haarcascade
Original Copy can be downloaded from the below website :
https://github.com/opencv/opencv/tree/master/data/haarcascades

STEP 3 :
Choose any image to detect faces

STEP 4 :
````
import cv2

face_cascade = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')

img = cv2.imread('image.jpg')

gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

faces = face_cascade.detectMultiScale(gray, 1.1, 4)

for (x, y, w, h) in faces:
    cv2.rectangle(img, (x, y), (x+w, y+h), (0, 0, 255), 2)

cv2.imshow('img', img)

cv2.waitKey()
````

run python file.py

