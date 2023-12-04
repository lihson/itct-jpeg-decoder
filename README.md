# 2023 ITCT Coding Assignment - JPEG Decoder
Author: 栗漢文  r11922191 

## Decode
* I have implement a baseline JPEG decoder for this assignment.
* I didn't use any external package except PTL and Numpy.
  1. PTL is used to output bmp.
  2. Numpy is used to accelerate DCT matrix multiplication. It is optional, default is True.
  3. When numpy is not used, decoding an image may take a while but still within 10 seconds.
  4. The code for performing DCT multiplication was referenced from https://github.com/yasoob/Baseline-JPEG-Decoder/ and I made some modification.
* Decode a jpeg file with numpy by the following script:
``` shell
python main.py /path/to/your/image use_numpy_or_not
```
For example:
``` shell
python main.py ./Image/teatime.jpg
Image height*width: 480 * 640
MCU height*width:  8 * 16
Save to ./Image/teatime.bmp
```
It will output a bmp file in the same directory with input image, e.g. ./Image/teatime.bmp

* If you want to disable numpy, excute the following script:
``` shell
python main.py ./Image/teatime.jpg false
```


