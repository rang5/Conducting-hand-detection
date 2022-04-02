# CS 445 Final Project Music Conducting

## Description
This project uses hand detection to control the tempo of a song. Similar to that of a conductor, the location of the user's index finger is used to play a certain beat of a song. The beats are then adjusted to fit the timing of the user's hand movements. The end result is an audio and video file created resulting with the updated tempo. Pauses/stops in the music can be detected by holding up one's hand and doing a stop signal. Audio is added in after the recording of the video.

## Prerequisites
* [cv2](https://pypi.org/project/opencv-python/)
* [numpy](https://numpy.org/install/)
* [scipy](https://docs.scipy.org/doc/scipy/getting_started.html)
* [mediapipe](https://google.github.io/mediapipe/getting_started/python.html)
* [tensorflow](https://www.tensorflow.org/install)
* [librosa](https://librosa.org/doc/latest/install.html)
* [iPython](https://ipython.org/install.html)
* [sounddevice](https://python-sounddevice.readthedocs.io/en/0.4.3/installation.html)
* [ffmpeg](https://pypi.org/project/ffmpeg-python/)

## How to Use Project
* Run first cell with all imports
* In the next cell, choose audio file for song you want to use
* Can listen to the audio to check if the correct song used
* In the third cell, can listen to the beats combined with the song
* Run the cells until webcam
* Allow permission for webcam and adjust fps (third parameter) in output if want a more synchronized video
* Once webcam starts, video will be recording
* Move index finger to first center circle, then first beat starts
* Move index finger to left circle, then second beat starts
* Move index finger to right circle, then third beat starts
* Repeat for however long you want, with time between hitting checkpoints as the tempo
* The faster you get from one checkpoint to the next, the faster the tempo
* Can put a pause in the music by holding up a stop sign with your hand, the hand signal currently shown by the hand is shown in the lower right corner
* Press 'q' to exit and stop recording
* Run rest of cells to get the audio outcome of video
* Run last cell to get audio-video combination (may not align completely, have to adjust fps to webcam fps for better alignment)


Example outcome: https://drive.google.com/file/d/10t1t6ZnkWwJKX9Pqw5woElmFCtHlTr_a/view?usp=sharing 

## Folders
* audio is where the original audio files are held
* results stores some example outcomes of the code
* beatmaps stores the beatmaps generated from the audio files
* result_audio stores just the audio portion generated without the video

[Hand Detection](https://techvidvan.com/tutorials/hand-gesture-recognition-tensorflow-opencv/)
The following files are the original source code from techvidan: 
* TechVidvan-hand_gesture_detection.py
* mp_hand_gesture
* gesture.names
* data.pickle