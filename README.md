# yoga_Pose_Detection_app
This is a Yoga Pose Estimation App which can be able to detect the yoga pose in real time by using posenet and KNN Classifier.  This project is done as a part of my internship in the role of Machine Learning Engineer Intern. This project can be extended to a perfect Yoga Trainer to track the poses and retain fitness using AI.

# This Project is mainly divided into 2 parts i.e frontend,backend part. Let's discuss each one of them in detail.

Frontend Part:- It mainly involves in collecting the image of the posture from front cam which is used for pose identification. This image is passed to posenet model which is pretrained in ml5.js and get the countor part locations x and y and save them for getting the data in form of json. We will be getting 17 poses detected from the image which has 2 values associated with it which will be in total 34 cordinates. Now once the data is converted we need to make use of pandas to convert to data frame and we need to train it with the KNN classifier and pickle it. The coordinates fro output is sent as request to flask app from ajax request.For getting the front cam i used p5.js.

Backend Part:- Now coming to backend part we used flask as a backend micro frame work to accept the request from front ed java script.Now we need to unpickle the model and predict with the request values which are in form of form values and predict the results and send the response to ajax there by we can get the pose identified.

Currently is is trained to identify only 3 poses. This model is getting 90.33 % accuracy.
