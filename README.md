# PedestrianDetection
VISION AND COGNITIVE SYSTEMS Final Projects (Powering up pedestrian segmentation with initial detection stage)
In this work, we have experimented in the field of Semantic Segmentation. The idea is to compare the standard
approach of semantic segmentation with a combination of
object detection and segmentation. Our method works by
feeding the input image into a fine-tuned object detection
model, extracting object crops, and feeding them into a segmentation model, the outputs of which are stitched together
to produce a full-resolution segmentation mask. We show
that this approach improves the quality of the segmentation
in some particular scenarios, but further experiments are
required to fully confirm the advantages of this approach.
