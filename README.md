# American Sign Language Alphabet Classification
# (COMP_6721-SUMMER-PROJECT)

--> GROUP 07 <--

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
* ![CuPy][CuPy]

## Repository Structure
* Supervised learning Classification with Decision Trees : Jupiter Notebook files for Decision Tree.
* Semi-supervised learning Classification with Decision Trees : Jupiter Notebook files for Decision Tree. 
* CNN: Jupiter Notebook files for CNN.

<!-- GETTING STARTED -->
## Getting Started
### Prerequisites
Depend on the operating system, install the Python3.9 or above

### Installation

### Option 1: Install Anaconda
Installing Anaconda allows to run all Jupyter Notebook files on local computer. If you haven't installed Anaconda, go here: https://store.continuum.io/cshop/anaconda/ This will install everything that you need.

### Option 2: Run on Google Colab
Running on Google Colab without local computer setup, which requires a Google Colab account. If you haven't register Colab, go here: https://colab.research.google.com/signup.

#### Decision Tree with Supervised Learning Classification
1. Download the dataset from [here](https://www.kaggle.com/datasets/kapillondhe/american-sign-language)
2. Depend on running with local computer or Google Colab, change the dataset path in this code section inside Supervised Learning Classification .ipynb files
```python
alphabet_dir = "ASL_Dataset/Train"
```
3. Change following constants in code for hyperparameters( Change only if tuning is required,otherwise skip this step)
```python
    param_grid = {
        'max_depth': [12],
        'criterion': ['gini', 'entropy'],
        'min_samples_split': [2, 5, 10]
    }
```
4. Run Jupyter Notebook, and see the results.

#### Decision Tree with Semi-Supervised Learning Classification
1. Download the dataset from [here](https://www.kaggle.com/datasets/kapillondhe/american-sign-language)
2. Depend on running with local computer or Google Colab, change the dataset path in this code section inside Semi-Supervised Learning Classification .ipynb files
```python
alphabet_dir = "ASL_Dataset/Train"
```
3. Change following constants in code for hyperparameters( Change only if tuning is required,otherwise skip this step)
```python
    param_grid = {
        'max_depth': [12],
        'criterion': ['gini', 'entropy'],
    }
```
4. Run Jupyter Notebook, and see the results.

#### ResNet18
1. Download the dataset from [here](https://www.kaggle.com/datasets/kapillondhe/american-sign-language)
2. Depend on running with local computer or Google Colab, change the dataset path in this code section inside each ResNet .ipynb files
```python
# give path of the input dataset folder
path="/kaggle/input/dataset-10n/dataset-10N"
# give path to save the plot results(Example training vs epoch,loss vs steps,etc)
saveFilePath="/kaggle/input/hyperparameters.pkl"
# give path to save the trained model
saveModelPath="/kaggle/input/"
```
3. Change following constants in code for hyperparameters
```python
#change input dimensions of the image fed to the CNN
inputDimension=(256,256)
#Setting different batch sizes
batch_sizes= [128,64,32]
#Setting different learning rates
learning_rates= [0.00001,0.0001,0.01]
#Setting the number of epochs
epochs=10
#setting the loss function
criterion=nn.CrossEntropyLoss()
```

4. Change the following variables under the "HyperParameter tuning" subsection in the notebook(only if tuning is required,otherwise skip this step)
```python
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

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[Python]: https://img.shields.io/badge/Python-3.9-3776AB.svg?style=flat&logo=python&logoColor=white
[Python-url]: https://www.python.org/
[Pytorch]: https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white
[Pytorch-url]: https://pytorch.org/
[Colab]:https://colab.research.google.com/assets/colab-badge.svg
[Colab-url]: https://colab.research.google.com/notebooks/intro.ipynb
[Matplotlib]: https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black
[Numpy]: https://img.shields.io/badge/Numpy-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black
[Scipy]: https://img.shields.io/badge/Scipy-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black
[scikit-learn]: https://img.shields.io/badge/scikit-learn-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black
[PIL]: https://img.shields.io/badge/PIL-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black
[Pickle]: https://img.shields.io/badge/Pickle-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black
[THOP]: https://img.shields.io/badge/THOP-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black
[CuPy]: https://img.shields.io/badge/CuPy-%23ffffff.svg?style=for-the-badge&logo=Python&logoColor=black
