# california_housing
 Neural network model for regression on the California housing dataset using TensorFlow

The given code implements a simple neural network model for regression on the California housing dataset. The code imports necessary libraries like matplotlib, numpy, tensorflow, fetch_california_housing from sklearn.datasets, train_test_split, StandardScaler from sklearn.preprocessing and pandas. The dataset is loaded into the variable housing using the fetch_california_housing() function from the sklearn.datasets module. The dataset is then split into train, validation and test datasets using the train_test_split() function from sklearn.model_selection. The features are scaled using StandardScaler() from sklearn.preprocessing.

The neural network model is built using the Sequential() model from tf.keras.models. The layers are defined using Dense() from tf.keras.layers. The model consists of 6 layers. The first five layers have 40, 30, 20, 10 and 5 neurons, respectively with ReLU activation. The final layer has 1 neuron without any activation function. The loss function is set to "mse" and the optimizer is set to "sgd".

Callbacks like ModelCheckpoint, EarlyStopping and TensorBoard are defined using tf.keras.callbacks. The ModelCheckpoint callback saves the best model weights during training. The EarlyStopping callback stops the training process early if the validation loss does not improve for a certain number of epochs. The TensorBoard callback creates a log of the training progress that can be visualized using TensorBoard.

The model is trained using fit() method of Sequential() model. The fit() method takes in the train, validation and test datasets, number of epochs and the defined callbacks as arguments. The history of the model is stored in a variable history.

Finally, the training process is visualized using TensorBoard.
