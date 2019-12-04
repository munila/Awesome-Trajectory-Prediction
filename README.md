# Awesome-Trajectory-Prediction
![version](https://img.shields.io/badge/version-0.0.1-ff69b4.svg) ![LastUpdated](https://img.shields.io/badge/LastUpdated-2019.11.13-lightgrey.svg) ![topic](https://img.shields.io/badge/topic-trajectory--prediction-brightgreen.svg?logo=github) [![HitCount](http://hits.dwyl.io/xuehaouwa/Awesome-Trajectory-Prediction.svg)](http://hits.dwyl.io/xuehaouwa/Awesome-Trajectory-Prediction) [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

<p align="center">
  <img width="250" src="https://camo.githubusercontent.com/1131548cf666e1150ebd2a52f44776d539f06324/68747470733a2f2f63646e2e7261776769742e636f6d2f73696e647265736f726875732f617765736f6d652f6d61737465722f6d656469612f6c6f676f2e737667" "Awesome!">
</p>

This is a list of useful information about trajectory prediction. Related papers, datasets and codes are included.

Maintainer - Hao Xue


## Contributing
Please feel free to [pull requests](https://github.com/xuehaouwa/Awesome-Trajectory-Prediction/pulls) to add new resources.

## Papers
#### RNN Related
- An Empirical Evaluation of Generic Convolutional and Recurrent Networks for Sequence Modeling, 2018, [code](https://github.com/locuslab/TCN)
- When will you do what? - Anticipating Temporal Occurrences of Activities, 2018 CVPR,   [code]( https://github.com/yabufarha/anticipating-activities)
- Independently Recurrent Neural Network (IndRNN): Building A Longer and Deeper RNN, 2018 CVPR, [code](https://github.com/batzner/indrnn), [keras-code](https://github.com/titu1994/Keras-IndRNN), [pytorch code](https://github.com/StefOe/indrnn-pytorch/blob/master/indrnn.py)
- Predicting the Next Location: A Recurrent Model with Spatial and Temporal Contexts, 2016 AAAI [code](https://github.com/yongqyu/STRNN)



#### Trajectory Prediction Related

- Disentangling Human Dynamics for Pedestrian Locomotion Forecasting with Noisy Supervision, 2020 WACV, [Paper](https://arxiv.org/abs/1911.01138)
	- unifying human pose estmation ad trajectory prediction
	- Disentanglement of overall motion into easier subparts
	- NN used: [Quasi-RNN](https://arxiv.org/pdf/1611.01576.pdf´)
	- JAAD dataset (SOTA keypoint displacement error KDE)
- Forecasting Trajectory and Behavior of Road-Agents Using Spectral Clustering in Graph-LSTMs, 2019 arXiv, [Paper](https://arxiv.org/pdf/1912.01118.pdf), [Code](https://gamma.umd.edu/researchdirections/autonomousdriving/spectralcows/)
	- combination of spectral graph analysis and deep learning to predict future trajectories (low-level; points) and road-agent behavior (high-level; e.g.overspeeding, braking)
	- NN used Conv-LSTM
	- Datasets: Argoverse (ADE, FDE SOTA), Lyft (ADE, FDE SOTA), Apolloscape (ADE, FDE SOTA) 
- PIE: A Large-Scale Dataset and Models for Pedestrian Intention Estimation and Trajectory Prediction, 2019 ICCV, [Paper](<http://openaccess.thecvf.com/content_ICCV_2019/papers/Rasouli_PIE_A_Large-Scale_Dataset_and_Models_for_Pedestrian_Intention_Estimation_ICCV_2019_paper.pdf>)
	- Combining modules for trajectory prediction, intention estimation and vehicle speed prediction
	- NN used:  Conv LSTM 
	- Datasets: PIE, JAAD (MSE over Bounding Box koordinates)
- STGAT: Modeling Spatial-Temporal Interactions for Human Trajectory Prediction, 2019 ICCV, [Paper](http://openaccess.thecvf.com/content_ICCV_2019/papers/Huang_STGAT_Modeling_Spatial-Temporal_Interactions_for_Human_Trajectory_Prediction_ICCV_2019_paper.pdf)
	- graph attention network to model spatial realtions, LSTM for temporal
	- NN used: sequence to sequnece LSTM
	- variety loss according to social GAN (adding different noise to hidden state)
	- Datasets: UCY/ ETH (ADE/FDE) SOTA 20V20
- RobustTP: End-to-End Trajectory Prediction for Heterogeneous Road-Agents in Dense Traffic with Noisy Sensor Inputs, 2019 ACM CSCS, [Paper](https://arxiv.org/pdf/1907.08752.pdf), [Code](https://github.com/rohanchandra30/TrackNPred)
	- designed for road agent trajectory prediction in dense heterogeneous traffic
	- NN used: Conv-LSTM
	- Datasets: TRAF (ADE/ SDE)
- Social and Scene-Aware Trajectory Prediction in Crowded Spaces, 2019 ICCV Workshop, [Paper](<https://arxiv.org/pdf/1909.08840.pdf>), [Code](<https://github.com/Oghma/sns-lstm/>)
	- prediction based on: people interaction, past observations, semantics of the surrounding
	- NN used: LSTM
	- Datasets: ETH/ UCY (ADE/ FDE)
- Scene Compliant Trajectory Forecast with Agent-Centric Spatio-Temporal Grids, 2019 ArXiv, [Paper](<https://arxiv.org/pdf/1909.07507.pdf>)
	- model based on 2D grid representation of trajectories in order to address heterognity of current scene data representation (RGB Img) and trajectory (usually Coordinates) to predict human trajectories
	- NN used: U-Net, ResNet, Conv-LSTM
	- Datasets: Stanford Drone Dataset (ADE/ FDE)
- Trajectory Prediction by Coupling Scene-LSTM with Human Movement LSTM, 2019 ISVC, [Paper](https://arxiv.org/pdf/1908.08908.pdf)
	- scene information and pedestrian movement information trained simultaneously, both utilizing LSTMs
	- encoding of spatial granularity and commun human movements by 2 level grid structure (cells and subgrids)
	- filter to determine relevant information within a scene
	- NN used: LSTM
	- datasets ETH/ UCY (ADE/FDE)
- SEABIG: A Deep Learning-Based Method for Location Prediction in Pedestrian Semantic Trajectories, 2019 IEEE Access, [Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8790746)
	- design of Gaussian MMto extract  stopover points from raw trajectories and annotate semantic information on stopover points
	- Bidirectional Gated Recurrent Unit to predict trajectories and annotate most likely semantic with embedding
	- NN used: RNN
	- Datasets: Bejing (dont realy know it ...)
- Trajectory Prediction of Mobile Construction Resources Toward Pro-active Struck-by Hazard Detection, 2019 ISARC, [Paper](https://search.proquest.com/openview/f6b42779cd7037405799f86f8ca9e544/1?pq-origsite=gscholar&cbl=1646340&casa_token=KxabXy5827MAAAAA:Kv6jfuGvLfpCRhZb1YlzEB0pgpSFJQPKAG8yEcLUwZk4yVjYWn1iCKR1uesqbnH76XJj6smFh5Q)
	- cannot read whole paper but doesnt seem to relevant to me
- A novel model based on deep learning for Pedestrian detection and Trajectory prediction, 2019 ITAIC, [Paper](https://ieeexplore.ieee.org/abstract/document/8785741)
	- integration of pedestrian detection, multi agent tracking and circular neighborhood (in social scale)
	- adding two different LSTMs to capture the interaction information between the target person and neighboring pedestrians
	- NN used: LSTM
	- Dataset: UCY (ADE/FDE but seems to measure in different prediction time which is not specified anywhere but according to qual results it is half of other methods)
- Pedestrian Trajectory Prediction Using a Social Pyramid, 2019 PRICAI
- Path predictions using object attributes and semantic environment, 2019 VISIGRAPP, [Paper](http://mprg.jp/data/MPRG/C_group/C20190225_minoura.pdf)
- Probabilistic Path Planning using Obstacle Trajectory Prediction, 2019 [CoDS-COMAD '19](http://cods-comad.in/2019/index.html), [Paper](https://dl.acm.org/citation.cfm?id=3297006)
- Human Trajectory Prediction using Adversarial Loss, 2019 (from Alahi, conference unknown for now), [Paper](http://www.strc.ch/2019/Kothari_Alahi.pdf)
- Social Ways: Learning Multi-Modal Distributions of Pedestrian Trajectories
  with GANs, 2019 CVPR [*Precognition Workshop*](https://sites.google.com/view/ieeecvf-cvpr2019-precognition), [Paper](http://openaccess.thecvf.com/content_CVPRW_2019/papers/Precognition/Amirian_Social_Ways_Learning_Multi-Modal_Distributions_of_Pedestrian_Trajectories_With_GANs_CVPRW_2019_paper.pdf), [Code](<https://github.com/amiryanj/socialways>)
- Peeking into the Future: Predicting Future Person Activities and Locations in Videos, 2019 CVPR, [Paper](http://openaccess.thecvf.com/content_CVPR_2019/papers/Liang_Peeking_Into_the_Future_Predicting_Future_Person_Activities_and_Locations_CVPR_2019_paper.pdf), [Code](https://github.com/google/next-prediction)
- Learning to Infer Relations for Future Trajectory Forecast, 2019 CVPR [*Precognition Workshop*](https://sites.google.com/view/ieeecvf-cvpr2019-precognition), [Paper](http://openaccess.thecvf.com/content_CVPRW_2019/papers/Precognition/Choi_Learning_to_Infer_Relations_for_Future_Trajectory_Forecast_CVPRW_2019_paper.pdf)
- TraPHic: Trajectory Prediction in Dense and Heterogeneous Traffic Using Weighted Interactions, 2019 CVPR, [Paper](<http://openaccess.thecvf.com/content_CVPR_2019/papers/Chandra_TraPHic_Trajectory_Prediction_in_Dense_and_Heterogeneous_Traffic_Using_Weighted_CVPR_2019_paper.pdf>), [Code](https://github.com/rohanchandra30/TrackNPred)
	-
- Which Way Are You Going? Imitative Decision Learning for Path Forecasting in Dynamic Scenes, 2019 CVPR, [Paper](<http://openaccess.thecvf.com/content_CVPR_2019/papers/Li_Which_Way_Are_You_Going_Imitative_Decision_Learning_for_Path_CVPR_2019_paper.pdf>)
- Overcoming Limitations of Mixture Density Networks: A Sampling and Fitting Framework for Multimodal Future Prediction, 2019 CVPR, [Paper](<http://openaccess.thecvf.com/content_CVPR_2019/papers/Makansi_Overcoming_Limitations_of_Mixture_Density_Networks_A_Sampling_and_Fitting_CVPR_2019_paper.pdf>)
- SoPhie: An Attentive GAN for Predicting Paths Compliant to Social and Physical Constraints, 2019 CVPR, [Paper](<http://openaccess.thecvf.com/content_CVPR_2019/papers/Sadeghian_SoPhie_An_Attentive_GAN_for_Predicting_Paths_Compliant_to_Social_CVPR_2019_paper.pdf>)
	- social and physical constraints taken into account by utilizing trajectory (social) and img of scene (physical contraints)
	- NN used: CNN Encoder, LSTM Encoder, LSTM-GAN
	- Datasets: ETH, UCY, Stanford DD
- Multi-Agent Tensor Fusion for Contextual Trajectory Prediction, 2019 CVPR, [Paper](<http://openaccess.thecvf.com/content_CVPR_2019/papers/Sadeghian_SoPhie_An_Attentive_GAN_for_Predicting_Paths_Compliant_to_Social_CVPR_2019_paper.pdf>)
- Future Person Localization in First-Person Videos, 2018 CVPR, [Paper](http://openaccess.thecvf.com/content_cvpr_2018/papers/Yagi_Future_Person_Localization_CVPR_2018_paper.pdf), [code](https://github.com/takumayagi/fpl) 
- Move, Attend and Predict: Anattention-based neural model for people’s movement prediction, 2018 Pattern Recognition Letters, [Paper](https://reader.elsevier.com/reader/sd/pii/S016786551830182X?token=1EF2B664B70D2B0C3ECDD07B6D8B664F5113AEA7533CE5F0B564EF9F4EE90D3CC228CDEB348F79FEB4E8CDCD74D4BA31)
- Group LSTM: Group Trajectory Prediction in Crowded Scenarios, 2018 ECCV Workshop, [Paper](http://openaccess.thecvf.com/content_ECCVW_2018/papers/11131/Bisagno_Group_LSTM_Group_Trajectory_Prediction_in_Crowded_Scenarios_ECCVW_2018_paper.pdf)
- Pedestrian Trajectory Prediction in Extremely Crowded Scenarios, 2019 Sensors (journal), [Paper](https://www.mdpi.com/1424-8220/19/5/1223/pdf)
- The Simpler the Better: Constant Velocity for Pedestrian Motion Prediction, 2019, [Paper](https://arxiv.org/pdf/1903.07933.pdf)
- SR-LSTM: State Refinement for LSTM towards Pedestrian Trajectory Prediction, 2019 CVPR, [Paper](https://arxiv.org/pdf/1903.02793.pdf)
- Situation-Aware Pedestrian Trajectory Prediction with Spatio-Temporal Attention Model, 2019 Computer Vision Winter Workshop (CVWW), [Paper](https://arxiv.org/pdf/1902.05437.pdf)
- Depth Information Guided Crowd Counting for Complex Crowd Scenes, 2018
- GD-GAN: Generative Adversarial Networks for Trajectory Prediction and Group Detection in Crowds, 2018 ACCV, [Paper](https://arxiv.org/pdf/1812.07667.pdf), [Demo](https://www.youtube.com/watch?v=7cCIC_JIfms)
- Tracking by Prediction: A Deep Generative Model for Mutli-Person Localisation and Tracking, 2018 WACV
- “Seeing is Believing”: Pedestrian Trajectory Forecasting Using Visual Frustum of Attention, 2018 WACV
- Social GAN: Socially Acceptable Trajectories with Generative Adversarial Networks, 2018 CVPR, [paper](https://arxiv.org/pdf/1803.10892.pdf) [code](https://github.com/agrimgupta92/sgan)
	- trajectory prediction based on data distribution of possible trajectories
	- only on trajectory data, no explicit knowledge about environment and a so called variety loss which basically computes loss for best of k samples in order to increase multimodality
	- proposal of pooling based on relativ pedestrian prediction
	- NN used: LSTM-GAN (LSTM-Encoder/Decoder)
	- Datasets: ETH, UCY (ADE/ FDE)
- Long-Term On-Board Prediction of People in Traffic Scenes under Uncertainty, 2018 CVPR, [[Paper]](http://openaccess.thecvf.com/content_cvpr_2018/papers/Bhattacharyya_Long-Term_On-Board_Prediction_CVPR_2018_paper.pdf), [code+data](https://github.com/apratimbhattacharyya18/onboard_long_term_prediction)
- Encoding Crowd Interaction with Deep Neural Network
  for Pedestrian Trajectory Prediction, 2018 CVPR, [[Paper]](http://openaccess.thecvf.com/content_cvpr_2018/papers/Xu_Encoding_Crowd_Interaction_CVPR_2018_paper.pdf), [code](https://github.com/ShanghaiTechCVDL/CIDNN)
- Scene-LSTM: A Model for Human Trajectory Prediction, 2018 ArXiv, [Paper](https://arxiv.org/pdf/1808.04018.pdf)
- Bi-prediction: pedestrian trajectory prediction based on bidirectional LSTM classification, 2017 DICTA, [Paper](<https://www.researchgate.net/profile/Du_Huynh/publication/322001876_Bi-Prediction_Pedestrian_Trajectory_Prediction_Based_on_Bidirectional_LSTM_Classification/links/5c03cef4a6fdcc1b8d5029bb/Bi-Prediction-Pedestrian-Trajectory-Prediction-Based-on-Bidirectional-LSTM-Classification.pdf>)
- Human Trajectory Prediction using Spatially aware Deep Attention Models, 2017 arxiv, [[Paper]](https://arxiv.org/pdf/1705.09436.pdf)
- Context-Aware Trajectory Prediction, 2017 arxiv, [[Paper]](https://arxiv.org/pdf/1705.02503.pdf)
- Soft + Hardwired Attention: An LSTM Framework for Human Trajectory Prediction and Abnormal Event Detection, 2017 arxiv, [[Paper]](https://arxiv.org/pdf/1702.05552.pdf) 
- Forecasting Interactive Dynamics of Pedestrians with Fictitious Play, 2017 CVPR, [[Paper]](http://openaccess.thecvf.com/content_cvpr_2017/papers/Ma_Forecasting_Interactive_Dynamics_CVPR_2017_paper.pdf)
- Social LSTM: Human Trajectory Prediction in Crowded Spaces, 2016 CVPR, [[Paper]](http://cvgl.stanford.edu/papers/CVPR16_Social_LSTM.pdf)
- STF-RNN: Space Time Features-based Recurrent Neural Network for predicting People Next Location, 2016 SSCI, [Keras-Code](https://github.com/mhjabreel/STF-RNN)



#### Vehicle Trajectory Prediction
- Forecasting Trajectory and Behavior of Road-Agents Using Spectral Clustering in Graph-LSTMs, 2019 arXiv, [Paper](https://arxiv.org/pdf/1912.01118.pdf), [Code](https://gamma.umd.edu/researchdirections/autonomousdriving/spectralcows/)
- RobustTP: End-to-End Trajectory Prediction for Heterogeneous Road-Agents in Dense Traffic with Noisy Sensor Inputs, 2019 ACM CSCS, [Paper](https://arxiv.org/pdf/1907.08752.pdf), [Code](https://github.com/rohanchandra30/TrackNPred)
- TraPHic: Trajectory Prediction in Dense and Heterogeneous Traffic Using Weighted Interactions, 2019 CVPR, [Paper](<http://openaccess.thecvf.com/content_CVPR_2019/papers/Chandra_TraPHic_Trajectory_Prediction_in_Dense_and_Heterogeneous_Traffic_Using_Weighted_CVPR_2019_paper.pdf>), [Code](https://github.com/rohanchandra30/TrackNPred)
- Multi-Step Prediction of Occupancy Grid Maps with Recurrent Neural Networks, 2019 CVPR, [Paper](https://arxiv.org/pdf/1812.09395.pdf)
- Argoverse: 3D Tracking and Forecasting With Rich Maps, 2019 CVPR, [Paper](http://openaccess.thecvf.com/content_CVPR_2019/papers/Chang_Argoverse_3D_Tracking_and_Forecasting_With_Rich_Maps_CVPR_2019_paper.pdf)
- Robust Aleatoric Modeling for Future Vehicle Localization, 2019 CVPR [*Precognition Workshop*](https://sites.google.com/view/ieeecvf-cvpr2019-precognition), [Paper](http://openaccess.thecvf.com/content_CVPRW_2019/papers/Precognition/Hudnell_Robust_Aleatoric_Modeling_for_Future_Vehicle_Localization_CVPRW_2019_paper.pdf)
- Convolutional Social Pooling for Vehicle Trajectory Prediction, 2018 CVPR, [Paper](http://openaccess.thecvf.com/content_cvpr_2018_workshops/papers/w29/Deo_Convolutional_Social_Pooling_CVPR_2018_paper.pdf) [code](https://github.com/nachiket92/conv-social-pooling)
#### Traffic Prediction


- Deep Sequence Learning with Auxiliary Information for Traffic Prediction, 2018 KDD, [Paper](https://arxiv.org/pdf/1806.07380.pdf), [Code](https://github.com/JingqingZ/BaiduTraffic)

## Datasets

* [UCY](https://graphics.cs.ucy.ac.cy/research/downloads/crowd-data)
* [ETH](http://www.vision.ee.ethz.ch/en/datasets/)
* [New York Grand Central](http://www.ee.cuhk.edu.hk/en-gb/~syi/cvpr2015_dataset_pedestrianWalkingPath.pdf) (404)
* [Central Station](http://www.ee.cuhk.edu.hk/~xgwang/grandcentral.html)
* [Town Center](http://www.robots.ox.ac.uk/ActiveVision/Research/Projects/2009bbenfold_headpose/project.html#datasets)
* [Edinburgh Informatics Forum Pedestrian Database](http://homepages.inf.ed.ac.uk/rbf/FORUMTRACKING/)
* [Cityscapes](https://www.cityscapes-dataset.com/login/)
* [Stanford Drone Dataset](http://cvgl.stanford.edu/projects/uav_data/)
* [Argoverse](https://www.argoverse.org/)
* [TRAF](https://gamma.umd.edu/researchdirections/autonomousdriving/trafdataset)
* [inD](https://www.ind-dataset.com/)
* [Lyft Level 5](https://level5.lyft.com/dataset/)
* [Apolloscape](http://apolloscape.auto/trajectory.html)
* [Joint Attention in Autonomous Driving](http://data.nvision2.eecs.yorku.ca/JAAD_dataset/)

