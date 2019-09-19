# Lane Detection

The goals / steps of this project are the following:

1. Compute the camera calibration matrix and distortion coefficients given a set of chessboard images.
2. Apply a distortion correction to raw images.
3. Use color transforms, gradients, etc., to create a thresholded binary image.

### 1. CAMERA CALIBRATION 

Why calibrate your camera?
After calibration, you can use your camera to do real world measurements. It establishes a relation between pixels and real world dimensions. Also, you can remove distortions caused by a camera's physical flaws. The goal of calibration is to estimate the following:

* Focal length of lens along X axis
* Focal length of lens along Y axis
* Lens displacement along X axis
* Lens displacement along Y axis
* 3 numbers that describe radial distortion
* 2 numbers that describe tangential distortion
* The position of the camera in the real world (x, y and z)

<img src="https://github.com/harrykarwasra/autonomous-vehicle/blob/master/images/calibration_after.jpg" width="300" height="250" description = "Chessboard image after calibration" />
