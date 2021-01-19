# Object-detection-accelerator-in-Xilinx-PYNQ-z2



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
* [Usage](#usage)
* [Algorithm](#algorithm)
* [References](#references)
* [Contributing](#contributing)
* [Contact](#contact)



## 1. OVERVIEW

Implementing the math function sqrt from the Linear Algebra Library 

## 2. SOFTWARE TOOLS AND SYSTEM REQUIREMENTS

Any Vivado HLS release from 2014.1 to 2016.1

## 3. DESIGN FILE HIERARCHY
```
	
	|   README.md
	\---code
			cordic_atan_11bits.h
		        cordic_defines.h
		    	cordic_isqrt.cpp
		    	cordic_sqrt.cpp
		    	float_sqrt.cpp
			test_main.cpp
    			top_magnitude.cpp
	\---code-opt
			cordic_atan_11bits.h
		        cordic_defines.h
		    	cordic_isqrt.cpp
		    	cordic_sqrt.cpp
		    	float_sqrt.cpp
			test_main.cpp
    			top_magnitude.cpp
	\---impl
			top_process_magnitude_csynth.rpt
	\---script
			script.tcl
			
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

<!-- References -->
## References

<!-- CONTRIBUTING -->
## Contributing

<!-- CONTACT -->
## Contact
