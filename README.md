# Face Detection Lock

Face Detection Lock is a Python program for detecting, recognizing and authenticating faces. The result of the authentication is displayed on a 16x2 LCD Screen. The code is a custom implementation on the code by [Adrian Rosebrock](https://github.com/jrosebr1) found in https://www.pyimagesearch.com/2018/09/24/opencv-face-recognition/

<p align="center">
  <img src="./images/img_authorized_lcd.png" alt="Image Authorized" width="400">
  <img src="./images/img_unauthorized_lcd.png" alt="Image Unauthorized" width="500">
</p>

### Dependencies
You need to install the following dependencies to get the project running
* opencv-python
* imutils
* smbus
* numpy

### Starting the project
The project depends on the [lcddriver](www.example.com) repository for displaying the detected names on a screen. After pulling the repository, use the following commands
* `cd FaceDetectionLock/`
* `git submodule init`
* `git submodule update`

Next, make sure you go to `lcd/lcddriver.py` and change the following lines
* `import i2c_lib` -> `from lcd import i2c_lib`
* `ADDRESS = ` to the address for your 16x2 LCD 

### Launch Commands:
* Exctract the embeddings:
`python3 extract_embeddings.py --dataset dataset --embeddings output/embeddings.pickle \
	--detector face_detection_model --embedding-model openface_nn4.small2.v1.t7`
* Train the model:
`python3 train_model.py --embeddings output/embeddings.pickle \
	--recognizer output/recognizer.pickle --le output/le.pickle`
* Launch the program:
`python3 recognize_video.py --detector face_detection_model \
	--embedding-model openface_nn4.small2.v1.t7 \
	--recognizer output/recognizer.pickle --le output/le.pickle`

## Future Plans for Development
* Connect an NFC tag as a second way of authentication

## Thank you
* Thanks to [Adrian Rosebrock](https://github.com/jrosebr1)
