# Navigation via DQN
This repository contains the implementation of a DQN algorithm and an agent to solve the Bananas environment. The simulation environment stems from [Unity ML-Agents](https://github.com/Unity-Technologies/ml-agents).

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.
This repository is part of a Udacity [Deep Reinforcement Learning Nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893) program submission.

## Dependencies

Set up your python environment to run the code in this repository, follow the instructions below.

1. Create and activate a new conda environment with Python 3.6. If you don't have *Conda*, click here for [Conda installation instructions](https://docs.conda.io/projects/conda/en/latest/user-guide/install/) 

	- __Linux__ or __Mac__: 
	```bash
	conda create --name navi python=3.6
	source activate navi
	```
	- __Windows__: 
	```bash
	conda create --name navi python=3.6 
	activate navi
	```

2. Clone this repository, and navigate to the `dqn-navigation/python/` folder.  Then, install several dependencies.
```bash
git clone https://github.com/ImmanuelXIV/dqn-navigation.git
cd dqn-navigation/python
pip install .
```

3. If you do not run the code on a Mac OSX, download a different version of the ```Banana.app``` file, suitable for Widows, or Linux, place it in the dir, decompress it and change the `file_name` accordingly. 

Downloads
- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

Paths
- **Mac**: `"path/to/Banana.app"` (in the git repo already)
- **Windows** (x86): `"path/to/Banana_Windows_x86/Banana.exe"` 
- **Windows** (x86_64): `"path/to/Banana_Windows_x86_64/Banana.exe"`
- **Linux** (x86): `"path/to/Banana_Linux/Banana.x86"`
- **Linux** (x86_64): `"path/to/Banana_Linux/Banana.x86_64"`
- **Linux** (x86, headless): `"path/to/Banana_Linux_NoVis/Banana.x86"`
- **Linux** (x86_64, headless): `"path/to/Banana_Linux_NoVis/Banana.x86_64"`

(For Windows users) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

(For AWS) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the "headless" version of the environment. You will not be able to watch the agent without enabling a virtual screen, but you will be able to train the agent. (To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the Linux operating system above.)


4. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `navi` environment.  
```bash
python -m ipykernel install --user --name navi --display-name "navi"
```

5. Run the following code and follow the instructions in the notebook (e.g. run all)
```bash
cd dqn-navigation/
jupyter notebook
```

6. Before running code in the `Navigation.ipynb` notebook, change the kernel to match the `navi` environment by using the drop-down `Kernel` menu in the toolbar. 
