# Crop Weed Identification 

This project serves the purpose of identifying weeds amongst crops (in this case, potato crops). This is proof of concept as while a small dataset is used, the dataset could be expanded to have more examples and more categories. Due to the limited data and close images, this isnt perfect. The idea of identifying weeds could be extremely useful in everyday gardening as it is a hassle to pick out weeds among crops.

## The Algorithm

The model is a re-trained ResNet-18 model that uses imagenet to identify if it is a crop or a weed. The model uses pictures of regular potato crops versus common weeds that grow among these crops.  

## Running this project

Libraries required: Jetson-Inference, Python3
1. Download both the resnet18.onnx and data image folder
2. After opening the nano, go to the classification directory
``` $ cd jetson-inference/python/training/classification ```
3. Put the model into the classification/weeds/models folder (might have to create a new folder named 'weeds' and the image folder in the classification/data folder
4. Set the variables
``` $ NET=models/weeds ```
``` $ DATASET=data/weeds ```
5. Run this command to generate an image.
``` $ imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/weed/182.jpg weed1.jpg ```
6. View the generated image in the classification folder.

[View a video explanation here](video link)
