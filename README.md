# Part2Word: Learning Joint Embedding of Point Clouds and Text by Bidirectional Matching between Parts and Words

## Introduction
This is the source code of Part2Word: Learning Joint Embedding of Point Clouds and Text by Bidirectional Matching between Parts and Words, an approch for Shape-Text Matching based on local based matching method. 
![](./doc/teaser.png)

## Requirements

```
pip install -r requirements.txt
```

## Download data
We pack the shapenet data with segmentation annotation in h5 file, you can download the h5 file from [here](https://drive.google.com/file/d/11uSuGUxV7WSM3Cogh4tZmt37ZPYCffVE/view?usp=sharing)


```
data
|-- models
|   `-- shapenet
|       
`-- shapenet
    |-- shapenetv2_level_1.pkl
    |-- split_shape_captioner
    |   |-- test_03001627.txt
    |   |-- test_04379243.txt
    |   |-- train_03001627.txt
    |   `-- train_04379243.txt
    `-- vocab
        `-- shapenet.json
```
## Set configure file

set data path in `conig/part2word_default.yaml`.


## Train model
```
python train.py --config conig/part2word_default.yaml
```

## evaluate model
```
python val.py --config conig/part2word_default.yaml
```


## Acknowledgments
Our code is built on top of the [SCAN](https://github.com/kuanghuei/SCAN) in PyTorch.

## Reference
If you found this code useful, please cite the following paper:
```
@article{tang2021part2word,
  title={Part2Word: Learning Joint Embedding of Point Clouds and Text by Matching Parts to Words},
  author={Tang, Chuan and Yang, Xi and Wu, Bojian and Han, Zhizhong and Chang, Yi},
  journal={arXiv preprint arXiv:2107.01872},
  year={2021}
}
```