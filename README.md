# Improvement-of-resolution

> AI Final Project

## Requirement
#### 1. Create a conda environment
```
conda create -n srfbn python=3.7
conda activate srfbn
```
#### 2. Install Dependencies
```
conda insall scikit-image
pip install torch==1.5.0+cu101 torchvision==0.6.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html
conda install tqdm
conda install pandas
pip install opencv-python
pip install gdown
pip install scipy==1.2.2
```

## Dataset
1. Download BSD300 [link](https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/bsds/BSDS300/html/dataset/images.html)
2. Run `Prepare_TrainData_HR_LR.m` to decompress the file, the data folder structure should look like this:
```
data
├── train
│   ├── HR_
│   │   ├── 100075_rot0_ds0.png
│   │   ├── 100075_rot0_ds1.png
│   │   ├── ......
│   └── LR
│       ├── 100075_rot0_ds0.png
│       ├── 100075_rot0_ds1.png
│       └── ......
└── val
    ├── HR
    │   ├── 106020_rot0_ds0.png
    │   ├── 106020_rot0_ds1.png
    │   ├── ......
    └── LR
        ├── 106020_rot0_ds0.png
        ├── 106020_rot0_ds1.png
        ├── ......
```


## Train
```
python train.py -opt options/train/train_SRFBN_custom.json
```

## Reference

[Paper99/SRFBN_CVPR19](https://github.com/Paper99/SRFBN_CVPR19)

