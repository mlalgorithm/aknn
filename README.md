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

### To predict on test data :

```Bash
python aknnPredict.py --data 'data/leukemia_test.csv'
```

## Usage

aknnTrain.py

Function: Training by Adaptive k-nearest neighbor

usage: aknnTrain.py [-h] [--data D] [--ne N] [--out O] [--cpu C]


　　　　optional arguments:
　　　　-h, --help  show this help message and exit
　　　　--data D    data to be trained, the last column is regarded as label
         　　　　   (required)
 　--ne N      maximum number of feature subsets to be evaluated in each
                iteration. the default is 2000000 (optional)
  　--out O     filename to keep the output of training. the default is
               lbsmodel.npz (optional)
  　--cpu C     the number of CPUs to use. the default is to use all of CPUs
                available (optional)


lbsPredict.py

Function: Prediction on the test set by the trained model 

usage: aknnPredict.py [-h] [--data D] [--model M] [--result R]
optional arguments:
　　-h, --help  show this help message and exit
　　--data D    data to be screened (required)
　　--model M   filename of the LBS model trained. the default is lbsmodel.npz
              (optional)
　　--result R  filename to keep the result of screening, index of screened
              samples are kept. the default is ScreenResult.txt (optional)

