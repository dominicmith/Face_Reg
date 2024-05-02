Face Recognition System 

- This repository contains Python code for a simple face recognition system using OpenCV. The system can detect and recognize faces in real-time from a webcam feed, as well as train on a dataset of images for recognizing specific individuals.

 Required Libraries

- OpenCV
- NumPy
- Pickle (for saving/loading label mappings)

 Installation Instructions

1. Install OpenCV:
   bash
   pip install opencv-python
   
2. Install NumPy:
   bash
   pip install numpy

Algorithms Used

- This face recognition system employs the following algorithms:

Haar Cascade Classifier:
-  Used for face detection. It is based on the Haar Wavelet technique and is capable of detecting faces in images or video frames.

LBPH (Local Binary Patterns Histograms) Face Recognizer:
-  Used for recognizing faces. LBPH is a popular method in face recognition that extracts local binary patterns from an image and computes histograms to represent the texture of the face.

Usage

Training the Face Recognizer

1. Place your training images inside the images directory. Organize the images into subdirectories where each subdirectory represents a person and contains images of that person.

Example structure:

images/
├── person1
│   ├── img1.jpg
│   ├── img2.jpg
│   └── ...
├── person2
│   ├── img1.jpg
│   ├── img2.jpg
│   └── ...
└── ...

2. Run the training script to train the face recognizer:

- python train.py

Real-time Face Recognition

1. After training, run the face recognition script:

- python recognize.py

2. The system will open your webcam and start recognizing faces in real-time. Press 'q' to quit.

Files

- train.py: Script to train the face recognizer using images in the images directory. It generates recognizer.yml and labels.pickle files.
- recognize.py: Script to perform real-time face recognition using the trained model. It loads the recognizer.yml and labels.pickle files.
- haarcascade_frontalface_default.xml: Haar cascade file for face detection.
- images/: Directory containing training images organized by person.
- recognizer.yml: Trained face recognizer model.
- labels.pickle: Pickle file containing label mappings.

References

- OpenCV documentation: https://docs.opencv.org - Official documentation for OpenCV library.
- LBPH Face Recognizer: Ahonen, Timo, Abdenour Hadid, and Matti Pietikäinen. "Face recognition with local binary patterns." Computer Vision-ECCV 2004. Springer, Berlin, Heidelberg, 2004. 469-481.
- Haar Cascade Classifier: Viola, Paul, and Michael J. Jones. "Rapid object detection using a boosted cascade of simple features." Computer Vision and Pattern Recognition, 2001. CVPR 2001. Proceedings of the 2001 IEEE Computer Society Conference on. Vol. 1. IEEE, 2001.
