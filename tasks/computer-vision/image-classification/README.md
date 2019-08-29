# Image Classification


## Environment
- Python 3
- Keras


# Data
- CIFAR-10 for training

# Model
- CNN (Convolutional Neural Network)
```
model = Sequential()
    
    # extract image features by convolution and max pooling layers
    model.add(Conv2D(32, kernel_size=3, padding='same',
                    input_shape=input_shape, activation='relu'))
    
    model.add(MaxPooling2D(pool_size=(2,2)))
    model.add(Dropout(0.25))
    model.add(Conv2D(64, kernel_size=3, padding='same', activation='relu'))
    model.add(MaxPooling2D(pool_size=(2,2)))
    model.add(Dropout(0.25))
    model.add(Conv2D(64, kernel_size=3, padding='same', activation='relu'))
    model.add(MaxPooling2D(pool_size=(2,2)))
    model.add(Dropout(0.25))
    
    # classifiy the class by fully-connected layers
    model.add(Flatten())
    model.add(Dense(512, activation='relu'))
    model.add(Dropout(0.5))
    model.add(Dense(num_classes))
    model.add(Activation('softmax'))
```
# Training
- batch_size=128, epochs=13

# Results
- Test loss: 0.7907178189277649
- Test accuracy: 0.7308

# discussion


