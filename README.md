# DeepVideoDenoising

Requirements : 
1. Python 3.6+
2. OpenCV-python
3. Pandas, Numpy, Json
4. PyTorch, use cuda for accelerated training and inference.
5. tqdm for progress bar


Download Deep Video Deblurring Dataset : https://github.com/shuochsu/DeepVideoDeblurring
http://www.cs.ubc.ca/labs/imager/tr/2017/DeepVideoDeblurring/DeepVideoDeblurring_Dataset.zip

Use the InfoExtractor.ipynb to prepare Info.csv for each of the dataset qualitative and quantitative dataset.
We are using this this file to sequentially iterate through different videos.

Then use the notebooks for model training or predicting.
We can load one of the pretrained weight provided in the "SaveWeights"

The architecture of the models are described below:
\

![conv3dDiagram](https://user-images.githubusercontent.com/83718299/164873169-d811294f-3d1a-4001-afa2-338ab7276d3c.jpg)

\

![convLSTMDiagram](https://user-images.githubusercontent.com/83718299/164873173-55c08cc1-1647-4558-a839-8ce9b1020b29.jpg)

The result from the models is below:
The top left represent : Input\
The top right represent : Ground Truth\
The down left represent output from : Conv3d\
The down right represent output from : ConvLSTM\



https://user-images.githubusercontent.com/83718299/164873540-97e01c5c-1668-4b7c-acbf-e4ac8fb8fc65.mp4



Furture Work:
ConvLSTM requires a powerful gpu to be trained properly. 
And currently all the input and output resolution is set to 640x360.
We aim to make the model work on patches to generate a proper result.

References:
1. https://github.com/shuochsu/DeepVideoDeblurring
2. https://github.com/KimUyen/ConvLSTM-Pytorch
