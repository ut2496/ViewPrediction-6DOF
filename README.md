# View Direction Prediction for 6DOF Immersive Content
- By Utkarsh Shekhar and Vishnuram Hariharan

## Overview:
We developed a model which is a hybrid of the LSTM and CNN architectures that can predict the gaze direction based on the past data of head rotation and body movement. 
We also trained a Contextual Encoder-Decoder network which generated accurate visual saliency maps for the unseen VR dataset. For Future work, we could increase the generality of the gaze prediction model by adding saliency coordinates as part of the training process to better predict the gaze direction of the viewer. 


# Usage
## LSTM Model
Step 1 : The model and data can be run as is, you just need jupyter installed

Step 2 : All the plots are stored in the results folder separated out in directories by their session numbers.


## Visual Saliency Map Generation
Step 1: Clone repository from https://github.com/alexanderkroner/saliency 

Step 2: Train the network with salicon dataset (default)
>> python main.py train

Step 3: Test on Museum VR image data. This will generate visual saliency maps.
>> python main.py test -d salicon -p [virtualRealityImageDataPath]
  
## Dataset Acknowledgement 
"M. Khan and J. Chakareski. NJIT 6DOF VR Navigation Dataset. 2020. https://www.jakov.org.",
