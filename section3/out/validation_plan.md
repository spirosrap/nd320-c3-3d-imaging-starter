# Validation Plan

## What is the intended use of the product?

The use of the product is to quickly identify the hippocampus volume , posterior and anterior and assist the doctors.

## How was the training data collected?

The training data was collected from various different subjects using MRI.

*We are using the "Hippocampus" dataset from the Medical Decathlon competition. This dataset is stored as a collection of NIFTI files, with one file per volume, and one file per corresponding segmentation mask. The original images here are T2 MRI scans of the full brain. As noted, in this dataset we are using cropped volumes where only the region around the hippocampus has been cut out. This makes the size of our dataset quite a bit smaller, our machine learning problem a bit simpler and allows us to have reasonable training times. You should not think of it as "toy" problem, though.*

Target: Hippocampus head and body
Modality: Mono-modal MRI 
Size: 394 3D volumes (263 Training + 131 Testing)
Source: Vanderbilt University Medical Center

Part of the Medical Segmentation Decathlon dataset http://medicaldecathlon.com/index.html


## How did you label your training data?

According to http://medicaldecathlon.com/index.html:

*All data has been labeled and verified by an expert human rater, and with the best effort to mimic the accuracy required for clinical use.*

## How was the training performance of the algorithm measured and how is the real-world performance going to be estimated?

The performance was measured using the Jaccard distance and dice distance from the labels. Τhe real-world performance will be measured when doctors use the system in a controled environment. 


## What data will the algorithm perform well in the real world and what data it might not perform well on?

The data will perform well in reasonable images of human brains with a clear view of the hippocambus. If the hippocambus isn't clear the algorithm will not perform well.

