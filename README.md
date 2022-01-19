Image Stitching with OpenCV
This simple project showcases an OpenCV function that stitches multiple images together to create a panorama view. The tutorial link from which this is referred is linked here: 

Basically, how image stitching works is by detecting the keypoints and extracting the local invariant descriptors like SIFT. You can check out my Medium article here on SIFT or other feature descriptors.

Then, the descriptors are matched across images before a RANSAC algorithm estimates a homography matrix which a warping transformation uses to join the images together.

The goal of getting into image stitching is to explore and attempt methods to perform localization of objects using multiple cameras. This image stitching is considered a first step in that direction. 

Available scripts:
- image_stitching_simple.py
    - Description: This script attempts to take the images located in the '/park' folder and stitch them together. There have been cases where OpenCV is unable to stitch too many images and return a error code, hence the folder '/temp'. 