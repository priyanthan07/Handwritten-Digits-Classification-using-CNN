# Handwritten-Digits-Classification-using-CNN
Implementing Convolutional Neural Network For Handwritten Digits Classification

## Required Libraries
    => tensorflow
    => keras
    => matplotlib
    => numpy
    => seaborn

## Dataset
    Data is loaded from keras datasets
    => minist
## Data processing
    => train and test data reshape
    => scaling the data

## Model building

     CNN = models.Sequential([
    
        layers.Conv2D(filters = 32, kernel_size=(3,3), activation= "relu", input_shape = (28, 28,1)),
        layers.MaxPooling2D(2,2),
        layers.Conv2D(filters = 32, kernel_size=(3,3), activation= "relu"),
        layers.MaxPooling2D(2,2),
        layers.Conv2D(filters = 64, kernel_size=(3,3), activation= "relu"),
        layers.MaxPooling2D(2,2),

        layers.Flatten(),
        layers.Dense(30, activation= "relu"),
        layers.Dense(10, activation= "softmax"),
     ])

## Compiling

    CNN.compile( optimizer = "adam",
            loss = "sparse_categorical_crossentropy",
            metrics = ["accuracy"]
    )

## Evaluation
    loss: 0.1328 
    accuracy: 0.9578

## classification_report
    precision    recall  f1-score   support

           0       0.96      0.98      0.97       980
           1       0.85      1.00      0.92      1135
           2       0.95      0.93      0.94      1032
           3       0.85      0.96      0.90      1010
           4       0.92      0.96      0.94       982
           5       0.92      0.95      0.93       892
           6       0.98      0.94      0.96       958
           7       0.69      0.97      0.81      1028
           8       0.99      0.54      0.70       974
           9       0.97      0.66      0.78      1009

    accuracy                           0.89     10000
    macro avg      0.91      0.89      0.88     10000
    weighted avg   0.90      0.89      0.88     10000

    
