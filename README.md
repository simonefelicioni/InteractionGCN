# InteractionGCN

This repository contains the model trained with our ICIP 2021 paper on [Interaction-GCN: a Graph Convolutional Network based framework for social interaction recognition in egocentric videos](https://arxiv.org/abs/2104.14007), as well as the features extracted from the GeorgiaTech dataset (available [here](http://cbs.ic.gatech.edu/egocentric/datasets.htm)) we used as input to our model. 

<br />
<p align="center">
  <img src="workflow.png" width="600"/>
</p>
<p align="center">
  Fig 1: Workflow of the framework. This extracts patterns of relational and non-relational cues at the frame level and uses them to build a relational graph from which the interactional context at the frame level is estimated via a Graph Convolutional Network (GCN) based approach. Then it propagates this context over time, together with first-person motion information, through a Gated Recurrent Unit (GRU) architecture.
</p>

### Updates
- **20/05/2021**: Accepted to ICIP 2021.
- **08/06/2021**: Pretrained model and features are released.

### Features

The pretrained model and the features of GeorgiaTech dataset are provided:
- Pretrained model is available in the `data/` folder.
- Relational and non-relational features are available in `data/all_features.zip`. Two types of files are given:
  - `f_*`: they contain the non-relational features for each individual for each frame with the following format: <p align="center">[ID, x_position, y_position, distance_from_camera, pitch, roll, yaw]</p>
  - `d_*`: they contain the relational features for each frame, i.e. the distance between two people _i_ and _j_, with the following format: <p align="center">[ID_i, ID_j, distance]</p>
- Homographies are available [here](https://drive.google.com/file/d/1KJlx1XYzBza4xOR06-OxdP9g2hZkbux3/view?usp=sharing).

### Challenging cases
In `examples/`, some challenging, failure and success examples are reported.

<br />

<p align="center">
  <img src="classes.png" width="600"/>
</p>
<p align="center">
  Fig 2: Classes of interactions. This illustrates the difficulty of the problem in the GeorgiaTech Social Interaction dataset, captured by a head-mounted wearable camera in an amusement park: five different conversation types may occur at different time intervals during a social interaction, even in absence of drastic visual changes, e.g, discussion vs dialogue.
</p>

### References
 If you find this work useful in your research, please cite:

```
@inproceedings{felicioni2021,
Author = {Felicioni, Simone and Dimiccoli, Mariella},
Title = {Interaction-GCN: a Graph Convolutional Network based framework for social interaction recognition in egocentric videos},
Booktitle  = {IEEE International Conference on Image Processing (ICIP)},
Year = {2021}
}
```
