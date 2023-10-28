Video Link: https://youtu.be/JvJiTMs-kqY

<h3>Test Run 1</h3>

Number of Convolutional Layers: 1
Number of Pooling Layers: 1
Pool Size: (2x2)
Sizes of Filters: 32
Number and sizes of hidden layers: 1 with 128 neurons
Dropout: 0.5

Results: 333/333 - 1s - loss: 3.4977 - accuracy: 0.0536 - 734ms/epoch - 2ms/step

Observations:
To start off, I went ahead and tested the same inputs there were used in the lecture video. It turned out to be highly inefficient as it produced an accuracy of only 5.56%. It also has a large loss of 3.50.


<h3>Test Run 2</h3>

Number of Convolutional Layers: 2
Number of Pooling Layers: 2
Pool Size: (2x2)
Sizes of Filters: 32
Number and sizes of hidden layers: 1 with 128 neurons
Dropout: 0.5

Results: 333/333 - 1s - loss: 0.1369 - accuracy: 0.9632 - 957ms/epoch - 3ms/step

Observations:
Doubling the number of Convolutional and Pooling Layers showed a significantly greater accuracy of 96.3% and a smaller loss of 0.137


<h3>Test Run 3</h3>

Number of Convolutional Layers: 3
Number of Pooling Layers: 3
Pool Size: (2x2)
Sizes of Filters: 32
Number and sizes of hidden layers: 1 with 128 neurons
Dropout: 0.5

Results: 333/333 - 1s - loss: 0.2902 - accuracy: 0.9176 - 778ms/epoch - 2ms/step

Observations:
I went ahead to increase the number of Convolutional and Pooling Layers in hopes that it will further increase its accuract. However, the accuracy decreased to 91.8% and the loss increased to 0.290. This suggested that 2 layers of Convolutional and Pooling Layers is optimal.

<h3>Test Run 4</h3>

Number of Convolutional Layers: 2
Number of Pooling Layers: 2
Pool Size: (2x2)
Sizes of Filters: 32
Number and sizes of hidden layers: 2 with 128 neurons
Dropout: 0.5

Results: 333/333 - 1s - loss: 0.1725 - accuracy: 0.9620 - 849ms/epoch - 3ms/step

Observations:
This time, the results were slightly worse than Test Run 2. This suggests that the number of hidden layers need not be increased.


<h3>Test Run 5</h3>

Number of Convolutional Layers: 2
Number of Pooling Layers: 2
Pool Size: (2x2)
Sizes of Filters: 32
Number and sizes of hidden layers: 1 with 128 neurons
Dropout: [0.9, 0.7, 0.5, 0.2, 0.1]

Results: [
    (Accuracy: 5.47% , Loss: 3.50),
    (Accuracy: 80.3%, Loss: 0.626),
    (Accuracy: 96.6%, Loss: 0.133),
    (Accuracy: 97.2%, Loss: 0.127),
    (Accuracy: 95.5%, Loss: 0.210)
    ]

Observations:
Next I wanted to experiment with the Dropout value. I shall represent the results in order of the Dropout values. It seems that increasing the Dropout value reduces accuracy while decreasing the Dropout value increases the accuracy. I also noticed that probably due to overfitting, the difference between the 10th Epoch result and the test result increased as the Dropout value decreased.


<h3>Test Run 6</h3>

Number of Convolutional Layers: 2
Number of Pooling Layers: 2
Pool Size: (2x2)
Sizes of Filters: 64
Number and sizes of hidden layers: 1 with 128 neurons
Dropout: 0.5

Results: 333/333 - 1s - loss: 0.1827 - accuracy: 0.9510 - 1s/epoch - 4ms/step

Observations:
Lastly I wanted to find out how doubling the number of filters will affect the accuracy. This slightly reduced accuracy but more importantly, I observed that it took twice as long for the learning process to complete.
