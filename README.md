# Lens Wipe Edge/Object Detection
### The goal is to preprocess the images, apply edge detection filters, and use feature matching to identify and draw bounding boxes around the lens wipe object.

#
![image](https://github.com/EdmundCye/Edge-Detection/assets/111274518/570723a2-6d4e-43f7-8a86-583aa18e2932)

Image matching process using the ORB (Oriented FAST and Rotated BRIEF) algorithm employed in this project to detect the lens wipe object. After preprocessing the reference (cropped lens wipe) and target images, ORB detects and describes distinctive keypoints in both images. These descriptors are then matched between the reference and target images. If a sufficient number of matches are found above a set threshold, it indicates the presence of the lens wipe object in the target image, allowing a bounding box to be drawn around the detected object using the matched keypoint locations. This efficient feature detection, description, and matching pipeline, combined with preprocessing steps like resizing and Gaussian blurring, enables accurate and robust detection of the lens wipe across various target images.

## Output
![detected_lens_wipe_random1](https://github.com/EdmundCye/Edge-Detection_Python/assets/111274518/e0aabfe2-b955-4db2-91f4-7ddabcf0ebc3 | width=250) ![detected_lens_wipe_random2](https://github.com/EdmundCye/Edge-Detection_Python/assets/111274518/c896a3f9-27dd-4b91-89d7-041b0b61cde0 =250x250)


## Approach 
1. Image Acquisition: Capture images of the lens wipe object against a white background, both alone and alongside other random objects like watches, coins, and necklaces.
2. Preprocessing: Resize the images to a consistent size and apply Gaussian blurring to reduce noise.
3. Edge Detection: Evaluate different edge detection filters (Canny, Laplacian, Prewitt, and Sobel) to determine the most suitable one for accurately detecting the lens wipe's edges.
4. Feature Matching: Use the ORB (Oriented FAST and Rotated BRIEF) algorithm to match keypoints between the lens wipe object and the target images. If a sufficient number of matches is found, draw a bounding box around the detected lens wipe in the target image.

## Dataset
### The dataset(original folder) consists of the following images:
- lens_wipe.jpg: The main lens wipe object cropped from its original packaging.
- lens_wipe_random1.jpg: Lens wipe alongside a watch and a piece of cloth.
- lens_wipe_random2.jpg: Lens wipe with a coin and a cross necklace.
- random1.jpg: Only the watch and cloth, without the lens wipe.
- random2.jpg: Only the coin and cross necklace, without the lens wipe.
