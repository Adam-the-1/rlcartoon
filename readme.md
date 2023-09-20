# Real Life vs Cartoon

 This project was made to help AI better classify whether something is a cartoon or not. I thought of this while looking at detectnet and imagenet datasets, when I noticed it didn’t do a good job identifying cartoon characters (specifically, Gustavo and Brick and Pickachu.)> 

![add image description here](direct image link here)

## The Algorithm

This model is a resnet-18 model that uses imagenet when run. It is retrained using transfer learning on images of cartoon humans and animals, and real humans and animals.

## Running this project

Download the dataset here https://drive.google.com/drive/folders/17r3rLjC0SvAbj6iUpUo9cEFKJwWHMFFi?usp=drive_link
Download and open the jetson inference library.
Change into the following directories with the “cd” command: python, training, classification
Run the following commands into the terminal: NET=models/rlcartoon DATASET=data/rlcartoon, imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/image1.jpg test1.jpg
Upload the image you want to test with the model.
Make sure to with image1 and test1 with the names of your image and what you want to call the test image.

1. Add steps for running this project.
2. Make sure to include any required libraries that need to be installed for your project to run.

[View a video explanation here](video link)

