# horseorhuman

* I have built three CNN models to classify horse or human from the freely available dataset on tensorflow called "horseorhuman"
* They are built in python using Tensorflow libraries
* This dataset contains 1027 training images and 256 test images.
* Images are of dimensions 300 x 300 x 3
* Image label is "0" for horse "1" for human.
* Three models are described as

## model1

* 4 convolution layers, activation is "relu" each conv layer followed by a max pool layer.
* Then 2 fully connected layers.

| Training accuracy | Training loss | Test accuracy | Test loss |
|-------------------|---------------|---------------|-----------|
|      100 %        |   4.05e-05    |     90.23 %   |   3.8     |


## model2

* This model is inspired from "ResNet50" model

| Training accuracy | Training loss | Test accuracy | Test loss |
|-------------------|---------------|---------------|-----------|
|      98.8 %       |    0.03       |     92.97 %   |   0.45    |


* Both are run on Epochs = 100

### model1 vs model2 

![alt text](https://github.com/elsiery/horseorhuman/blob/main/Accuracy.png)


![alt text](https://github.com/elsiery/horseorhuman/blob/main/Loss.png)

## model3 

* This is a transfer learning model
* "MobileNetV2" is used.
* Training is set to false
* weights from "imagenet" are used.
* Two additional layers are added in the end.
* With the model frozen, only the newly added additional layers are trained for Epochs = 20.

| Training accuracy | Training loss | Test accuracy | Test loss |
|-------------------|---------------|---------------|-----------|
|      99.6 %       |    0.01       |     100 %     |   0.003   |


### model3 performance

![alt text](https://github.com/elsiery/horseorhuman/blob/main/model3.png)


## Remarks 
* Model3 standsout
* Models 1 & 2 are overfitting on Training data.


## ToDo

- [ ] Avoiding overfitting for Models 1 & 2
