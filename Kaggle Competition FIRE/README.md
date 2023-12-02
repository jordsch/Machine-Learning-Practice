# Overview
This folder contains the main code used in a previous team's project for Facial Recognition and Detection. The main notebook/implementation and the inputs/outputs can be found at this link https://www.kaggle.com/code/jordanchen1/t-4-facial-recognition-detection

This project used a previously trained Facial Recognition model which could only identify one person (given that they were in the center of the photo), and a Object Detection Model.

The objection detection model drew bounds around specific objects identifying them as cars, persons, etc.

The Facial Recognition model worked was that it had used a true dataset where Photos of people with their true name attached was used to train the model.

Our team combined both of these models to create a model that could take one photo of multiple people (without any facial location constraint), and attempt to identify every face found.
Our general approach was that we tweaked the object detection model to only focus on faces rather than many objects, and with the bounds of the faces we converted those bounds into data so that the Facial Recognition model could accept its input.
With each face inserted into the model, we outputted what the facial recognition model thought the person was per bounding box.
