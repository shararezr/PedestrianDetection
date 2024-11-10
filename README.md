![Python](https://img.shields.io/badge/language-python-blue.svg)
![PyTorch](https://img.shields.io/badge/framework-PyTorch-orange.svg)

# PedestrianDetection
In this work, we have experimented in the field of Semantic Segmentation. The idea is to compare the standard
approach of semantic segmentation with a combination of
object detection and segmentation. Our method works by
feeding the input image into a fine-tuned object detection
model, extracting object crops, and feeding them into a segmentation model, the outputs of which are stitched together
to produce a full-resolution segmentation mask. We show
that this approach improves the quality of the segmentation
in some particular scenarios, but further experiments are
required to fully confirm the advantages of this approach.

# Abstract
This project explores advancements in the field of semantic segmentation. Specifically, we compare the traditional approach to semantic segmentation with an integrated method combining object detection and segmentation. Our method involves feeding an input image into a fine-tuned object detection model, extracting object crops, and passing them through a segmentation model. The outputs of the segmentation are then stitched together to create a full-resolution segmentation mask. Our experiments indicate that this hybrid approach can enhance segmentation performance in certain scenarios, although further testing and validation are necessary to fully assess its advantages.

1. Introduction
Pedestrian detection, particularly in crowded urban environments, is a challenging task in computer vision. The Pen-Fudan dataset serves as an important benchmark, pushing the boundaries of algorithms designed for crowded object detection. Our study focuses on improving pedestrian detection in complex urban settings, addressing issues such as occlusions, scale variations, and crowded scenes. This research is vital for applications such as urban planning, traffic management, and public safety, where reliable computer vision systems are essential.

We propose a tailored approach to the Pen-Fudan dataset, aiming to refine existing techniques and enhance the robustness of detection systems in real-world scenarios. By leveraging both object detection and segmentation, we explore ways to boost performance in pedestrian detection tasks.

2. Methodology
Our approach combines the strengths of object detection and semantic segmentation. First, an object detection model is fine-tuned on the Pen-Fudan dataset. The model's detections are then used to extract pedestrian regions from the input image. These cropped regions are subsequently fed into a segmentation model, which generates pixel-wise labels for the detected pedestrians. The outputs of these models are stitched together to create a full-resolution segmentation mask for the entire image. This method aims to improve segmentation accuracy by focusing computational resources on relevant regions, thus reducing false positives.

3. Results
Our experiments demonstrate that while smaller U-Net models perform well on the Pen-Fudan dataset due to the low-quality ground truth masks and the small size of the dataset, our combined detection-segmentation pipeline achieved slightly better quantitative results. By isolating pedestrian regions and reducing the false positives generated in background areas, this method can improve segmentation performance. However, this improvement comes with a performance penalty, and the method’s efficiency and effectiveness need further evaluation using larger datasets.

4. Conclusion
This study explored a hybrid approach to pedestrian segmentation by incorporating an initial detection stage. The integration of object detection into the segmentation pipeline proved to be beneficial in reducing false positives and improving segmentation accuracy in some cases. While the results on the Pen-Fudan dataset were promising, the small size of the dataset and the quality of ground truth masks limited the conclusions that could be drawn. Further research using different, larger datasets is required to validate the performance of this approach and assess its scalability.

We believe that this study lays the groundwork for future work in pedestrian detection and segmentation, particularly in complex urban environments. Further optimizations in both object detection and segmentation algorithms will enhance system performance and reliability in real-world applications.
