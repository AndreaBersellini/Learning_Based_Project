# Learning_Based_Project

The file data_level_fusion_U-NET.ipynb contains a model based on the Data-Level Fusion approach. Using raw images, it employs the DLFDataset(Dataset) class to generate a dataset that includes the early fusion of camera and LiDAR images, along with ground truth depth maps.
This dataset is then passed in batches to the neural network for training using the train(model, epochs) function.
Every 5 batches of data, a prediction is displayed, and a backup of the model is saved to allow for monitoring of the results.
The files camera_lidar_separate_U-NET.ipynb and ensamble_dataset_generation.ipynb are used similarly to make predictions on the raw data separately and to generate a dataset for use during the stacking procedure based on the Decision-Level Fusion approach.
Finally, the file decision_level_fusion_U-NET.ipynb contains the ensemble learning model to merge the predictions of the two individual models. Unlike the previous models, this network takes as input single-channel grayscale images and outputs equivalent single-channel images.
