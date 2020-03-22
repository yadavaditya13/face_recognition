# face_recognition_with_OpenCV_Python_DeepLearning

This program basically recognizes faces in static images, video files and live cam... using encodings technique.

Requirements : 1) dlib and 2) face_recognition 
	

Note : I have places a few datasets for example in dataset folder and one example image in examples folder. Inorder to run the file use your own dataset and eample files and video files to test it as well. 

The structure of your project folder must look like : 
for example-

├── dataset
│   ├── person1 [no. of entries]
│   ├── person2 [no. of entries]
│   ├── person3 [no. of entries]
│   ├── person4 [no. of entries]
│   ├── person5 [no. of entries]
│   └── person6 [no. of entries]
├── examples
│   ├── example_01.png
│   ├── example_02.png
│   └── example_03.png
├── output
│   └── video1_output.avi
├── videos
│   └── video1.mp4
├── encode_faces.py
├── recognize_faces_image.py
├── recognize_faces_video.py
├── recognize_faces_video_file.py
└── encodings.pickle

encodings.pickle file will be created when you will run encode_faces.py file.

For datasets i used images of size 250x250 pixel value.

Refer to argparse documentation to understand how we use it. it is really helpful.

Note:
While running the file the way in which you muct write arguments in command line is as follows :
just for example-

1) Running encode_faces.py
=>	$ python encode_faces.py --dataset dataset --encodings encodings.pickle
 
2) Running recognize_faces_image.py
=>	$ python recognize_faces_image.py --encodings encodings.pickle --image examples/example_01.png

3) Running recognize_faces_video.py
=>	 python recognize_faces_video.py --encodings encodings.pickle
	--output output/webcam_face_recognition_output.avi --display 1

4) Running recognize_faces_video_file.py
=>	$ python recognize_faces_video_file.py --encodings encodings.pickle
	--input videos/video1.mp4 --output output/video1_output.avi
	--display 0
