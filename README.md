# Eye Detection 

## Description
This project implements eye detection using the **integral image technique** . An optimized filter (kernel) is convolved over facial images to localize the eye region efficiently using summed-area tables.

## Features
- Computes the integral (summed area table) of a grayscale face image.
- Calculates the sum over any rectangular subregion using the integral image.
- Defines a custom kernel as per assignment (different weights/areas) to detect eye-like patterns.
- Slides the kernel over the image to compute a “response map” and select the region with the highest response.
- Extracts and visualizes the detected region for qualitative assessment.

## Main Functions
- `CalculateIntegral(image)`:  
Returns the integral image for efficient local sum calculation.
- `CalculateLocalSum(ii, p0, p1)`:  
Returns sum of pixels in a rectangular region using the integral image.
- `DetectEye(ii, kernel_width)`:  
Slides the custom kernel and returns the best-match eye location.
- `ExtractDetectedEye(image, location, kernel_width)`:  
Extracts and displays the region containing the eyes.



