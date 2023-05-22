# deep-learning-challenge REPORT

The report should contain the following:

Overview of the analysis: 

The purpose of this analysis is to create a tool for Alphabet Soup that can help it detect and select applicants for funding with the best chance of success in thier ventures. 

Results: 
Data Preprocessing
What variable(s) are the target(s) for your model?

The "IS_SUCCESSFUL" variable is the target for my model. we want to build a model around the other variables to determine if this specific variable can be forcasted/predicted. 

What variable(s) are the features for your model?

the features of the model are mostly the other columns in the data set except for the identification columns (EIN and NAME)

What variable(s) should be removed from the input data because they are neither targets nor features?
Columns (EIN and NAME)



Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
I used anywhere between 1 and 30, I used a variation of functions from 'relu','tanh', and 'ELU'. I just really tried to tune the model the best I could. 


Were you able to achieve the target model performance?

Not 75% but I am still working on it. 

What steps did you take in your attempts to increase model performance?

I changed the neurons, I changed the layers, I tried different activation functions

Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

The provided code defines a deep learning model for binary classification tasks. The model architecture is created using the Keras Sequential API and allows for hyperparameter tuning using the Keras Tuner library.

The key features of the model are as follows:

Activation Function: The activation function for the hidden layers is determined by the Keras Tuner, with 'relu' and 'tanh' as the options in the original code. However, you can customize the activation options based on your specific requirements.

Number of Layers and Neurons: The number of layers and the number of neurons in each layer are also determined by the Keras Tuner. The code allows for tuning the number of layers (from 1 to 5) and the number of neurons in each layer (from 1 to 30) with a step size of 5.

Output Layer: The model includes a single neuron output layer with a sigmoid activation function, which is suitable for binary classification problems.

Compilation: The model is compiled with the 'binary_crossentropy' loss function, 'adam' optimizer, and 'accuracy' metric for evaluation.

In terms of a recommendation for solving the classification problem using a different model, it would depend on the specific characteristics of the problem, dataset, and the desired trade-offs between accuracy, interpretability, and computational complexity. Here's a general recommendation:

Maybe consider using a pre-trained convolutional neural network (CNN) such as VGG16, ResNet, or Inception, followed by a few dense layers for classification tasks.
