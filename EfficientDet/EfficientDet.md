### EfficientDet

https://github.com/zylo117/Yet-Another-EfficientDet-Pytorch

##### 自定义数据集进行训练

在EfficientDet/project下面书写.yml文件

参考：

```yaml
project_name: VOC2007  # also the folder name of the dataset that under data_path folder
train_set: train
val_set: val
num_gpus: 1

# mean and std in RGB order, actually this part should remain unchanged as long as your dataset is similar to coco.
mean: [0.485, 0.456, 0.406]
std: [0.229, 0.224, 0.225]

# this is coco anchors, change it if necessary
anchors_scales: '[2 ** 0, 2 ** (1.0 / 3.0), 2 ** (2.0 / 3.0)]'
anchors_ratios: '[(1.0, 1.0), (1.4, 0.7), (0.7, 1.4)]'

# must match your dataset's category_id.
# category_id is one_indexed,
# for example, index of 'car' here is 2, while category_id of is 3
obj_list:  ['aeroplane', 'bicycle', 'bird', 'boat', 'bottle', 'bus', 'car', 'cat', 'chair', 'cow', 'diningtable', 'dog', 'horse', 'motorbike', 'person', 'pottedplant', 'sheep', 'sofa', 'train', 'tvmonitor']


```





##### 数据集格式转换相关

参考https://github.com/zldscr0/datasets

文件找不到，主要去修改一下`projects/voc2007.yml`或`efficientdet/datasets.py`



##### train

```bash
bash EfficientDet/scripts/train.sh
```



##### 数据目录

`datasets/voc2coco`







