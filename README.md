# Multi-Class Transportation and Object Detection

* In this experiment, the objective was to develop an object detection model using a dataset provided in COCO JSON format.
* The dataset included eight classes: 'vehicles', 'bicycle', 'bus', 'car', 'motorcycle', 'person', 'taxi', and 'truck'.
* The goal was twofold: to accurately detect objects within images using bounding boxes and to classify these objects into the correct categories.

# Steps and Challenges
**Data Loading and Preprocessing:**

I began by loading and preprocessing the data using custom functions [ parse_coco_json and CocoDataGenerator ]. These functions were responsible for parsing the COCO JSON files and extracting the necessary annotations to prepare the data for training.

**Data Augmentation:**
 
To improve the robustness of the model, I implemented data augmentation techniques, including Rotation, Color Jittering, and Horizontal Flip. These techniques were intended to help the model generalize better to unseen data.

**Model Architecture and Training:**

* I experimented with several pre-trained models, including ResNet50, CNN, and VGG. Although I initially considered using YOLO for object detection, an unfortunate incident occurred on August 14, 2024, after 6 PM in Syria,where the dataset was suddenly deleted from the site before I could finalize the YOLO model.


* During training, I encountered several challenges, particularly with the bounding box predictions. Despite adjusting various hyperparameters and loss functions, the models often produced bounding boxes that did not align correctly with the objects in the images.

**Evaluation:**

* The evaluation results indicated that the models were underfitting, as they struggled to learn the necessary patterns from the data. Despite trying different loss functions and metrics, the best model achieved the following results: 
* Precision: 0.4683
* Recall: 0.2057
* F1-Score: 0.1652
* These metrics suggest that the models were not able to effectively detect and classify objects. Upon reflection, I believe the core issue stemmed from the dataset itself, which I discovered too late when trying many training model processes.
