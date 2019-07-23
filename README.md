# kPAM: Generalizable Robotic Manipulation

This project aims at pose-aware robotic manipulation for a category of object. Different from most existing pose aware manipulation algorithms that most contain an explicit pose estimation, we define the object target configuration on top of semantic keypoints. In this way, the proposed pipeline can handle potentially unknown objects with substantial variations on shape, appearance and topology.

### Publication

Lucas Manuelli*, Wei Gao*, Pete Florence, Russ Tedrake, "kPAM: KeyPoint Affordances for Category-Level Robotic Manipulation", ISRR 2019  [[Project]](<https://sites.google.com/view/kpam>)[[Paper]](https://arxiv.org/abs/1903.06684)[[Video]](https://www.youtube.com/watch?v=fm5RZ-ht1y0)

### Code Organization

The code is distributed into several modularized packages

- mrcnn_integrate: The code to train the maskrcnn-benchmark instance segmentor
- mrcnn_ros: The ros binding of maskrcnn-benchmark
- mankey: The keypoint detection for the pipeline
- mankey_ros: The ros binding of mankey
- kplan_ros: The planning backend
- kpam_coordinator: The package that integrate all the submodules

In our experiment setup, these packages will be the submodule of spartan, which provides the interface to our robots. However, everything except  `kpam_coordinator` should be platform-independent.

### Data

