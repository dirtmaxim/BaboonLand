---
layout: default
permalink: /
title: ""
---

![](assets/images/introduction.jpg)

---

### **Overview**

BaboonLand is a dataset comprised of 21 consecutive days of drone video footage collected by following three troops of wild Olive baboons in Laikipia, Northern Kenya as they left and returned from known sleeping sites, morning and night. Over 10 hours of video footage were collected in several different environments, including at a sleeping tree, at a river, on a rock, during a river crossing, in an open savannah, and on a cliff. Frames include up to 70 individuals tracked simultaneously, which forms a complex and dense dataset of overlapping individuals from an aerial perspective. Three fundamental subtasks have been identified from the original dataset: detection, tracking, and behavior recognition. The data contains lots of visual noise from camera motion, varying light conditions, spectral contrast from shadow, and different background environments.

This is the first dataset to automate the classification of primate behavior from aerial video. This enables inter-group interactions to be understood in context to the natural environment and in relation to the behavior of other troop members. Existing video datasets of primates are from camera traps or hand-held video recorders, which limits the number of individuals that can be seen in a frame at once and the spatial and temporal window in which behavior is observed. Using a mobile monitoring technique enables troop behavior to be observed collectively and at a scale relevant to the scale at which ecological choices are made.

The resulting data provides insight into primate ecology and evolution and can also be used to inform models of zoonotic disease dynamics. Primates are one of several key host clades that act as reservoirs for deadly viruses, sharing a 75-98.5% genetic homology with humans; inter and intra-troop social interactions shape disease transmission pathways in primates with behavioral matrices informing transmission, e.g., grooming interactions, mating, and fighting. All recent pandemics have had animal viral origins, and zoonotic transmission is regarded as the likely cause of the next pandemic. The changing climate has caused many wild animals to shift their range, creating the conditions for more first encounters and opportunities for undiscovered zoonoses to emerge and viruses to find new hosts. Better empirical data on troop behavior informs prediction models of known and yet-to-be-discovered viruses.

---

### **Detection**

Examples of baboon detection from drone videos:

![](assets/gifs/detection/detection.jpg)

We evaluate [YOLOv8-X](https://github.com/ultralytics/ultralytics) model with input resolution of 768x768 on our dataset and report mAP@50, Precision, and Recall.

<div class="detection"></div>

| Model | mAP@50 | Precision | Recall |
| :---: | :---: | :---: | :---: | :---: |
| YOLOv8-X | **92.62** | **93.70** | **87.60** |

---

### **Tracking**

An example of tracking over a cliff:

<div class="demo"></div>

![](assets/gifs/tracking/tracking_1.gif)

An example of tracking over a river:

<div class="demo"></div>

![](assets/gifs/tracking/tracking_2.gif)

An example of tracking over a tree:

<div class="demo"></div>

![](assets/gifs/tracking/tracking_3.gif)

An example of tracking over a rock:

<div class="demo"></div>

![](assets/gifs/tracking/tracking_4.gif)

We evaluate [ByteTrack](https://arxiv.org/abs/2110.06864), and [BotSort](https://arxiv.org/abs/2206.14651) tracking algorithms on our dataset and report MOTA, MOTP, IDF1, Precision, and Recall.

<div class="tracking"></div>

| Tracker | MOTA | MOTP | IDF1 | Precision | Recall |
| :---: | :---: | :---: | :---: | :---: | :---: |
| ByteTrack | 63.55 | 34.10 | 77.01 | 96.32 | 64.90 |
| BotSort | **63.81** | **34.31** | **78.24** | **97.21** | **66.16** |

---

### **Behavior Recognition**

The dataset includes a total of eight categories that describe various animal behaviors. These categories are `Walking/Running`, `Sitting/Standing`, `Fighting/Playing`, `Self-Grooming`, `Being Groomed`, `Grooming Somebody`, `Mutual Grooming`, `Infant-Carrying`, `Foraging`, `Drinking`, `Mounting`, `Sleeping`, and `Occluded`.

<div class="gifs"></div>

| **Walking/Running** | ![](assets/gifs/examples/Walking-Running-1.gif) | ![](assets/gifs/examples/Walking-Running-2.gif) | ![](assets/gifs/examples/Walking-Running-3.gif) |
| :---: | :---: | :---: | :---: |
| **Sitting/Standing** | ![](assets/gifs/examples/Sitting-Standing-1.gif) | ![](assets/gifs/examples/Sitting-Standing-2.gif) | ![](assets/gifs/examples/Sitting-Standing-3.gif) |
| **Fighting/Playing** | ![](assets/gifs/examples/Fighting-Playing-1.gif) | ![](assets/gifs/examples/Fighting-Playing-2.gif) | ![](assets/gifs/examples/Fighting-Playing-3.gif) |
| **Self-Grooming** | ![](assets/gifs/examples/Self-Grooming-1.gif) | ![](assets/gifs/examples/Self-Grooming-2.gif) | ![](assets/gifs/examples/Self-Grooming-3.gif) |
| **Being Groomed** | ![](assets/gifs/examples/Being-Groomed-1.gif) | ![](assets/gifs/examples/Being-Groomed-2.gif) | ![](assets/gifs/examples/Being-Groomed-3.gif) |
| <span id="long-text">**Grooming Somebody**</span> | ![](assets/gifs/examples/Grooming-Somebody-1.gif) | ![](assets/gifs/examples/Grooming-Somebody-2.gif) | ![](assets/gifs/examples/Grooming-Somebody-3.gif) |
| **Infant-Carrying** | ![](assets/gifs/examples/Infant-Carrying-1.gif) | ![](assets/gifs/examples/Infant-Carrying-2.gif) | ![](assets/gifs/examples/Infant-Carrying-3.gif) |
| **Foraging** | ![](assets/gifs/examples/Foraging-1.gif) | ![](assets/gifs/examples/Foraging-2.gif) | ![](assets/gifs/examples/Foraging-3.gif) |
| **Drinking** | ![](assets/gifs/examples/Drinking-1.gif) | ![](assets/gifs/examples/Drinking-2.gif) | ![](assets/gifs/examples/Drinking-3.gif) |
| **Mounting** | ![](assets/gifs/examples/Mounting-1.gif) | ![](assets/gifs/examples/Mounting-2.gif) | ![](assets/gifs/examples/Mounting-3.gif) |
| **Sleeping** | ![](assets/gifs/examples/Sleeping-1.gif) | ![](assets/gifs/examples/Sleeping-2.gif) | ![](assets/gifs/examples/Sleeping-3.gif) |
| **Occluded** | ![](assets/gifs/examples/Occluded-1.gif) | ![](assets/gifs/examples/Occluded-2.gif) | ![](assets/gifs/examples/Occluded-3.gif) |

We evaluate [I3D](https://arxiv.org/abs/1705.07750), [SlowFast](https://arxiv.org/abs/1812.03982), and [X3D](https://arxiv.org/abs/2004.04730) models on our dataset and report Micro-Average (Per Instance) and Macro-Average (Per Class) accuracy.

<div class="behavior_recognition"></div>

| Method | Micro  Top-1 | Micro Top-3 | Micro Top-5 | Macro Top-1 | Macro Top-3 | Macro Top-5 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| I3D | 61.29 | 89.38 | 92.34 | 26.53 | 54.51 | 65.47 |
| SlowFast | 61.71 | 90.35 | 93.11 | 27.08 | 56.73 | 67.61 |
| X3D | **63.97** | **91.34** | **95.17** | **30.04** | **60.58** | **72.13** |

---

### **Format**

```
BaboonLand
    /charades -> The dataset converted to Charades format to train and evaluate behavior
                 recognition models. You can download the generated dataset from our webpage
                 or you can generate it yourself. See instructions below.
        ...
    /cvat_templates -> You can use these templates to backup projects in CVAT.
                       It will allow you to explore and adjust the annotations in CVAT.
        /behavior.zip
        /tracking.zip
    /dataset -> The dataset is located here.
        /video_1
            /actions -> The behavior annotations are located here.
                /0.xml
                /1.xml -> Annotations of the behavior for an individual with ID=1.
                ...
                /n.xml
            /mini-scenes -> Generated mini-scenes from video.xml and tracks.xml. The name of
                            the video matches ID of the track in tracks.xml. The name of the
                            video also matches the behavior annotations file in the actions
                            folder. For example, a track with ID=1 will be extracted into
                            mini-scenes/1.mp4 and there will be behavior annotations for this
                            track located in actions/1.xml.
                /0.mp4
                /1.mp4
                ...
                /n.mp4
            /timeline.jpg -> A timeline of the original video and corresponding mini-scenes.
                             This file is generated for convenience only. You can use it to
                             look for a mini-scene with a specific length or relative
                             location in the video.
            /tracks.xml -> This file contains tracks and bounding boxes of baboons in
                           CVAT for video 1.1 format. Each track has a unique ID. This
                           number matches the name of the file in the actions folder.
                           For example, if you want to get the track and corresponding
                           bounding boxes of a baboon with ID=1, you can get this
                           information from the tracks.xml file. If you want to explore
                           the behavior of the baboon with ID=1, you can get this
                           information with the help of the actions/1.xml file.
            /video.mp4 -> The original video from a drone.
        /video_2
            /actions
                /0.xml
                /1.xml
                ...
                /n.xml
            /mini-scenes
                /0.mp4
                /1.mp4
                ...
                /n.mp4
            /timeline.jpg
            /tracks.xml
            /video.mp4
        ...
        /video_n
            /actions
                /0.xml
                /1.xml
                ...
                /n.xml
            /mini-scenes
                /0.mp4
                /1.mp4
                ...
                /n.mp4
            /tracks.xml
            /video.mp4
    /scripts
        /requirements.txt -> Install all the requirements to be able to run scripts.
        /tracks2mini-scenes.py -> Use this script to generate the mini-scenes from
                                  video.xml and tracks.xml files.
        /dataset2charades.py -> Use this script to generate a dataset for Baboon behavior
                                recognition in Charades format. The generated dataset can
                                be used to train a model with the SlowFast framework. 
        /charades2video.py -> Use this script if you want to combine images from the dataset
                              in Charades format back to videos. These videos can be used to
                              create demos of the model performance.
        /charades2visual.py -> Use this script if you want to combine images from the dataset
                               in Charades format back to videos and visualize corresponding
                               behavior annotations.
        /dataset2tracking.py -> Use this script to generate a data split for training and
                                evaluating tracking algorithms.
        /tracking2ultralytics.py -> Use this script to generate a Baboon detection dataset in
                                    Ultralytics (YOLO) format. The dataset can be used to
                                    train detection models with the Ultralytics (YOLOv8)
                                    framework.
        /ultralytics2pyramid.py -> Use this script to split the original 5.3K images in the
                                   Ultralytics dataset into tiles. You will create a dataset
                                   with 2x2, 3x3, and 4x4 tiles. It will help to train a
                                   model that will be more robust for both small and
                                   large baboons.
    /tracking -> The dataset split into train and test for tracking and train converted to
                 Ultralytics format to train and evaluate detection models. You can download
                 the generated dataset from our webpage or you can generate it yourself.
        ...
    /README.md
```

---

### **Citation**
```BibTeX
Coming soon...
```

<style>
p {
    text-align: justify !important;
}

tr, td, th {
    border: none !important;
}

div.gifs + table tr,
div.gifs + table td,
div.gifs + table th {
    border: none !important;
    padding: 1px !important;
  	line-height: 0px !important;
}

#long-text {
    line-height: 25px !important;
}

div.detection + table td {
    padding: 25px 78px !important;
}

div.tracking + table td {
    padding: 25px 43px !important;
}

div.behavior_recognition + table td {
    padding: 15px 78px !important;
}

div.demo + p img {
    display: block;
    width: 80%;
    margin-left: auto;
    margin-right: auto;
}

div.demo + p img {
    padding: 10px!important;
}

td {
    padding: 0px !important;
}

tr:nth-child(even), th {
    background: #F8F8F8 !important;
}

#td-g {
    line-height: 0px !important;
    background: #5288AD !important;
}

#td-z {
    line-height: 0px !important;
    background: #AD7752 !important;
}

h1 {
    margin: 30px 0;
    font-size: 4em;
    letter-spacing: -1px;
}

hr {
    border-top: 1px solid #E3CD81FF !important;
}
</style>
