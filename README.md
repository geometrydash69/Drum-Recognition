# Drum-Recognizer
My Project works with image recognition in the Jetson Inference library. You can see and use the code in my-recognition.py.

## The Algorithom:
My Project is The Drum Recognizer. My Project uses images of drums and recognizes what kind of drum it is. how it works is it the set of training images is used for transfer learning, while the validation images are used to evaluate classification accuracy during training, and the test images are to be used after training completes.

## How it works
  
  1.Get a Jetson Nano and install the Jetson Inference library and Python 3 on your system
  
  2.Makes a drums folder in the models directory at jetson-inference/python/training/classification/models
  
  3.Put model_best.pth.tar and resnet18.onnx in jetson-inference/python/training/classification/models/drums

  4.Put the drums folder in jetson-inference/python/training/classification/data
  
  5.Set the variables in terminal
Code Demo:https://youtu.be/M6NI0q29WnY
```
  NET=models/drum  
  DATASET=data/drums
```
  
  6.Input this command to run the model
```
  imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/bass/bass.jpg bass.jpg
```
  7. And if you want to do a diffrent image replace the image and the dataset file path with your own imagefile 

### Hope you find this useful!

