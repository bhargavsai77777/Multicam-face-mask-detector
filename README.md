Three Important steps to predict if the objects in the video has a mask or not.
1) we have to capture the video using  imutils.video import VideoStream once done, we read the video into frames.
2) once we have the frame, we first need to detect the face object in the frame using opencv deep neural network called readnet. this will draw the bounding box around the face 3)now we cut the face and send this to the masknet which is nothing but a mask detector neural net which is where actual mask detection is taking place.




Three important things:
1)how the face takes the image and detect the face
2)whats happening in the mask net detector
3)how you are starting the computers camera using video stream.



In mask detector instaed of using convolution we are using mobility nets as a base part of the network.




for face detction readnet uses:
single shot multiobject detector which uses resnet 10 as a architecture

for mask detection we use:
mobilenetsv2 because they are also a good feature extraction nets avilable in the market but lot faster than any other cnn available  as they store less parametres which deceraese in parameters , there is decrease in computational power, faster the process
inputs--> mobilenetv2-->max pool-->fully connected NN-->OUTPUT
