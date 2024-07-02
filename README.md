# Torch and Torchvision for Jetson Xavier NX on Python 3.10

If you own an NVIDIA Jetson Xavier NX by now you realised you are stuck with python 3.8. In fact, only from version 6 of the jetpacks is when you will see all the libraries adapted to work on python 3.10

Problem is that many of modern models that run on top of scikit-learn such as FastPitch require python 3.10, and the Torch and Torchvision they also require do not accept 
