# Torch and Torchvision for Jetson Xavier NX on Python 3.10

If you own an NVIDIA Jetson Xavier NX by now you realised you are stuck with python 3.8. In fact, only from version 6 of the jetpacks is when you will see all the libraries adapted to work on python 3.10

Problem is that many of modern models that run on top of scikit-learn such as FastPitch require python 3.10, and the Torch and Torchvision they also require and which come with the jetpacks 5 are compiled for python 3.8

So, unless you want to buy a Jetson Orin, the only solution is to comnpile both torch and torchvision from source after of course having installed python 3.10 and created an environment to run them

Also, the compiled versions have to work with one another and torch has to be compiled with CUDA (otherwise you could just do a pip install torch)

So, after 2 weeks of painful testing I believe I got them right and I am giving them here. Note that torchvision throws an error "UserWarning: Failed to load image Python extension: '/usr/local/lib/python3.10/dist-packages/torchvision/image.so: undefined symbol: _ZNK3c1017SymbolicShapeMeta18init_is_contiguousEv'If you don't plan on using image functionality from `torchvision.io`, you can ignore this warning", but still seems to work ok. At one point I will try to recompile it better and update it here

hope it suits your purpose!

As the files are big and github has a limit of 25 Mb for files, I put them here:

1 - TORCH: https://www.tekntrash.com/github/torch-2.0.0a0+gite9ebda2-cp310-cp310-linux_aarch64.whl

2 - TORCHVISION: https://www.tekntrash.com/github/torchvision-0.16.1+fdea156-cp310-cp310-linux_aarch64.whl
