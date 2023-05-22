# LiMM
This is the code of our paper"Index Matters: Learning Road Network Index Structure for Fast Map Matching"

## Dataset
We provide a sample dataset of porto in \[data/porto]. 
- Folder \[data/porto/rein_tra] is the training dataset of Q-learning for adaptive searching range. 
- Folder \[data/porto/trajectory] is the raw trajectories of HMMLimm matching. 

Please download porto map from <a href="https://www.openstreetmap.org" target="_blank">OpenStreetMap</a>, with boundary : {***lat_min = 41.05, lat_max = 41.25, lon_min = -8.75, lon_max = -8.45***}, name \[***porto.osm***],  put it in \[***data/porto/***].

## Requirements
- python == 3.7
- tensorflow == 1.15.0
- networkx == 2.6.3
- rtree == 0.9.7
- osm2gmns==0.6.8
- psutil == 5.9.0
- tqdm == 4.65.0

## Running
python main.py porto -p trajectory -e HMMLimm

## Result
- Folder \[result/porto/rein_ground_truth] is the ground truth(matched trajectories) of reinforcement learning for adaptive searching range. 
- Folder \[result/porto/hexagon_q_table] is the Q-tables for each hexagon.
- Folder \[result/porto/limm] is the matching trajectories of HMMLimm.
