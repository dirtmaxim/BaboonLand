---
layout: default
permalink: /
title: ""
---

![](assets/images/introduction.jpg)

---

### **Overview**

This dataset comprises twenty-one consecutive days of video footage collected by a drone, following three troops of wild Olive baboons in Laikipia, Northern Kenya, as they left and returned to known sleeping sites, morning and night. Over ten hours of video footage were collected in various environments, including at a sleeping tree, a river, a rock, during a river crossing, in open savannah, and on a cliff. Frames include up to 70 individuals tracked simultaneously, forming a complex and dense dataset of overlapping individuals from an aerial perspective. Three fundamental subtasks have been identified from the original dataset: detection, tracking, and behavior recognition. The data contains significant visual noise from camera motion, varying light conditions, spectral contrast from shadows, and different background environments. This is the first dataset to automate the classification of non-human primate behavior from aerial video, enabling the understanding of inter-group interactions in the context of the natural environment and in relation to the behavior of other troop members. This provides insight into the social network of the group.

Automatically tracking individual ethograms that form collective behavior can help unravel consistent patterns of group organization. Tracking individual exchanges enables the identification of triggers for switches in group behavior, leading to a better understanding of why splinter groups emerge. Additionally, various formations in the attack and defense of territory can be mapped. Non-human primates are highly territorial and switch allegiances depending on resource availability and prior interactions. By automatically modeling these interactions, we can better understand group dynamics and tipping points in collective behavior, including the emergence of new group formations. This goal is to methodologically advance the analysis of social network structures and collective decision-making to improve predictive capabilities. Existing video datasets of primates are from camera traps or hand-held video recorders, limiting the number of individuals visible in a frame at once and the spatial and temporal window in which behavior is observed. Using a mobile monitoring technique enables troop behavior to be observed collectively and at a scale relevant to the decisions made.

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

We evaluate [SORT](https://arxiv.org/abs/1602.00763), [DeepSORT](https://arxiv.org/abs/1703.07402), [StrongSORT](https://arxiv.org/abs/2202.13514), [ByteTrack](https://arxiv.org/abs/2110.06864), and [BotSort](https://arxiv.org/abs/2206.14651) tracking algorithms on our dataset and report MOTA, MOTP, IDF1, Precision, and Recall.

<div class="tracking"></div>

| Tracker | MOTA | MOTP | IDF1 | Precision | Recall |
| :---: | :---: | :---: | :---: | :---: | :---: |
| SORT | **84.76** | 50.15 | 77.43 | 90.83 | 91.19 |
| DeepSORT | 84.40 | **87.22** | 81.38 | 90.26 | **91.57** |
| StrongSORT | 82.48 | 85.37 | **84.98** | 88.00 | 90.10 |
| ByteTrack | 63.55 | 34.10 | 77.01 | 96.32 | 64.90 |
| BotSort | 63.81 | 34.31 | 78.24 | **97.21** | 66.16 |

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

| Method | WI | Micro  Top-1 | Micro Top-3 | Micro Top-5 | Macro Top-1 | Macro Top-3 | Macro Top-5 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| I3D | Random | 61.29 | 89.38 | 92.34 | 26.53 | 54.51 | 65.47 |
| SlowFast | Random | 61.71 | 90.35 | 93.11 | 27.08 | 56.73 | 67.61 |
| X3D | Random| 63.97 | 91.34 | 95.17 | 30.04 | 60.58 | 72.13 |
| X3D | K-400 | **64.89** | **92.54** | **96.66** | **31.41** | **62.04** | **74.01** |

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

### **Acknowledgments**

ID was supported by the National Academy of Sciences Research Associate Program and the United States Army Research Laboratory while conducting this study. MK was supported by the National Science Foundation under [Award No. 2118240](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2118240) and [Award No. 2112606](https://www.nsf.gov/awardsearch/showAward?AWD_ID=2112606) (AI Institute for Intelligent Cyberinfrastructure with Computational Learning in the Environment ([ICICLE](https://icicle.osu.edu))). ID collected all the UAV data on a Civil Aviation Authority Drone License CAA NQE Approval Number: 0216/1365 in conjunction with authorization from a KCAA operator under a Remote Pilot License. The data was gathered at the Mpala Research Centre in Kenya, in accordance with Research License No. NACOSTI/P/22/18214. The data collection protocol adhered strictly to the guidelines set forth by the Institutional Animal Care and Use Committee under permission No. IACUC 1835F.

---

### **Citation**
```BibTeX
@misc{duporge2024baboonland,
  title={BaboonLand Dataset: Tracking Primates in the Wild and Automating Behaviour Recognition from Drone Videos}, 
  author={Isla Duporge and Maksim Kholiavchenko and Roi Harel and Dan Rubenstein and Meg Crofoot and Tanya Berger-Wolf and Stephen Lee and Scott Wolf and Julie Barreau and Jenna Kline and Michelle Ramirez and Chuck Stewart},
  year={2024},
  eprint={2405.17698},
  archivePrefix={arXiv},
  primaryClass={cs.CV}
}
```

---

### **See Also**

<a href="https://dirtmaxim.github.io/kabr" id="see-also-link">KABR Dataset</a>

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

#see-also-link {
  display: inline-block;
  padding: 10px 20px;
  font-size: 16px;
  font-weight: bold;
  color: #ffffff;
  background-color: #4CAF50;
  text-align: center;
  text-decoration: none;
  border-radius: 5px;
  transition: background-color 0.3s ease;
}

#see-also-link:hover {
  background-color: #45a049;
}
</style>
