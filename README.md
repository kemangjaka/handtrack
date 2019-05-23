# Hand Tracker
This repository contains code for performing foreground/background segmentation of the human hand in videos from an egocentric perspective, using pixel-level classification.  This project is based on [work by Cheng Li and Kris Kitani](http://www.cs.cmu.edu/~kkitani/datasets/), and described in the publication below: 

*Li, Cheng, and Kris M. Kitani. "Pixel-level hand detection in ego-centric videos." Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition. 2013. [(pdf)](http://www.cs.cmu.edu/~kkitani/pdf/LK-CVPR13.pdf)*

## Training Data
Using this app requires training data.  This project comes with sample training data, but you can create your own by labeling images using [Kitani's 'Labeling Tool'](http://www.cs.cmu.edu/~kkitani/perpix/code_grabcut/), which we have also ported to work with the latest Xcode IDE. You can find it [here](https://github.com/cmuartfab/grabcut).

## Dependencies
Library: OpenCV 2.4.x
OS: Ubuntu, Windows, Mac OS

## HOW TO
I modified the code to run with Webcam 
```
cd handtrack
mkdir build && cd build
cmake ..
make -j5
./Main $(webcam Index)
```

