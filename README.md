# Opencv-Gesture-Recognizer
Opencv-Gesture-Recognizer

![Screenshot software](https://github.com/credo92/Opencv-Gesture-Recognizer/blob/master/sample.png "screenshot software")

Many common image operations are performed using Region of Interest in OpenCV. A ROI allows us to operate on a rectangular subset of the image. The typical series of steps to use ROI is: create a ROI on the image, perform the operation you want on this subregion of the image, reset back the ROI

Convert to gray scale :

Why ? https://stackoverflow.com/questions/42867928/why-convert-to-grayscale-opencv

Image Blurring (Image Smoothing)
Image blurring is achieved by convolving the image with a low-pass filter kernel. It is useful for removing noises. It actually removes high frequency content (eg: noise, edges) from the image. So edges are blurred a little bit in this operation.

Thresholding
In image processing, thresholding is used to split an image into smaller segments, or junks, using at least one color or gray scale value to define their boundary. The advantage of obtaining first a binary image is that it reduces the complexityof the data and simplifies the process of recognition and classification.



https://www.quora.com/Why-is-thresholding-used-in-image-processing


Contours
What are contours?
Contours can be explained simply as a curve joining all the continuous points (along the boundary), having same color or intensity. The contours are a useful tool for shape analysis and object detection and recognition.

For better accuracy, use binary images. So before finding contours, apply threshold or canny edge detection.

In OpenCV, finding contours is like finding white object from black background. So remember, object to be found should be white and background should be black.

How to draw the contours?
To draw the contours, cv2.drawContours function is used. It can also be used to draw any shape provided you have its boundary points. Its first argument is source image, second argument is the contours which should be passed as a Python list, third argument is index of contours (useful when drawing individual contour. To draw all contours, pass -1) and remaining arguments are color, thickness etc.

Finding Convex Hull

The Convex Hull of a convex object is simply its boundary.
This can be done using convexHull function.




