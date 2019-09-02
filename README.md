This is implemented on https://github.com/sgrvinod/a-PyTorch-Tutorial-to-Object-Detection
Following the instruction of “PyTorch Tutorial to Object Detection”, we could build the working environment. Besides those, some codes are added or modified for more functions.

The main idea of this project is to create the "demo.py" through modifying the "detect.py". By using the tracking method in “pytorch-detect-to-track” to link the frame, we could achieve our aim of tracking the objects with SSD detector.
- First step is to get the target boxes and corresponding scores for the detected objects. To achieve this aim, the “detect1” is written based on original “detect” function to only obtain the boxes and scores without the filtering. In this way, we could create the “VideoPostProcressor” using them as suitable inputs.
- Applying the threshold, we could obtain the optimal paths with the methods in “VideoPostProcressor”. Combining the paths and images helps us get the plotted frames.
- Read and write the target video which is made of these plotted frames.

Besides, there are some codes to train and test the models on the ImageNet. And you could apply the "create_imagenet_data_lists.py" to get the processed dataset from the original ImageNet.