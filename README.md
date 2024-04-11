# AGDN
Attention Guidance Distillation Network for Efficient Image Super-Resolution
Hongyuan Wang, Ziyan Wei, Qingting Tang, Shuli Cheng, Liejun Wang, and Yongming Li

## Environment

[PyTorch == 2.1.2](https://pytorch.org/)
[BasicSR >= 1.3.4.9](https://github.com/XPixelGroup/BasicSR)

### Installation
```
pip install -r requirements.txt
python setup.py develop
```

## How To Test
· Refer to ./options/test for the configuration file of the model to be tested, and prepare the testing data and pretrained model.
· The pretrained models are available in ./pretrain/
· Then run the follwing codes (taking AGDN_x4.pth as an example):

```
python basicsr/test.py -opt options/test/benchmark_AGDN_x4.yml
```
The testing results will be saved in the ./results folder.

## How To Train
· Refer to ./options/train for the configuration file of the model to train.
· Preparation of training data can refer to this page. All datasets can be downloaded at the official website.
· Note that the default training dataset is based on lmdb, refer to [docs in BasicSR](https://github.com/XPixelGroup/BasicSR/blob/master/docs/DatasetPreparation.md) to learn how to generate the training datasets.
· The training command is like
```
CUDA_VISIBLE_DEVICES=0 python basicsr/train.py -opt options/train/train_AGDN_x4.yml
```
For more training commands and details, please check the docs in [BasicSR](https://github.com/XPixelGroup/BasicSR)  

## Results
The inference results on benchmark datasets are available at [Google Drive](https://drive.google.com/file/d/1TCFJgGIw5aR3OOhMtfvvU-WOe5w4wVPX/view?usp=drive_link).

## Contact
If you have any question, please email why5200@stu.xju.edu.cn.
