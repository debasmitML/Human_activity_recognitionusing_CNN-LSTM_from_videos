1. The dataset has been taken from UCF50 video dataset. 50 classes are present in the dataset. From 50 classes, 3 classes have been taken for classification namely 'Biking','JumpRope','Nunchucks'.
From each video, 15 frames have been taken. Then pre-processing has been done on these video frames. The shape of the training set is (310,15,71,71,3) and the testing set is (133,15,71,71,3). Each 
video frame's (RGB image) width and height is 71. So, 310 and 133 videos with 15 frames have been present in the training and testing set respectively.

2. Then the training and testing dataset have been reshaped into (4650,71,71,3) and (1995,71,71,3) respectively. Then VGG16 model has been used for features extraction. After using VGG16, 
training and testing features shape are (4650,2048) and (1995,2048) respectively.

3. Then again, training and testing features have been reshaped into (310,15,2048) and (133,15,2048) respectively. Now the features again have been converted into time-series data. Then LSTM
has been used for the classification. Dropout layer, regularizer has been used to overcome the overfitting problem.

4. In the result folder, the plots of Confusion Matrix and Training, validation loss and Training, Validation loss are present.

5. VGG16+LSTM.h5 is the saved model.

6. The code has been written on Google Colab.
 
