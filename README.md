# View Direction Prediction for 6DOF Immersive Content
- By Utkarsh Shekhar and Vishnuram Hariharan

## Overview:
We developed a model which is a hybrid of the LSTM and CNN architectures that can predict the gaze direction based on the past data of head rotation and body movement. Based on our results, we were able to replicate  and improve the results of the X. Hou, J. Zhang, M. Budagavi and S. Dey, "Head and Body Motion Prediction to Enable Mobile VR Experiences with Low Latency" research publication using Chakareski et all (2020) dataset which was collected using the same methodology on the same VR environment. While this doesn’t mean that our work outright overperforms Hou et all (2019) it does show promise. 

We also trained a Contextual Encoder-Decoder network which generated accurate visual saliency maps for the unseen VR dataset. For Future work, we could increase the generality of the gaze prediction model by adding saliency coordinates as part of the training process to better predict the gaze direction of the viewer. 


# Usage

## Visual Saliency Map Generation
Step 1: Clone repository from https://github.com/alexanderkroner/saliency 

Step 2: Train the network with salicon dataset (default)
>> python main.py train

Step 3: Test on Museum VR image data. This will generate visual saliency maps.
>> python main.py test -d salicon -p [virtualRealityImageDataPath]
  
