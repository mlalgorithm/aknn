# Adaptive k-nearest neighbor

Adaptive k-nearest neighbor is a general framework for variable selection in high dimensional data. It can take advantage of multiple CPU cores to significantly accelerate the running time.

|Author|Weixing Dai|
|---|---
|E-mail|daiweixinghk@gmail.com

## Example

### To train:

```Bash
python aknnTrain.py --data 'data/leukemia_train.csv'
```
The result of training on leukemia data set:

![github](https://github.com/mlalgorithm/imageache/blob/master/aknn_train.png)  

### To predict on test data :

```Bash
python aknnPredict.py --data 'data/leukemia_test.csv'
```
The result of prediction on leukemia test set by the trained model:

![github](https://github.com/mlalgorithm/imageache/blob/master/aknn_test.png)  

## Usage
```Bash
aknnTrain.py
```
Function: Training by Adaptive k-nearest neighbor

usage: aknnTrain.py [-h] [--data D] [--ne N] [--out O] [--cpu C]

optional arguments:  
-h, --help　  show this help message and exit  
--data D　    data to be trained, the last column is the labels (required)  
--ne N 　     maximum number of feature subsets evaluated in each epoch. the default is 2000000 (optional)  
--out O 　    filename to keep the output of training. the default is lbsmodel.npz (optional)    
--cpu C 　    the number of CPUs to use. the default is to use all of CPUs available (optional)  

```Bash
aknnPredict.py
```
Function: Prediction on the test set by the trained model 

usage: aknnPredict.py [-h] [--data D] [--model M] [--result R]

optional arguments:  
-h, --help 　 show this help message and exit  
--data D  　  data to be predicted, the last column is the labels (required)  
--model M 　  filename of the model trained. the default is lbsmodel.npz(optional)  
--result R 　 filename to keep the result of prediction. the default is Result.txt (optional)  

