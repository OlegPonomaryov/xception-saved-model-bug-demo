## Issue desription
When building a model with a pretrained Xception net as base, than saving it in the Saved Model format, loading and running fit(), ResourceExhaustedError (out of memory) occurs. However, everything is alright when training the model without saving or if the Keras H5 format is used, which makes me think that there is actually enough GPU memory and this is indeed a bug.

## Additional info
The issue is demonstrated in the model.ipynb notebook. Replacing Xception with InceptionV3 solves the issue.

## System Information
- **OS Platform and Distribution:** Linux Ubuntu 18.04.4 64-bit
- **TensorFlow installed from:** pip
- **TensorFlow version:** 2.3.0-rc2 and 2.4.0-dev20200727
- **Python version:** 3.7.6
- **CUDA/cuDNN version:** CUDA 10.1, cuDNN 7.6.4.38
- **GPU model and memory:** RTX 2060 Super (8 GB)