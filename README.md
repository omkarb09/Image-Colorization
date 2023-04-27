# Image Colorization using CNN

In image colorization, the goal is to produce a colored image given a grayscale input image.
This problem is challenging because it is multimodal -- a single grayscale image may correspond to many plausible colored images.
Deep neural networks have shown remarkable success in automatic image colorization (ability to capture semantic information.

## Dataset
I have used images from the Oxford IIIT pet dataset: https://www.kaggle.com/datasets/tanlikesmath/the-oxfordiiit-pet-dataset.
The Oxford-IIIT Pet Dataset is a 37 category pet dataset with roughly 200 images for each class created by the Visual Geometry Group at Oxford.
The model is trained on images of basset hound which is a subset from the above dataset.
Training images = 134, Validation images = 36, Test images = 30

## Methodology
![image](https://user-images.githubusercontent.com/44408619/234952539-31420723-65e7-40b5-aafb-64c5e8590dd0.png)
![image](https://user-images.githubusercontent.com/44408619/234952594-e235a01c-db91-4bfb-ae32-475e947d5893.png)

This approach uses lab color space. The aim is to infer a full-colored image, which has 3 values per pixel (lightness, saturation, and hue), from a grayscale image, which has only 1 value per pixel (lightness only). This project uses images of size 224 x 224, so our inputs are of size 224 x 224 x 1 (the lightness channel) and our outputs are of size 224 x 224 x 2 (the other two channels).

## Sample Outputs 
![2](https://user-images.githubusercontent.com/44408619/234937121-eec374ab-4f69-4043-b8b0-f3fa31b6989a.jpg)
![4](https://user-images.githubusercontent.com/44408619/234937147-ffced2ef-413f-4923-a267-3fe21a141ed7.jpg)
![6](https://user-images.githubusercontent.com/44408619/234937214-30843703-253e-4b22-b4a7-73a422a78daa.jpg)
