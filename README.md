# Detection-of-Continuous-Gravitational-Waves
This notebook is implemented in Kaggle's G2NET Hackathon, where the objective of the Hackathon is to find a Gravitational wave in a given noise.


G2Net is a network of Gravitational Wave, Geophysics and Machine Learning. Via an Action from COST (European Cooperation in Science and Technology), a funding agency for research and innovation networks, G2Net aims to create a broad network of scientists. From four different areas of expertise, namely GW physics, Geophysics, Computing Science and Robotics, these scientists have agreed on a common goal of tackling challenges in data analysis and noise characterization for GW detectors.

The ```EfficientNet``` model developed in this notebook achieved an accuray of 0.674 against the 76% of test data. 

## About the Data

The dataset is available in competiton page in [Kaggle](https://www.kaggle.com/competitions/g2net-detecting-continuous-gravitational-waves/data)

Each data sample contains either real or simulated noise and possibly a simulated continuous gravitational-wave signal (CW). The task is to identify when a signal is present in the data (target=1).

Each sample is comprised of a set of Short-time Fourier Transforms (SFTs) and corresponding GPS time stamps for each interferometer. The SFTs are not always contiguous in time, since the interferometers are not continuously online.

The simulated signals are present throughout the entire duration of the set of SFTs in both detectors. The signals are characterised by the location and orientation of the hypothetical astrophysical source as well as two intrinsic parameters: frequency and spin-down. In total there are eight parameters which have all been randomised. These are not provided as part of the data. The typical amplitudes of the resulting signals are one or two orders of magnitude lower than the amplitude of the detector noise.

### Dataset Description
```[train/|test/]``` - folders containing the training and test files; Note: a small example set of training data has been provided, although it is expected that competitors will need to generate additional data for training as described here.

```train_labels.csv``` - a file containing the target labels; 1 if the data contains the presence of a gravitational wave, 0 otherwise. (Please note the presence of a small number of files labeled -1. Physicists are currently unable to determine the status of these files.)


## Installation
1. Download this repo in a zip file by clicking this [link](https://github.com/Naidu-Suraj-Vardhan/Detection-of-Continuous-Gravitational-Waves/archive/refs/heads/main.zip) or execute this from the terminal: ```git clone https://github.com/Naidu-Suraj-Vardhan/Detection-of-Continuous-Gravitational-Waves.git ```.
2. Install the [Anaconda Environment](https://anaconda.org/anaconda/anaconda-navigator) .
3. Navigate to the repo directory and create a conda environment. Then install the dependencies with ```pip install -r requirements.txt```.
4. Run the  ```g2netgo.ipynb ```.

## Dependencies
1.  Numpy
2. Pandas
3. Matplotlib
4. PyTorch
5. Timm (PyTorch Image models)
6. Scikit-Learn
