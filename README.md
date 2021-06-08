# InteractionGCN

This repository will contain the GCN-based implementation [1] for social interaction classification on GeorgiaTech dataset [2].

### Features and model

In `data/`, the pretrained model and the features of [2] are provided. In `data/all_features.zip`, two types of files are given:
- `f_*`: they contain the non-relational features for each individual for each frame with the following format: [ID, x_position, y_position, distance_from_camera, pitch, roll, yaw]
- `d_*`: they contain the relational features for each frame, i.e. the distance between two people _i_ and _j_, with the following format: [ID_i, ID_j, distance]

### Challenging cases
In `examples/`, some challenging, failure and success examples are reported.  

### References
[1] [Interaction-GCN: a Graph Convolutional Network based framework for social interaction recognition in egocentric videos](https://arxiv.org/abs/2104.14007)

[2] [Social interactions: A first-person perspective](http://amav.gatech.edu/sites/default/files/papers/cvpr2012.Fathi_.Hodgins.Rehg_.printed.pdf)
