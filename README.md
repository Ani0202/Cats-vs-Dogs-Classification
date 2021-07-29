# Cats-vs-Dogs-Classification
Build and train a convolution neural network for classifying images of Cats and Dogs

Cats vs Dogs classification is a fundamental Deep Learning project for beginners.

## The Dataset
https://www.kaggle.com/chetankv/dogs-cats-images

I have made two models. One is the CNN model which is having the following layers:
_________________________________________________________________
Layer 
=================================================================
zero_padding2d (ZeroPadding2 (None, 226, 226, 3)       0         
conv2d (Conv2D)              (None, 224, 224, 32)      896       
batch_normalization (BatchNo (None, 224, 224, 32)      128       
max_pooling2d (MaxPooling2D) (None, 112, 112, 32)      0         
dropout (Dropout)            (None, 112, 112, 32)      0         
conv2d_1 (Conv2D)            (None, 110, 110, 32)      9248      
batch_normalization_1 (Batch (None, 110, 110, 32)      128       
dropout_1 (Dropout)          (None, 110, 110, 32)      0         
conv2d_2 (Conv2D)            (None, 108, 108, 64)      18496     
batch_normalization_2 (Batch (None, 108, 108, 64)      256       
max_pooling2d_1 (MaxPooling2 (None, 54, 54, 64)        0         
dropout_2 (Dropout)          (None, 54, 54, 64)        0         
conv2d_3 (Conv2D)            (None, 52, 52, 64)        36928     
batch_normalization_3 (Batch (None, 52, 52, 64)        256       
dropout_3 (Dropout)          (None, 52, 52, 64)        0         
conv2d_4 (Conv2D)            (None, 50, 50, 128)       73856     
batch_normalization_4 (Batch (None, 50, 50, 128)       512       
max_pooling2d_2 (MaxPooling2 (None, 25, 25, 128)       0         
dropout_4 (Dropout)          (None, 25, 25, 128)       0         
conv2d_5 (Conv2D)            (None, 23, 23, 128)       147584    
batch_normalization_5 (Batch (None, 23, 23, 128)       512       
dropout_5 (Dropout)          (None, 23, 23, 128)       0         
conv2d_6 (Conv2D)            (None, 21, 21, 256)       295168    
batch_normalization_6 (Batch (None, 21, 21, 256)       1024      
max_pooling2d_3 (MaxPooling2 (None, 10, 10, 256)       0         
dropout_6 (Dropout)          (None, 10, 10, 256)       0         
conv2d_7 (Conv2D)            (None, 8, 8, 256)         590080    
batch_normalization_7 (Batch (None, 8, 8, 256)         1024      
dropout_7 (Dropout)          (None, 8, 8, 256)         0         
average_pooling2d (AveragePo (None, 4, 4, 256)         0         
flatten (Flatten)            (None, 4096)              0         
dense (Dense)                (None, 128)               524416    
dropout_8 (Dropout)          (None, 128)               0         
dense_1 (Dense)              (None, 128)               16512     
dense_2 (Dense)              (None, 1)                 129       
Training set accuracy: 95%
Validation Set accuracy: 93%


I have also used VGG 16 with fine tuning to achieve a 98% accuracy.
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
input_3 (InputLayer)         [(None, 224, 224, 3)]     0         
_________________________________________________________________
sequential_4 (Sequential)    (None, 224, 224, 3)       0         
_________________________________________________________________
tf.__operators__.getitem (Sl (None, 224, 224, 3)       0         
_________________________________________________________________
tf.nn.bias_add (TFOpLambda)  (None, 224, 224, 3)       0         
_________________________________________________________________
vgg16 (Functional)           (None, 7, 7, 512)         14714688  
_________________________________________________________________
average_pooling2d_1 (Average (None, 3, 3, 512)         0         
_________________________________________________________________
flatten_1 (Flatten)          (None, 4608)              0         
_________________________________________________________________
dense_3 (Dense)              (None, 1)                 4609      
=================================================================
Total params: 14,719,297
Trainable params: 7,084,033
Non-trainable params: 7,635,264

Training set accuracy: 99%
Test Set accuracy: 98%
