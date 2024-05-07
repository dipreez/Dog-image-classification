<img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=Python&logoColor=white"/> <img src="https://img.shields.io/badge/NumPy-013243?style=flat&logo=NumPy&logoColor=white"/> <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=TensorFlow&logoColor=white"/>
# Dog-image-classification
This repository contains CNN model that can classify dog images by their breed.

# Model structure
We designed and trained a CNN model with the following structure.
![ai1](https://github.com/dipreez/Dog-image-classification/assets/50349104/17c79441-39f1-4930-8715-a80070497c3e)
![ai2](https://github.com/dipreez/Dog-image-classification/assets/50349104/656c23a5-02a2-4f2d-8f96-ed7ddb3f60d9)

# Initial training result
![ai3](https://github.com/dipreez/Dog-image-classification/assets/50349104/a8657e63-72ca-4e94-816e-3ef4d0757f9e)
The graph above shows the initial training results of the model (the x-axis is the number of iterations). Training accuracy continues to increase over 10 iterations, near 100%. However, the validation accuracy is tied near 20% after the second iteration. We can see similar situation on the trainig loss. Training loss decreases over 10 iterations. However, validation loss rather rises after second iteration. This is a typical symptom of overfitting, so further improvement is needed.

# Model improvements
## Data augmentation
One causes of overfitting is insufficient learning data. Since our dataset contains approximately 130 images for each class subject, this might be insufficient to train our CNN model. In this case we can create new data by applying random transformations to the data we have. In this project, this is implemented this by using the Keras preprocessing layer
## Drop out
Dropout, another way to solve overfitting, is aplied into the model. Drop out means to randomly selects a node of a model for each period and remove it.

# Final training result
![ai4](https://github.com/dipreez/Dog-image-classification/assets/50349104/80495fe7-a8d5-4477-a173-d308bdeafe77)
Above graph is the training result after the improvement.
