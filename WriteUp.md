
**PID Control Project**

The goals / steps of this project are the following:
* Make a PID Controller. 
* Use the PID controller to control a car around a track.
* Test the the car in the simulator.
* Summarize the results with in a written report.

[//]: # (Image References)

[image1]: ./s1.png
[image2]: ./s2.png
[image3]: ./s3.png

## Rubric Points
### Here I will consider the [rubric points](https://review.udacity.com/#!/rubrics/1972/view) individually and describe how I addressed each point in my implementation.  

---
### Compilation

#### 1. Your code should compile.
My project includes the following files:
* main.cpp file which includes the code for generating the steering angle using the PID, and the code required for the interfacing with the simulator
* PID.h a header file for the PID controller.
* PID.cpp, the .cpp file for the PID controller.
* A reflection addressing how the project was implemented.

* The project compiles successfully with no errors.

### Implementation.
#### 2. The PID procedure follows what was taught in the lessons.
	
Yes, The PID algorithm is the same algorithm taught in the lectures.
The P (Proportional) component makes the car to steer to the lane center proportionally to the cross-track error.
The D (Differential) component steers the car based on the change of the cross-track error. 
The I (Integral) component steers the car based on the accumulated cross-track error. This counteracts the bias on the steering created by the vehicle itself or the curves on the track. 

#### 3. Describe how the final hyperparameters were chosen.
The hyperparameters were tuned manually by observing the car's behaviour. Then I added the throttle controller and re-tuned both controllers to make faster laps.

#### 4. Describe the effects of the P, I, and D components of the PID controller.
For a digital system, the proportional component decreases the error and drives the system towards minimizing the error between the desired set point and the measured process value -the current state-, but it causes oscillations in a digital system, and that's why we add the derevative component. The D component of the controller dampens the system behaviour and thus reduces oscillations and improves stability. We Also add the Integral component -That is the I component- to eleminate any system bias that could have been introduced to our system, Thus the PID (Proportional, Integral and Derevative) controller.

### Simulation
The vehicle successfully drives a lap around the track.

Here are some screenshots from the simulated lap

![alt text][image1]
![alt text][image2]
![alt text][image3]




