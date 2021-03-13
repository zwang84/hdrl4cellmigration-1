# Hierarchical deep reinforcement learning reveals novel mechanism of cell movement

## Introduction
This is accompany code and data associated with the paper submission 'Hierarchical deep reinforcement learning reveals novel mechanism of cell movement'.

## Package requirements
  Python3 <br />
  PyTorch 0.2 (tested on 0.2.0_3) <br />
  Mesa <br />
  PIL 4.2.1 <br />
  scikit-learn 0.19.1 <br />
  numpy (tested on 1.15.0) <br />
  
## File structure
  ./data/: folder with textual data of nuclei <br />
  ./data/Cpaaa_0: embryonic data for Cpaaa migration training and evaluation. <br />
  ./data/Cpaaa_[1-4]: embryonic data for Cpaaa test case. <br />
  ./data/mu_int_R_CANL_[1-2]: embryonic data for mu_int_R and CANL case. <br />
  ./trained_models/:folder with all the pre-trained models <br />
  ./trained_models/dqn_eval_net_pretrained.pkl: checkpoint of the trained lower-level DQN <br />
  ./trained_models/motion_model.pkl: checkpoint of the trained Motion Model <br />
  ./trained_models/neighbor_model_800k_train.p: checkpoint of the trained Neighbor Relationship Model <br />
  ./Embryo.py: functions for parsing the embryo data
  ./draw_plane.py: visualization
  ./model.py: agent-based model
  ./run.py: simulation running

## Usage
1. Explore the successful scenarios: python3 run_dqn.py <br />
   3 Files are generated in the 'saved_data' folder after the evaluation: <br />
     - movement_index.pkl: the movement index (1 for directional movement and 0 for random movement) of Cpaaa at each time step. <br />
     - cpaaa_locations.pkl: location of Cpaaa at each time step. <br />
     - target_locations.pkl: location of the target cell (ABarpaapp) at each time step. If ABarpaapp is not born, [0,0,0] is used as a placeholder. <br />

## Citation
add after paper submitted to biorxiv.

