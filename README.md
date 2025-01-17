# RL Surgical Gesture Segmentation

This repo includes two parts:
1. Re-implementation of Temporal Convolutional Networks (For the original version, please refer to [Colin Lea's repo](https://github.com/colincsl/TemporalConvolutionalNetworks)).
2. The MDP formulation and a customized OpenAI Gym Env. Policy training is implemented with OpenAI Baseline.

# Install

All packages should be their versions from around 2018, along with Python 3.6.

1. Install scipy, numpy, pandas, matplotlib
2. Install pytorch, tensorflow, gym
3. Clone [this snapshot version of OpenAI Baseline](https://github.com/Finspire13/baselines) and follow its install instructions. [The offical library](https://github.com/openai/baselines) is under rapid development and often brings breaking changes
4. Clone this repo

# Dataset

The code is tested on the JIGWSAWS visual suturing and GTEA. Thanks to Colin Lea for providing pre-processed data for these datasets!

# How to Run

### Hyper-parameters

Setttings and hyper-parameters are in *config.json*. 

### Run the whole experiment (Recommanded)

First setup the experiment in *experiment.py*. Then:

`cd <this repo>`

`python3 experiment.py`

On Google Cloud, this takes about 3 hours (2 hours TCN, 1 hour RL).

### Output

CSV files: the final results

Folder *result*: the results in npy format

Folder *graph*: plots and figures

Folder *tcn_featrues*: featrues extracted by TCN (states for RL)

Floder *tcn_log*: Training log for TCN (Visulize with tensorboard)

Folder *tcn_model*: Trained models for TCN

Folder *trpo_model*: Trained models for RL

# Citation

@InProceedings{10.1007/978-3-030-00937-3_29,
  author="Liu, Daochang and Jiang, Tingting",
  title="Deep Reinforcement Learning for Surgical Gesture Segmentation and Classification",
  booktitle="Medical Image Computing and Computer Assisted Intervention -- MICCAI 2018",
  year="2018",
  publisher="Springer International Publishing",
  address="Cham",
  pages="247--255",
  isbn="978-3-030-00937-3"
}
