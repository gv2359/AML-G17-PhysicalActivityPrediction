# Physical Activity Prediction

## Data collection :

The data that will be used is to be stored in the folder 'data' from the [dataset](https://archive.ics.uci.edu/dataset/231/pamap2+physical+activity+monitoring)

These files should be dowloaded from the above link and stored in the data folder - 
`subject101.dat, subject102.dat, subject103.dat, subject104.dat, subject105.dat, subject106.dat, subject107.dat, subject108.dat, subject109.dat`

Please refer to the readme.pdf and other docs in the 'data' folder for the data collection related information that was provided with the dataset.

Using this informatation, The raw data from various subjects are collected by running the `Data_Collection.ipynb` python notebook. This collects the data from the various subject files and stores into a single .csv file (`compiled_raw_data.csv`) in the same folder for further analysis.

## Exploratory Data Analysis :

We use the `compiled_raw_data.csv` data file to perform exploratory data analysis using `Data_EDA_Cleanup.ipynb` python notebook.

Here, We perform EDA and collect useful information from the data, and perform feature extraction using PCA (Principle Component Analysis) and other techniques. We remove the unnecessary columns and rows based on the exploratory analysis and store the final data as `final_data.csv` in the same folder

This final data is normalized (standard) and the target data is label encoded. 

Activity IDs are encoded and the mappings are : 

`{0:'lying',1:'sitting',2:'standing',3:'walking',4:'running',5:'cycling',6:'nordic_walking',7:'ascending_stairs',8:'descending_stairs',9:'vacuum_cleaning',10:'ironing',11:'rope_jumping'}`

## Training and Evaluation:

We use the `final_data.csv` from the folder `data`, which has the final set of features and cleaned data to perform training on various machine learning algorithms. The various training algorthms are trained in the python notebooks prefixed with 'Train_'.

The machine learning algorithms that we train the data on includes :

- Logistic Regression
- Decision Trees
- Random Forests
- Support Vector Machines (SVM)
- Deep Neural Networks

Each algorithms and the techniques used in these algorithms are explained below:

### Logitic Regression

### Decision Trees

### Random Forests

### Support Vector Machines

### Deep Neural Networks


## Analysis

Here, We collect the model performance from each of the algorithms and pick the best model to be used with it's best hyperparameters.

We finally get the final model to be deployed ( `deployed_model`). 