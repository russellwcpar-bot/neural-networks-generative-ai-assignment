# neural-networks-generative-ai-assignment
The model  begins by loading the data, which scales the raw pixel values (0-255) to a range of 0 to 1, helping the neural network converge faster during training. 
Next, using a sequential stack: it starts with an input layer to define the image dimensions, followed by Convolutional layers to extract visual features and Pooling layers to reduce spatial dimensions. 
The data is then turned  into a vector to pass through a hidden layer with ReLU activation
Finally, the model is compiled with the Adam optimizer and trained using Data Augmentation; this step uses an Imagedatagenerator  to create random rotations and flips, to tech the model to recognize objects regardless of their orientation. 
Reflection
Data augmentation enhanced the performance by addressing the problem of overfitting. Creating synthetic variations of training data like rotated, flipped, or zoomed images forces the model to learn the features of an object rather than memorizing  it. This creates a model that generalizes better with unseen data, and results in a more stable and higher test accuracy compared to models trained on a static dataset.
In real world applications, these techniques are vital for domains where data is scarce or expensive to collect.  For instance, data augmentation can help a diagnostic AI recognize a tumor regardless of the angle at which the scan was taken.  By artificially expanding the variety of training examples, organizations can build more reliable and AI systems that perform consistently with edge cases.

Resources 
Python Lessons. (2019, May 17). Building our first Convolutional Neural Networks in Keras step by step. YouTube. https://www.youtube.com/watch?v=4ZkjRv1AGkk
Keras Team. (n.d.). Transfer learning & fine-tuning (Section: Data Augmentation). Keras.io. https://keras.io/guides/transfer_learning/
