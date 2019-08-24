# FACE RECOGNITION USING OPENCV

## GETTING STARTED

In this project we can able to know how we can able to train a model for face recognition.If you are not installed an opencv try to install it with this link :https://github.com/Karthikeyan-alp/OpenCV-PI-Installation

## PREREQUISITES
   - Raspberry pi 3/3B+/4
   - Proper Internet connections
   - Raspbian stretch os
  
## DOWNLOADING

   You need a Haarcascades for developing the face detection.so Install the cascades file from this link
   https://github.com/opencv/opencv/tree/master/data/haarcascades 
   
   
  Check the folder ,If haarcascades is available Neglect the upcoming steps
  
  Home >> pi >> opencv-3.3.0 >> data >> haarcascades >> Xml files
  
  ### IF NOT AVAILALE IN ABOVE PATH 
   
   Download it by giving the command in Terminal like
    
            cd
            
            cd opencv-3.3.0
            
            cd data
            
            mkdir haarcascades
            
            cd haarcascades
            
            wget (** Right click on the haarcascdes.xml file and copy the path from browser and paste it and hit Enter **)
            
            
  ## CHECKING HAARCASCADES
  
   Now we are going to check the Haarcascades with some code.Now open the python idle and type the following code from https://github.com/Karthikeyan-alp/FaceRecognition/blob/master/face.py
   After finish the coding save it and open the Terminal window.type the following code to run the file.
   
             cd 
             
             source ~/.profile
             
             workon cv
             
             python3 face.py
             
   It will open the camera and put the box around our face.press ESC to stop the live video.
   
   ## GETTING IMAGES FOR TRAINING
   
   In this step we are getting the images for Training our model
   
   Now create a Directories by Entering the Following commands
   
               cd
               
               mkdir Facedetection
               
               cd Facedetection
               
               mkdir capturing
               
               mkdir training
               
   After this run the following code in Python Idle  to Train a Image for facial Recogntion(capturing.py).
   https://github.com/Karthikeyan-alp/FaceRecognition/blob/master/capturing.py
   
   Save the file as capturing.py and open the Terminal and write the following command.
   
             cd 
             
             source ~/.profile
             
             workon cv
             
             python3 capturing.py
             
  This command will save the photo at capturing folder in Grayscale format.If you want to train more person run the same code by giving different user Id.
  
 ## TRAINING AN IMAGES FOR PROCESSING
 
 In this step we are going to create a yml file for Facial Detection.This file is produced by using the Negative images stored in the capturing folder.
 
You can get the file(training.py) https://github.com/Karthikeyan-alp/FaceRecognition/blob/master/training.py

 Save the file as training.py and open the Terminal and write the following command.
   
             cd 
             
             source ~/.profile
             
             workon cv
             
             python3 training.py
             
  After this execution you can find the yml file in training directory.
   
   
