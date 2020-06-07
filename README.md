# Human-Face-Detector
Uses Deep Learning for multi-scale face detection and tracking. This algorithm is considered the predecessor to R-CNN and its variants, as it exhaustively searches the image space. 

To run: 
  1) Run FaceDetector.py to test it out with your computers webcam. It does not like bright lights. 

How it works:
  The general principal is to run a sliding window across the image, and pass each window into the neural net for face detection. This allows you to localize the faces by treating each window as a bounding box. It also allows for detecting any number of faces within the image.
  
  However, being able to detect a human face of varying size is a more complex problem (multi-scale detection). This is solved by constructing an image pyramid from the input frame, with a user configurable scale factor. A deeper pyramid allows for a tighter bounding box, at the cost of speed. 
  
 It is currently configured to for real-time detection without the use of your GPU. 

