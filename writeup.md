# Writeup: Sensor Fusion and Object Tracking

This is the project for the second course in the  [Udacity Self-Driving Car Engineer Nanodegree Program](https://www.udacity.com/course/c-plus-plus-nanodegree--nd213) : Sensor Fusion and Tracking. 

This final project of the second course is finished within the online-workspace VM.

The final project consists of four sections, as described in [project rubric](https://review.udacity.com/#!/rubrics/3006/view)

## Section 1: Implement an "EKF" to track a single real-world target
In this section, we a simple single-target-scenario to start, where there is only one vehicle to be tracked. 
![img1](images-final/step1_output2.png)


![img1](images-final/step1_output1.png)

Since the initial estimation is not well handled, the initial tracking error is relatively large.

Remark: since only lidar-data are used in this section, the extended Kalman filter is indeed equivalent to the classic Kalman filter.

## Section 2: Implement the track management, then initialize and activate it.

In this section, we deal with the track management including its initlization as well as the management of track state and track score.

## Section 3: Imlement a single nearest neighbor data association for multi-object tracking

In this step, the closest neighbor association is made to catch several different targets. 

![img1](images-final/step3_output1.png)


## Section 4: implement the non-linear observation model with camera and complete the sensor fusion module for camera-lidar fusion!

The core of this course, we use different sensors (lidar and camera) to complement the pros and cons of each sensor. To end this, we first implemented a nonlinear observation model for camera, that is the reason for using extended Kalman filter. Since each sensor typically has a different field of view, we introduced function `in_fov()` to figure out if some object can be identified by a camera theretically. This is a significantly critical topic, because it is related to the state of detected object.

The final results can be obtained as follows:

![img1](images-final/step4_output1.png)

![img1](images-final/step4_output2.png)


1. Write a short recap of the four tracking steps and what you implemented there (filter, track management, association, camera fusion). Which results did you achieve? Which part of the project was most difficult for you to complete, and why?



2. Do you see any benefits in camera-lidar fusion compared to lidar-only tracking (in theory and in your concrete results)?




3. Which challenges will a sensor fusion system face in real-life scenarios? Did you see any of these challenges in the project?



4. Can you think of ways to improve your tracking results in the future?



