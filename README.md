Autonomous Driving – Vision Project
Overview

This project implements a lane detection pipeline for autonomous driving using Python and OpenCV. It identifies lane lines from road images or videos, forming the basis for vision-based self-driving systems.

Features

Detects lane lines on roads.

Works on images and video.

Simple, efficient Python/OpenCV implementation.

Installation
pip install opencv-python numpy

Usage

Image:

import cv2
image = cv2.imread('test_road.jpg')
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
processed_image = detect_lanes(image)  # your lane detection function
cv2.imshow("Lane Detection", processed_image)
cv2.waitKey(0)
cv2.destroyAllWindows()


Video:

cap = cv2.VideoCapture('test_video.mp4')
while cap.isOpened():
    ret, frame = cap.read()
    if not ret: break
    processed_frame = detect_lanes(frame)
    cv2.imshow("Lane Detection", processed_frame)
    if cv2.waitKey(1) & 0xFF == ord('q'): break
cap.release()
cv2.destroyAllWindows()

Project Structure
images/          # Sample road images
videos/          # Sample videos
lane_detection.py # Main code
README.md        # Project description

Outcome

Detects lanes accurately for vision-based autonomous driving.

Can be extended to real-time video or AI decision-making systems.
