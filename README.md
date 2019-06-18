# Self-Driving-Car
A self driving car with obstacle prevention and ambulance detection modules.

The car can perform the below mentioned functionalities:

1.) Detect obstacles in the front and avoid the crash.

2.) Detect ambulance in the surrounding with the help of image detection and audio detection.

I'll be discussing the image detection and obstacle avoidance aspect of the emergency vehicle detection(which was my role).

THEORY:

The aim of the project is to give path to the ambulance only in the emergency situations which would be detected with the help of audio detection i.e., siren detection of the ambulance.

The model used for image detection is Deep Convolutional Network. The images are fed into the model and with the help of trained parameters it will detect ambulance in the frame provided.

Requirements:

1.) Raspberry pi with raspbian os

2.) 4 wheels

3.) Motor Driver L298N

4.) Powerbank(source to powerup the raspberry pi)

5.) Battery(to power up the motor driver)

6.) Ultrasonic sensor HC-SR04

7.) Camera 

STEPS for Hardware Connections:

1.) Get the base ready to set up the different hardware parts on the car.

2.) Connect the 4 wheels of the car with the motor driver and connect the motor driver with the raspberry pi and the battery to power the motor which in turn rotate the wheels.

In order to achieve the second step refer to the link: https://www.youtube.com/watch?v=bNOlimnWZJE&t=1s

3.) Connect the ultrasonic sensor to the raspberry pi to detect obstacles in front of the car in a specified range of distance.

In order to complete the 3rd step refer to the link: https://www.youtube.com/watch?v=sXJjfEisjpo&t=157s

4.) Connect the raspberry pi with the camera like this: https://www.youtube.com/watch?v=xA9rzq5_GFM

5.) Connect the raspberry pi with a power bank or a power source.

STEPS for Software Configuration:

1.) Download the raspbian os from the raspberry pi official website: https://www.raspberrypi.org/downloads/
You can download Noobs if you want to get a easy installation process else raspbian os where you'll need to install it manually.

2.) Mount the os onto a sd card which would be inserted in the raspberry pi as the memory source.

3.) Once the sd card is loaded with the raspbian os, insert the sd card into the raspberry pi and load up the raspberry pi connecting it with a source. Refer this link: https://www.youtube.com/watch?v=jsi50bCo_W4

4.) You can connect the raspberry pi with a monitor or a television with the help of HDMI cable to see the operations(you can also use ssh and remotely operation).

5.) Set up the os.

6.) To ensure smooth functioning of the program, create a virtual environment otherwise the new library installation might get disturbed with the already installed libraries and dependencies. Refer : http://raspberrypi-aa.github.io/session4/venv.html

7.) Now download all the required libraries:
os, numpy, argparse, cv2, random, keras, matplotlib, sklearn, imutils.

8.) Create a python file in the virtual environment and copy the code from the file named train.py to that file.

9.) There will be a test file as well which would see the working of the model in real time. 

10.) The program from ultrasonic sensor would be referred from where the configuration has been applied with the raspberry pi.

11.) Only the test program needs to be present in the raspberry with the model trained in train file.

12.) Execute the test file in the virtual environment and the car would operate as expected.


POINTS TO BE TAKEN CARE OF:

1.) The code provided might not work because of the difference in the configuration in the pins of raspberry pi.

2.) Change the code as required.

3.) Save the trained model in the same location as the test file.

4.) Take care with the positive and negative connections with the battery.

5.) Change the range of obstacle in ultrasonic sensor program as required.

6.) The ultrasonic sensor can be used without a breadboard, directly connecting the sensor to the raspberry pi but it is adviced to use breadboard in order to prevent any damage because of high voltage to the sensor.

7.) Check the functioning of the camera attached.

P.S: I have added almost all the points which needs to be considered while building this car. Still if you face any issue, you can contact me anytime, would be happy to help.
