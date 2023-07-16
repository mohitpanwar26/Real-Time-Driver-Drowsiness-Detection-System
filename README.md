# SOC_Project
Summer of code project on "Real Time Driver Drowsiness Detection System"

## Training and Testing using images and building model for prediction

1) Drowsiness Detection Dataset to train the model is downloaded from kaggle (https://www.kaggle.com/datasets/prasadvpatil/mrl-dataset)
2) Preprocessing the data is done like resizing images to 224x224 as our model architecture will require inputs of 224x224 size
3) MobileNet model is used and transfer learning is performed on it
4) Finalizing the model architecture and specifying the input and output, afterwhich compiling is done
5) Train the model on desired number of epochs and save it for future use
6) Test on few images where, prediction value for open eyes will be a negative value and for closed eyes it will be a positive value
7) Using the haarcascade model for eye detection afterwhich eyes are cropped and then applying our model to make predictions

## For real time detection and prediction

1) Take live video as input from webcam for prediction of closed eyes by running code from webcam_capture_prediction.ipynb
2) At first the face cascade and eye cascade models are loaded to detect face and eyes from the live video input through webcam
3) A rectangle box gets created around face and inside that, box for both eyes are also created
4) After which cbs parameter is set to 1 if eyes are detected otherwise 0
5) If cbs is 1 then eyes are cropped and prediction is done using model whether eyes are closed or open and will get displayed on the window frame
6) Press q to exit out of the window

