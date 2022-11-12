# Mask Wear Detector
## Table of contents
* [Demo](#demo)
* [Overview](#overview)
* [Project Goal](#project-goal)
* [Technical Aspects](#technical-aspects)
* [Feature Request](#feature-request)
* [Used Technologies](#used-technologies)
* [Appendix](#appendix)
* [FAQ](#faq) 
* [Author](#author)
* [License](#license)
* [Feedback](#feedback)

## Demo

• Overview of Mask Wear Detector :

![link1](https://im5.ezgif.com/tmp/ezgif-5-57af00c1f7.gif)

## Overview

COVID-19 mask detector could potentially be used to help ensure your safety and the
safety of others.
Approach: A simplified approach to achieve this purpose using some basic Machine
Learning packages like TensorFlow, Keras, and OpenCV. This method
detects the face from the image correctly and then identifies if it has a mask on it or not.

The goal of this project is to build a robust solution that should detect and identify the person is
wearing mask or not. With a varying distance and color combination, it should work for
any person.

Overall, 1143 images for training and 286 images for validation were used. Transfer Learning (InceptionV3) is used in this project to get the best results with limited the dataset.
## Project Goal
This complete poject is made as a part of Data Science Internship at [iNeuron.ai](https://internship.ineuron.ai/).
## Technical Aspects

• 	𝐃𝐚𝐭𝐚 𝐏𝐫𝐞𝐩𝐚𝐫𝐚𝐭𝐢𝐨𝐧 : This consists of downloading the dataset from [Flickr-Faces-HQ (FFHQ)(https://github.com/NVlabs/ffhq-dataset), Data Visualization and Data Preprocessing. Using Image Data Generator we scaled, shuffled, inserted target size as 150x150, and chose appropriate class mode (binary) with the batch size of 32 for training and validation data. 

• 	𝐌𝐨𝐝𝐞𝐥 𝐃𝐞𝐯𝐞𝐥𝐨𝐩𝐦𝐞𝐧𝐭 : After data preprocessing, we use the processed data to train the model. I used Transfer Learning method with InceptionV3 model by importing local weights for the model with TensorFlow Hub. The final model comprised Dense layer with sigmoid activation function.  The model is compiled with RMSprop optimizer (learning rate= 0.0001) and Binary Cross Entropy loss function. 

• 	𝐌𝐨𝐝𝐞𝐥 𝐑𝐞𝐬𝐮𝐥𝐭𝐬  :
The model was trained with 6 epochs. Training process ended with 99.36% accuracy and 0.0285 loss on training dataset and 98.97% accuracy, 0.0396 loss on validation dataset. Model was saved as “.h5” file. The model performed very well on live Webcam.

## Feature Request

If you find a bug (the website couldn't handle the query and / or gave undesired results), kindly email me (mahammad.ojagzada@outlook.com) by including your search query and the expected result.

If you'd like to request a new function, feel free to do so by opening an issue here. Please include sample queries and their corresponding results.

## Used Technologies
![Logo1](https://opencv.org/wp-content/uploads/2021/02/1_HfZmZayUqnYioPC9qTfd4A.png)

![Logo3](https://static.javatpoint.com/tutorial/tensorflow/images/tensorflow-tutorial.png)

## Appendix
Link for video regarding to the explanation of the project :  
https://drive.google.com/file/d/1PJjjtYs4YO_-XqkUtXAT9Eb5XGx90flY/view?usp=sharing

Link for App Documentation :    
https://github.com/mahammadodj/iNeuron-Internship-Project/tree/master/Documents

## FAQ
#### What is the source of data?

MaskedFace-Net is a dataset of human faces with a correctly or incorrectly worn mask (133,783 images) based on the dataset [Flickr-Faces-HQ (FFHQ)](https://github.com/NVlabs/ffhq-dataset).

#### What techniques were you using for data pre-processing?

Image Augmentation technique was not applied to the dataset in this project as it would take much more training time.  As I preferred Transfer Learning (InceptionV3),  I simply used shuffling, scaling in Image Data Generator.

#### How training was done or what models were used?

InceptionV3 model was used and training process  consisted of 6 epochs.  Local pre-trained weights  applied to the model. The final model comprised Dense layer with sigmoid activation function. Training ended with 99.36% accuracy and 0.0285 loss on training dataset and 98.97% accuracy, 0.0396loss on validation dataset. 

#### How detection is done?

The trained model is able to identify faces with trained classifier - “haarcascade_frontalface_default.xml”.  The model was tested with webcam for detection in real-time and it performed very well. 

## Author
 [Mahammad Ojagzada](https://www.linkedin.com/in/mahammed-ojagzada/)

## License

[MIT](https://choosealicense.com/licenses/mit/)

Copyright 2022 Mahammad Ojagzada

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Feedback

If you have any feedback, please reach out to me at mahammad.ojagzada@outlook.com.
