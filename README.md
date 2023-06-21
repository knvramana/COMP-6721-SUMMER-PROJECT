# American Sign Language Alphabet Classification
# (COMP_6721-SUMMER-PROJECT)

--> GROUP 07 <--
<!-- ABOUT THE PROJECT -->
## About The Project
ASL is accepted by many high schools, colleges, and universities in fulfillment of modern and “foreign” language academic degree requirements across the United States. This project aims for ASL alphabet classification to facilitate better understanding and interaction with the ASL community. The goal is to develop a reliable and efficient tool for ASL alphabet recognition, which can bridge the communication gap between individuals with hearing impairments and those who do not know sign language. we will use PyTorch to build and train a deep learning model to classify images to classes.

### Built With
* [![Python][Python]][Python-url]
* [![Pytorch][Pytorch]][Pytorch-url]
* [![Colab][Colab]][Colab-url]
* ![Matplotlib][Matplotlib]
* ![Numpy][Numpy]
* ![Scipy][Scipy]
* ![scikit-learn][scikit-learn]
* ![PIL][PIL]
* ![Pickle][Pickle]
* ![THOP][THOP]

## Repository Structure
*CNN: Notebooks for CNN.


#### ResNet18
1. Download the dataset from [here](https://www.kaggle.com/datasets/kapillondhe/american-sign-language)
2. Depend on running with local computer or Google Colab, change the dataset path in this code section inside each ResNet .ipynb files
```python
# Other constants
model_save_name = 'resnet_3_categories_model.pth'
statistic_save_name = 'resnet_3_categories_statistic.pkl'
statistic_path = F"/content/drive/My Drive/comp6721-project/{statistic_save_name}"
model_path = F"/content/drive/My Drive/comp6721-project/{model_save_name}" 

ROOT_PATH = '/content/drive/MyDrive/comp6721-project/datasets/dataset-3/'
training_path = f'{ROOT_PATH}/train'
validation_path = f'{ROOT_PATH}/val'
evaluation_path = f'{ROOT_PATH}/test'
```
3. Change following constants in code for hyperparameters
```python
# Model training constants
batch_size = 32
num_epochs = 10

# Loss function & optimizer constants
lr = 0.0001

# Image constants
image_size = 256
mean = [0.554, 0.450, 0.343]
std = [0.231, 0.241, 0.241]
num_classes = 3

4. Change the following variables under the "HyperParameter tuning" subsection in the notebook(only if tuning is required,otherwise skip this step)
#change input dimensions of the image fed to the CNN
inputDimension=(256,256)
#different batch sizes
batch_sizes=[128,64,32]
#different learning rates
learning_rates= [0.00001,0.0001,0.01]
#Setting the number of epochs
epochs=10
``` 
5. Run Jupyter Notebook, and see the results
