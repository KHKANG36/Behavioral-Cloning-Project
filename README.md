
# **Built the convolutional neural network(CNN) model end-to-end driving in a simulator, using TensorFlow and Keras**

This is a project for Udacity Self-Driving Car Nanodegree program. In this project I built the convolutional neural network(CNN) to drive in a simulator by cloning driving (steering) behavior, using TensorFlow and Keras. The CNN model is implemented in the file `Model_RyanKang.ipynb`. 

## Requirement 

- Python > 3.5.0
- OpenCV Library
- TensorFlow > 0.12 
- Keras
- GPU (if available)

## Run the Project 

To run this project, you have to download Udacity self-driving car simulator first from [here](https://classroom.udacity.com/nanodegrees/nd013/parts/fbf77062-5703-404e-b60c-95b78b2f3f9e/modules/6df7ae49-c61c-4bb2-a23e-6527e69209ec/lessons/46a70500-493e-4057-a78e-b3075933709d/concepts/1c9f7e68-3d2c-4313-9c8d-5a9ed42583dc). 
After driving a couple of laps at the training mode, you can get "driving_log.csv" file. Run the `Model_RyanKang.ipynb` on the ipython notebook, and it generate "model.h5" file. Run 
```
python drive.py model.h5
```
in the terminal. Run your simulator at the autonomous mode. You can see the self-driving car based on your training result. 

## About the Project 

In this project, I implemented the pipeline with below steps: 

1. Gathered first 2 laps on track of center lane driving.Below is an example of center camera image and sterring angle 
![Test image](https://github.com/KHKANG36/Behavioral-Cloning-Project/blob/master/mydata/Sample_image1.jpg)
2. Collected 1 more lap of smooth curving data in order to strengthen learning at curve road 
![Test image](https://github.com/KHKANG36/Behavioral-Cloning-Project/blob/master/mydata/Sample_image2.jpg)
3. Augment 3 times of data by using center/right/left camera. Correct fixed value (+-0.2) of steering angle for left/right camera image
![Test image](https://github.com/KHKANG36/Behavioral-Cloning-Project/blob/master/mydata/Sample_image3.jpg)
4. Implement convolutional neural network (CNN) model using 4 convolutional layers and 3 fully connected layers with dropout of 0.5
5. Train the driving behavior and test it on autonomous mode in simulator (The result video had been uploaded with project files)

More detailed explanation for the project is written on "Writeup_RyanKang.pdf" file. 

## Discussion/Issues 

1. Incorrect/poor driving behavior at difficult driving situation such as a lot of curve, narrow road..(You can see this "Track2" in simulator). We should come up with ideas to implement more robust model. 
