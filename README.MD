# horseorhuman

* I have built three models to classify horse or human from the freely available dataset on tensorflow called "horseorhuman"
* This dataset contains 1027 training images and 256 test images.
* Images are of dimensions 300 x 300 x 3
* Image label is "0" for horse "1" for human.
* Three models are described as

## model1

* 4 convolution layers, activation is "relu" each conv layer followed by a max pool layer.
* Then 2 fully connected layers.

| Training accuracy | Training loss | Test accuracy | Test loss |
|-------------------|---------------|---------------|-----------|
|      100 %        |   2.2447e-04  |     90.62 %   |   2.5270  |


## model2

* This model is inspired from "ResNet50" model

| Training accuracy | Training loss | Test accuracy | Test loss |
|-------------------|---------------|---------------|-----------|
|      99.9 %       |    0.0102     |     76.95 %   |   2.6     |


* Both are run on Epochs = 100

### model1 vs model2 

![Alt text]( "model1 vs model2")

## model3 

* This is a transfer learning model
* "MobileNetV2" is used.
* Training is set to false
* weights from "imagenet" are used.
* Two additional layers are added in the end.
* With the model frozen, only the newly added additional layers are trained for Epochs = 20.

| Training accuracy | Training loss | Test accuracy | Test loss |
|-------------------|---------------|---------------|-----------|
|      99.8 %       |    0.01       |     100 %     |   0.005   |


### model3 performance

![Alt text]( "model3")


## Remarks 
* Model3 standsout
* Models 1 & 2 are overfitting on Training data.


## ToDo

- [ ] Avoiding overfitting for Models 1 & 2