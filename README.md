
# Camera Calibration - Robot Perception

This project contains a Python implementation for camera calibration using a planar chessboard pattern. It was developed as an assignment for the Robot Perception course in the Computational Modeling postgraduate program at FURG.

## Overview
The main goal of this script is to estimate the intrinsic parameters and distortion coefficients of a standard smartphone camera. By analyzing multiple images of a chessboard taken from various angles, the algorithm models the camera's optical properties and corrects lens deformations.

## Features
- **Corner Detection:** Automatically detects internal chessboard corners across a dataset of images.
- **Calibration Parameters:** Computes the camera's intrinsic matrix (focal lengths and optical center) and distortion coefficients (radial and tangential).
- **Reprojection Error:** Calculates the Root Mean Square (RMS) error to evaluate the accuracy of the estimated model.
- **Image Undistortion:** Applies the mathematical model to rectify the original images, removing the "barrel" or "pincushion" lens effects.

## Results
- **Dataset:** 20 pictures taken, 18 successfully processed.
- **RMS Reprojection Error:** ~1.22 pixels.
- **Conclusion:** The calibration successfully mitigated radial distortion, rendering the lines in the environment perfectly straight in the undistorted output.

## Technologies Used
- Python
- OpenCV
- NumPy
- Matplotlib
- Google Colab

## How to Run
1. Update the grid size according to your printed chessboard.
2. Provide the path to the directory/drive containing your calibration images.
3. Run the script to extract the parameters and generate the corrected images.
