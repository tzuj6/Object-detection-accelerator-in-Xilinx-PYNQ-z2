# Object-detection-accelerator-in-Xilinx-PYNQ-z2



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
* [Usage](#usage)
* [Algorithm](#algorithm)
* [References](#references)
* [Contributing](#contributing)
* [Contact](#contact)



## OVERVIEW

Implementing the math function sqrt from the Linear Algebra Library 

## SOFTWARE TOOLS AND SYSTEM REQUIREMENTS

Any Vivado HLS release from 2014.1 to 2016.1

## DESIGN FILE HIERARCHY
```
	
	|   README.md
	\---Design IP
			cnn.cpp
			cnn.h
	\---testbench
			coco.names (item in coco dataset)
			main.cpp
			stb_image.h
			stb_image_write.h
			yolov2.cfg
			yolov2.h
	\---image
			kite.jpg (for test use)
			result.jpg
			
```
      


<!-- USAGE EXAMPLES -->
## Usage
* **build process**
  * For example, if you have a host program
  ```sh
  python FIRN11MAXI.py
  ```
  * If you implemented with vitis on U50
  ```sh
  make run
  ```

<!-- Algorithm -->
## Algorithm
YOLO v2 is trained on different architectures such as VGG-16 and GoogleNet. The paper also proposed an architecture called Darknet-19. The reason for choosing the Darknet architecture is its lower processing requirement than other architectures 5.58 FLOPS ( as compared to 30.69 FLOPS on VGG-16 for 224 * 224 image size and 8.52 FLOPS in customized GoogleNet). The structure of Darknet-19 is given below:

For detection purposes, we replace the last convolution layer of this architecture and instead add three 3 * 3 convolution layers every 1024 filters followed by 1 * 1 convolution with the number of outputs we need for detection.

For VOC we predict 5 boxes with 5 coordinates (tx, ty, tw, th, to (objectness score)) each with 20 classes per box. So total number of filters is 125.

![image1](https://github.com/tzuj6/Object-detection-accelerator-in-Xilinx-PYNQ-z2/blob/main/yolov2_net.png)

<!-- Result -->
## Result
![image1](https://github.com/tzuj6/Object-detection-accelerator-in-Xilinx-PYNQ-z2/blob/main/result.png)

<!-- References -->
## References
https://github.com/dhm2013724/yolov2_xilinx_fpga

<!-- CONTRIBUTING -->
## Contributing


## SUPPORT

For questions and to get help on this project or your own projects, visit the [Vivado HLS Forums][]. 

