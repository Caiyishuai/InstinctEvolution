# Instinct-driven Reinforcement Learning

Evolving Physical Instinct for Morphology and Control Co-Adaption (IROS 2023)
Paper: [https://ieeexplore.ieee.org/document/10342243]

![1712754301453](https://github.com/Caiyishuai/InstinctEvolution/assets/39987654/663504ba-f749-4314-ae6b-1b535a694866)

## Installation

1. Create a new python virtual env with python 3.6, 3.7 or 3.8 (3.8 recommended)
2. Install pytorch 1.10 with cuda-11.3:
   - `pip3 install torch==1.10.0+cu113 torchvision==0.11.1+cu113 torchaudio==0.10.0+cu113 -f https://download.pytorch.org/whl/cu113/torch_stable.html`
3. Install Isaac Gym
   - Download and install Isaac Gym Preview 3 from https://developer.nvidia.com/isaac-gym
   - `cd isaacgym/python && pip install -e .`
   - Try running an example `cd examples && python 1080_balls_of_solitude.py`
   - For troubleshooting check docs `isaacgym/docs/index.html`)

4. Install RL-Games
   * https://github.com/Denys88/rl_games
# Paper and Citation

If you find our work useful, please consider citing us! 

```bibtex
@inproceedings{cai2023task2morph,
  title={Task2Morph: Differentiable Task-Inspired Framework for Contact-Aware Robot Design},
  author={Cai, Yishuai and Yang, Shaowu and Li, Minglong and Chen, Xinglin and Mao, Yunxin and Yi, Xiaodong and Yang, Wenjing},
  booktitle={2023 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
  pages={452--459},
  year={2023},
  organization={IEEE}
}
```


## Usage


Run a simple training process by the following command (set `headless=True` to disable the viewer):

`python train.py task=Dog morph=PSOSearch train=MorphTensor headless=False`

## Settings

We use Hydra to manage configurations
 * https://hydra.cc/docs/intro/

Following main options are currently supported:

```
task: Kangaroo | Raptor | Dog | 
terrain: Flat | Uphill | Downhill | 
train: SinglePPO | MorphTensor 
morph: Fix | PSOSearch
```

See more arguments in `inrl/cfg`.

# Paper and Citation

If you find our work useful, please consider citing us! 

```bibtex
@inproceedings{chen2023evolving,
  title={Evolving Physical Instinct for Morphology and Control Co-Adaption},
  author={Chen, Xinglin and Huang, Da and Li, Minglong and Cai, Yishuai and Wen, Zhuoer and Cai, Zhongxuan and Yang, Wenjing},
  booktitle={2023 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
  pages={6616--6623},
  year={2023},
  organization={IEEE}
}
```
