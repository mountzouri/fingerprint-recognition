# Fingerprint Recognition
This project was created for the Master of Artificial Intelligence, KU Leuven. It is related to a school project of the Master Course entitled: Biometrics System Concepts.
In this project, biometric systems in verification setting are validated by using actual fingerprint similarity scores of the left and right index finger.
Different fingerprint recognition systems are implemented and evaluated in three databases provided.

## Overview
The basis FPR matching is based on matching keypoints, called minutiae. 
They are defined as the ridge endings and bifurcations and can be easily determined by first thresholding and skeletonizing/thinning the fingerprint image.  

In order to detect the matching keypoints in the authentication/verification scenario, feature detection and description is implemented using ORB, SIFT and SURF, 
while homography transformation is presented as well and used properly for this reason. 

In each case, different matching methods are used: 
* The first matching method uses as a criterion the sum of matches between two fingerpints; the more the matches, the better it is. 
* The second matching method uses as a criterion the matching distance between the best matching keypoints; it calculates the matching distances between the best matching 
keypoints of two fingerprints (a proportion of the total matching keypoints is used), and keeps the median one. 
* The third matching method calculates the matching distances between the best matching keypoints of two fingerprints 
(a proportion of the total matching keypoints is used again), and keeps the average value. In general, the less the distance the better it is. 

Also, as an extra scenario, homography transformation is applied to the images, and then ORB algorithm is used again, to detect the matching keypoints between the initial images 
and the aligned ones and then the sum of the matches is calculated. Those images with more matches are supoosed to match better.

