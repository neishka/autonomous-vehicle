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

OpenCV provide some really helpful built-in functions for the task on camera calibration. First of all, to detect the calibration pattern in the calibration images, we can use the function cv2.findChessboardCorners(image, pattern_size).

Once we have stored the correspondeces between 3D world and 2D image points for a bunch of images, we can proceed to actually calibrate the camera through cv2.calibrateCamera(). Among other things, this function returns both the camera matrix and the distortion coefficients, which we can use to undistort the frames.

The code for this steps can be found in calibration_utils.

We applied this distortion correction to the test image using the cv2.undistort() function and obtained the following result (appreciating the effect of calibration is easier on the borders of the image):

<img src="https://github.com/harrykarwasra/autonomous-vehicle/blob/master/images/calibration_after.jpg" width="300" height="250" description = "Chessboard image after calibration" />
