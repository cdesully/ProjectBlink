# ProjectBlink
Track blinking eyes for morse code character translation

Introduction:
This project is aimed at detecting eye blinking and being able to deliver Morse code messages. 

The project contains the following:

ProjectBlink.ipynb
	This entails the sum of research not included in the final result. It will show code attempted to integrate LSTM and Transformer Encoder modules for morse code prediction. It also contains video dataloaders attempted.

ProjectBlink_final.ipynb
	This contains the necessary notebook cells to produce the morse code blinking model.
	If opened on a device with a camera, the last code block with "inference_video" can be run to test results.
	This notebook file also has the logs showing training iterations and the corresponding statistics with a correlation chart visualizing how close embeddings relate to each other in the same category after training.

eyes_pack.zip
	This will contain the small dataset for open and shut eyes, the attempted video dataset for video training not utilized, the shape_predictor_68_face_landmarks.dat file for dlib to use. This is in a zip file to make it easier to upload to an environment such as Google Colab.
	
base_model_project.pt
	This file is for restoring weights to the model for convenience.

done.avi
	This is an example video made spelling the word done at the upper left of the frame.

Instructions:
	If necessary, install dlib into the python environment. 
	
	Run the notebook with the option of running cell 2 that unzips the eyes_pack.zip. If already unzipped then skip that cell.
	
	There is also the option to load an included saved weights file.
	
	Activate the last cell to enable cv2 to activate the device camera. Depending on personalized differences in blinking rate, adjust how quick a "dot" blink should be and how long to be considered done blinking for a letter with parameters dot_threshold and end_threshold respectively.
	
	Detection can be a little sensitive.