# SOC_Project
Summer of code project on "Real Time Driver Drowsiness Detection System"

## Training and Testing using images and building model for prediction
Run SOC_Project.ipynb file

1) Drowsiness Detection Dataset to train the model is downloaded from kaggle (https://www.kaggle.com/datasets/prasadvpatil/mrl-dataset)
2) Preprocessing the data is done like resizing images to 224x224 as our model architecture will require inputs of 224x224 size
3) MobileNet model is used and transfer learning is performed on it
4) Finalizing the model architecture and specifying the input and output, afterwhich compiling is done
5) Train the model on desired number of epochs and save it for future use
6) Test on few images where, prediction value for open eyes will be a negative value and for closed eyes it will be a positive value
7) Using the haarcascade model for eye detection afterwhich eyes are cropped and then applying our model to make predictions

## For real time detection and prediction
Run webcam_capture_prediction.ipynb file

1) Take live video as input from webcam for prediction of closed eyes by running code from webcam_capture_prediction.ipynb
2) At first the face cascade and eye cascade models are loaded to detect face and eyes from the live video input through webcam
3) A rectangle box gets created around face and inside that, box for both eyes are also created
4) After which cbs parameter is set to 1 if eyes are detected otherwise 0
5) If cbs is 1 then eyes are cropped and prediction is done using model whether eyes are closed or open and will get displayed on the window frame
6) Press q to exit out of the window

## Model Deployment using Flask
Run model.deploy.py file

1) This code is a Flask web application that uses a pre-trained deep learning model (that we have trained using SOC_Project.ipynb file)  and Haar Cascade classifiers to detect drowsiness in a driver's eyes in real-time.
2) It captures frames from the webcam, processes them to detect eyes, and then feeds the eye images to the pre-trained model for classification.
3) If closed eyes are detected with high confidence, it plays an alert sound to warn the driver.
4) The app runs on a local server and displays the webcam feed with real-time drowsiness detection.




https://github.com/mohitpanwar26/Real-Time-Driver-Drowsiness-Detection-System/assets/88027885/e97d6957-620a-461c-a76d-d9e6c68d55ad



https://github.com/mohitpanwar26/Real-Time-Driver-Drowsiness-Detection-System/assets/88027885/594478c1-79bc-4578-9d58-8ae1d8574335


