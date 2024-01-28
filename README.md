# Reweighted-Behavior-Cloning
Repository that holds code for for CSCE: 689 Deep Reinforcement Learning's Course Project. Here we briefly go over the different parts of the repository.

# Authors
1. Vijay Anand Raghava Kanakagiri (vijay7anand@tamu.edu)
2. Shubham Parashar (shubhamprshr@tamu.edu)


# Overview
The repo contains source code for our project, Reweighted-Behavior-Cloning. We derive motivation from the following repos:
1. https://github.com/YyzHarry/imbalanced-regression - FDS
2. https://github.com/nerdimite/behavioral-cloning - PyTorch starter kit for behavior cloning.
3. https://github.com/upul/Behavioral-Cloning - Image Augmentations and dataset for the Udacity Simulator.
4. https://github.com/SteiMi/denseweight -  DenseWeight and corresponding DenseLoss

# Datasets
1. Udacity: We have used the dataset collected by https://github.com/upul/Behavioral-Cloning. It has different Left, Center and Right viewpoint images. Our training has been done using this dataset of 23000 images. Please download the dataset from: https://drive.google.com/file/d/1Is3attEWWhGMJlV2ffEbu2sC10ex3wcq/view?usp=sharing

The stats for the dataset are as follows:

<img width="416" alt="image" src="https://user-images.githubusercontent.com/113248148/205827140-99a92ded-17c1-4e71-be72-3f1c21af8106.png">


2. DonkeyCar: For our own educational purposes we have collected data on the DonkeyCar simulator (https://docs.donkeycar.com/guide/deep_learning/simulator/). Please download the dataset from: 
https://drive.google.com/file/d/1kU2eZ9NLhgOPE7MrnNx7tG_KPRbWeVOH/view?usp=share_link

# Training
We have used Colab for training our models. If you would like to do the same, we recommend downloading the Training-Notebook.ipynb from `/train` folder. 
Steps are as follows:
1. Upload the Notebook on Colab.
2. Download any compressed dataset from /Datasets.
3. Upload the same on your google drive and point accordingly in the Colab notebook.
<img width="677" alt="image" src="https://user-images.githubusercontent.com/113248148/205719301-bdea6227-2de1-4f1f-9b5f-8db0c197cd45.png">
4. After the dataset has been extracted, you are ready to go! Models shall be saved in the /models folder.

# Testing
For Testing please refer to the code in /test folder. The steps are as follows:
1. Download and install the Udacity Autonomous Car Simulator. (https://github.com/udacity/self-driving-car-sim)
2. After that create a conda environment using the requirements.txt specified in the test folder. 
3. Lastly run `drive.py` with the following command. Make sure to pass the model_name you would like to test.

# Models
We have some pre-trained models in PyTorch available. Note that each model has been trained with a batch size of 32, learning rate=1e-4. The models have been explained below:
1. Vanilla-BC.pth: A CNN inspired architecture for Vanilla Behavior Cloning. This has no changes or modifications.
2. Best-DenseLoss-alpha-0.8-BC.pth: This is the state of the art model for our set of experiments. It generalizes very well on less frequently seen steering angles as well.
3. DenseLoss-alpha-1.0.pth: A model with alpha=1.0 for DenseLoss.
4. DenseLoss-alpha-1.2.pth: A model with alpha=1.2 for DenseLoss.
5. FDS.pth: A model with FDS smoothing applied.
6. FDS-DenseLoss-alpha-0.8.pth: A model which trains using both FDS and DenseLoss, alpha was 0.8.

# Demos and Videos
We have captured screen recordings for all the above models, in this folder. They have been organized as per name.
https://drive.google.com/drive/folders/13jPhnE_FFQDmREW7dpUCF9JxNZ7lMYur

For a quick summary demo of different approaches:
https://youtu.be/-Ibj_SYtF-w

