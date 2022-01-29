# Multi-Object-Tracking-Lacrosse-Game
This repo contains my codes for Multi-Object Tracking in a Lacrosse Game

## Introduction: Multiple Object Tracking 

Multiple Object Tracking (MOT) is the problem of automatically identifying multiple objects in a video and representing them as a set of trajectories with high accuracy.

![image](https://user-images.githubusercontent.com/35584782/151681212-634d49ca-79a3-40c6-8e5e-f419f9299257.png)


## Goal: MOT in Lacrosse Game

Lacrosse is competitive sport in which two teams of players use long-handled, racketlike implements (crosses) to catch, carry, or throw a ball down the field or into the opponents' goal.

![image](https://user-images.githubusercontent.com/35584782/151681237-744948e4-c1d7-408b-98cd-335565197a11.png)


## Proposed Solution

Our solution requires three parts:

- Object detection to detect players
- Object tracker to track trajectories of players in the video
- Define Metrics of how well each player is playing

## Player Detection 

![image](https://user-images.githubusercontent.com/35584782/151681272-b6460826-923e-49df-90d7-1cf6de7d65eb.png)

## Multi Object Trackers

- CentroidTracker: Computes the Euclidean distance between the centroids of the input bounding boxes and the centroids of existing objects that we already have examined.

- CentroidKF_Tracker: CentroidTracker+Kalman filter

- IOUTracker: tracking algorithm or method to track objects based on their Intersection-Over-Union (IOU) information across the consecutive frame.


## Evaluation Metrics

 After applying our CenterNet+ Centroid Tracker model, we obtained the trajectory of each player in the video game.

We then define the following metrics:

- Total distance traveled
- Speed of the player 



## Results

Example: Player ID 1

![image](https://user-images.githubusercontent.com/35584782/151681327-957cbf4a-6283-46c7-be61-9585822ecfdb.png)


total traveled 2299.26 in pixels and his speed was 208.70 pixels/sec


Example: Player ID 2

![image](https://user-images.githubusercontent.com/35584782/151681336-96f372f7-1415-40ab-b885-f73557b8922c.png)

total traveled 1022.74 in pixels and his speed was 99.90 pixels/sec


## References 

- Duan, Kaiwen, et al. "Centernet: Keypoint triplets for object detection." Proceedings of the IEEE/CVF International Conference on Computer Vision. 2019.
- Tan, Mingxing, Ruoming Pang, and Quoc V. Le. "Efficientdet: Scalable and efficient object detection." Proceedings of the IEEE/CVF conference on computer vision and pattern recognition. 2020.
- Sandler, Mark, et al. "Mobilenetv2: Inverted residuals and linear bottlenecks." Proceedings of the IEEE conference on computer vision and pattern recognition. 2018.
- Redmon, Joseph, and Ali Farhadi. "Yolov3: An incremental improvement." arXiv preprint arXiv:1804.02767 (2018).
- https://github.com/adipandas/multi-object-tracker









