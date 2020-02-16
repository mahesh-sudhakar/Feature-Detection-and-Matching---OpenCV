# Feature-Detection-and-Matching---OpenCV

Assignment 1 of grad course AER1515 - Perception for Robotics - UTIAS - University of Toronto.

This is a python notebook .ipynb file created on Colab, converted to a .py file.

The dataset is accessed by mounting the google drive. 
Please change the path of dataset accordingly in line 259.

Also change file paths for left, right images and to access calibration files in line 262 - 265, and 288.

Please see attached report for details on implementation of functions.

--------------

This project implements feature point detection and its matching between stereo pair images from KITTI
dataset. For a given input RGB image from left camera, the features which are described to be an image
region that is salient, local, repeatable, compact and efficient, are identified and studied by visual
inspection for unreliability on matching. As the features are detected in its corresponding right camera
image as well, we match the feature with a brute force matcher. For each match pair identified, the
disparity between the x values are calculated, and they are converted into depth values using the
predefined functions and calibration details provided. The calculated depth values are then documented
as a text file and attached for evaluation on test images. A RANSAC based outlier rejection method has
been implemented on the match pairs, and promising results have been noted. The method has been fine
tuned on train images by evaluating the results for corresponding changes to its confidence and
reprojection threshold values.
