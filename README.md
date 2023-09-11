

## Requirements
* Python 3.6+
* NumPy (`pip install numpy`)
* Pandas (`pip install pandas`)
* Tensorflow (`pip install tensorflow` or `pip install tensorflow-gpu`)


---
## Introduction
Glaucoma is a major cause of blindness and vision impairment worldwide, and visual field (VF) tests are essential for monitoring the conversion of glaucoma. In this project, we propose and  implement several deep-learning approaches that naturally incorporate temporal and spatial information infrom longitudinal visual field data to predict time-to-glaucoma. 

## Notebooks

### LSTM
*To apply this method, we need the longitudinal observed visual field dataset (https://github.com/rivenzhou/VF_prediction/blob/main/data/temporal/X5_all_arti.csv) and dataset containing censoring indicator (https://github.com/rivenzhou/VF_prediction/blob/main/data/temporal/Y5_e_arti.csv).

*For method application and time-to-glaucoma prediction, [Here is the Notebook] (https://github.com/rivenzhou/VF_prediction/blob/main/lstm.ipynb).

### Bi-LSTM
*To apply this method, we need the  longitudinal observed visual field dataset (https://github.com/rivenzhou/VF_prediction/blob/main/data/temporal/X5_all_arti.csv) and dataset containing censoring indicator (https://github.com/rivenzhou/VF_prediction/blob/main/data/temporal/Y5_e_arti.csv).

*For method application and time-to-glaucoma prediction, [ Here is the Notebook] (https://github.com/rivenzhou/VF_prediction/blob/main/bilstm.ipynb).

### CNN-LSTM
*First, apply zero-padding (https://github.com/rivenzhou/VF_prediction/blob/main/zero-padding.ipynb) on dataset (https://github.com/rivenzhou/VF_prediction/blob/main/data/temporal/X5_72_arti.csv), which contains  longitudinal observed visual field at 54 points. After applying zero-padding, we get visual field data with 72 points (https://github.com/rivenzhou/VF_prediction/blob/main/data/temporal/data_72_arti.csv), which can be transformed to $8 \times 9$ image and used for CNN-LSTM.

*For method application and time-to-glaucoma prediction, [Here is the Notebook] (https://github.com/rivenzhou/VF_prediction/blob/main/cnn-lstm.ipynb).

### ResNet50-LSTM

*First, apply zero-padding (https://github.com/rivenzhou/VF_prediction/blob/main/zero-padding.ipynb) on dataset (https://github.com/rivenzhou/VF_prediction/blob/main/data/temporal/X5_72_arti.csv), which contains  longitudinal observed visual field at 54 points. After applying zero-padding, we get visual field data with 72 points (https://github.com/rivenzhou/VF_prediction/blob/main/data/temporal/data_72_arti.csv), which can be transformed to $8 \times 9$ image and used for ResNet50.

* Apply ResNet50 (https://github.com/rivenzhou/VF_prediction/blob/main/resnet.ipynb) on transformed zero-padding images (https://github.com/rivenzhou/VF_prediction/blob/main/data/temporal/data_72_arti.csv).

*For method application and time-to-glaucoma prediction, [Here is the Notebook] (https://github.com/rivenzhou/VF_prediction/blob/main/lstm-resnet.ipynb).