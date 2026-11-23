Computer Vision Annotation Portfolio
Helia Salimi  
M.Sc. Student in Artificial Intelligence and Robotics | Shiraz University
Focus: Image Annotation · Computer Vision · YOLOv7 · Dataset Preparation · Python · PyTorch · OpenCV
Overview
This repository presents selected image annotation examples from my YOLOv7 object-detection project. It includes images, paired YOLO-format label files, and bounding-box previews. The examples show single-object annotation on clean backgrounds and a more challenging outdoor background.
The broader project considered five weapon categories:
Pistol
Rifle
Shotgun
Revolver
Machine Gun
Note: The original numeric class-ID mapping has not yet been recovered or verified. The list above identifies the categories, not their original IDs.
Selected annotation samples
1. Pistol — clean background
![Pistol annotation sample](previews/semi_auto_pistol_7_annotated.jpg)
Original image · YOLO label
2. Pistol — clean background
![Second pistol annotation sample](previews/semi_auto_pistol_10_annotated.jpg)
Original image · YOLO label
3. Shotgun — complex background
![Shotgun annotation sample](previews/shotgun_12_annotated.jpg)
Original image · YOLO label
The third sample includes extra background inside its bounding box and is a candidate for annotation quality review.
Annotation format
YOLO bounding-box labels use the format:
```text
class_id center_x center_y width height
```
The four spatial values are normalized to the range 0–1. Each provided image has a corresponding `.txt` file.
Important note on class IDs
The original supplied sample labels all used class ID `0`. For this showcase, the files were provisionally relabeled under an earlier three-class demonstration mapping:
`semi_auto_pistol_7.txt` → `0` (Pistol)
`semi_auto_pistol_10.txt` → `0` (Pistol)
`shotgun_12.txt` → `2` (Shotgun)
These are portfolio-specific provisional labels, not verified original five-class IDs. The current `classes.txt` and `data.yaml` in this repository also describe that earlier three-class example and should not be used as the original five-class training configuration.
The five-category taxonomy will be reflected in the dataset configuration and all annotation IDs only after the original class ordering is confirmed. These images show annotations, not model inference or proof of a trained five-class model.
Relevant skills
Image annotation and dataset preparation
Bounding-box inspection and annotation QA
LabelImg and YOLO-format labels
Python, PyTorch, OpenCV and YOLOv7
Repository structure
```text
images/       Source sample images
labels/       Paired YOLO-format annotation files
previews/     Images with annotation boxes visualized
classes.txt   Earlier provisional three-class example
data.yaml     Earlier provisional three-class example
README.md     Portfolio documentation
```
Project attribution
The annotated dataset work is presented as part of my project experience. YOLOv7 is an existing computer vision framework; this repository does not claim authorship of that framework. Images and annotations should be shared in accordance with any applicable source and licensing terms.
