# Crop Weed Identification 

This project servers the purpose of identifying weeds amongst crops (in this case, potato crops). This is proof of concept as while a small dataset is used, the dataset could be expanded to have more examples and more categories. The idea of identifying weeds could be extremely useful in everyday gardening as it is a hassle to pick out weeds among crops.

## The Algorithm

The model is a re-trained ResNet-18 model that uses imagenet to identify if it is a crop or a weed. I used pictures of regular potato crops versus common weeds that grow among these crops.  

## Running this project

Libraries required: Jetson-Inference, Python3
1. Download both the resnet18.onnx and data image folder
3. After opening the nano, go to the classification directory
``` $ cd jetson-inference/python/training/classification ```
4. Set the variables
``` $ NET=models/weed ```
``` $ DATASET=data/weed ```
5. Run this command to generate an image.
``` $ imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/potato/138.jpg crop1.jpg ```
6. View the generated image in the classification folder. - Alternatively, the result could be viewed in the terminal

[View a video explanation here](video link)
