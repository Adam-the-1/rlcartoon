# Real Life vs Cartoon

 This project was made to help AI better classify whether something is a cartoon or not. I thought of this while looking at detectnet and imagenet datasets, when I noticed it didn’t do a good job identifying cartoon characters (specifically, Gustavo and Brick and Pickachu.) 

![add image description here](direct image link here)

## The Algorithm

This model is a resnet-18 model that uses imagenet when run. It is retrained using transfer learning on images of cartoon characters, and real humans. (It was only trained on close-up images of faces with generic backgrounds.)

## Running this project

1. Download the dataset here https://drive.google.com/drive/folders/17r3rLjC0SvAbj6iUpUo9cEFKJwWHMFFi?usp=drive_link
2. Download and open the jetson inference library.
3. Change into the following directories with the “cd” command: python, training, classification
4. Run the following commands into the terminal:
```NET=models/rlcartoon```
```DATASET=data/rlcartoon```
```imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/image1.jpg test1.jpg```
7. Upload the image you want to test with the model.
8. Make sure to with image1 and test1 with the names of your image and what you want to call the test image.

[View a video explanation here](video link)

