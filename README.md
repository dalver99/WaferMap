# WaferMap

My small Deeplearning project with https://www.kaggle.com/datasets/qingyi/wm811k-wafer-map/data

Using pkl file as input

Tried ResNet like structure
DenseNet like structure

But a simple DL model with

model3 = Sequential([
Conv2D(32, (3,3), activation='relu', padding='same', input_shape=(32, 32, 1)),
Conv2D(32, (3,3), activation='relu', padding='same'),
MaxPooling2D(pool_size=(2,2)),

    Conv2D(64, (3,3), activation='relu', padding='same'),
    Conv2D(64, (3,3), activation='relu', padding='same'),
    MaxPooling2D(pool_size=(2,2)),

    Conv2D(128, (3,3), activation='relu', padding='same'),
    Conv2D(128, (3,3), activation='relu', padding='same'),
    MaxPooling2D(pool_size=(2,2)),

    Flatten(),
    Dense(128, activation='relu'),
    Dropout(0.5),  # Dropout is correctly placed here
    Dense(y_train.shape[1], activation='softmax')

])

Gives the best result for now!

Will add more..
