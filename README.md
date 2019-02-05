# FINAL-MACHINE-LEARNING-PROJECT

#DATA SET LINK : https://drive.google.com/file/d/1w-LbOkhXheyJv5vpkH608wMnimueZmUS/view?ts=5c062484


Classification of Blood Cell Images into Cancerous and Non-Cancerous types:


We have 10661 single blood cell images of which 7272 are non-cancerous and 3389 are cancerous. The steps we have followed for classifying the images are given below:

Preprocessing:
For preprocessing our images, we have used filters for varying saturation, contrast, brightness, sharpness etc. From all these filters, emboss filter was the most efficient one in increasing our accuracy.


#Running Models:

1.Ensemble Model:
        For Ensemble learning, we have run 3 CNN models namely:
        1. MobileNetV2
        2. DenseNet121
        3. NasNetMobile
        and at last, we took 3 separate results from the 3 models and taken max voting in prediction stage.
        
        Result obtained : Accuracy - 75.33%

#Concatenation Model 

        It joins( concatenate ) the output of features extracted by ( output  of globalpooling layer from this two model)   MobileNET   and   DenseNet121. 

        This is stronger model. It overfits badly, so we didn't prepare final result from it.


#Single Model:
        We ran Mobilenet as a single model. We used weights from imagenet as initial weights from covolutional layers. And drop the fully connected layer in the top and used our custom dense layer.
        Accuracy : 80.0%

#AutoEncoder Model:
        We trained Auntoencoder and then used the encodeder part of the autocoder for classification.
        accuracy : 81.79%
        this our best performing model.
        confusion matrix:
        [[326 144]
        [112 841]]



Result:
The Accuracies of the models implemented on our dataset are given below:

Ensemble: 75.33
Single: 80.0
Autoencoder: 81.79
