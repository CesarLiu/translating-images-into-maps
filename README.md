# Translating Images into Maps
#### Avishkar Saha, Oscar Mendez Maldonado, Chris Russell and Richard Bowden

This is the official code for the paper [Translating Images Into Maps](https://arxiv.org/abs/2110.00966) presented at ICRA 2022.

### Translating Images into Maps
<div>
<img src="images/image_to_bev_motivation.gif"></img>
</div>
<br />

### Setup
The code was written using python 3.7. 
The following libraries are the minimal required for this repo: 
```python
pip install --no-cache-dir torch==1.10.1+cu111 torchvision==0.11.2+cu111 torchaudio==0.10.1 -f https://download.pytorch.org/whl/cu111/torch_stable.html

opencv-python
numpy
pickle
pyquaternion
shapely
lmdb
tensorboard
nuscenes-devkit
```

### Data
The official nuScenes data will be required to train the entire model. 
But for convenience, we provide the nuScenes mini dataset wrapped into 
lmdb's:
```
https://drive.google.com/drive/folders/1-1dZXeHnPiuqX-w8ruJHqfxBuMYMONRT?usp=sharing
```

The contents of this folder need to be unzipped and placed in a folder, create the folder
as follows:
```
$ pip install gdown
$ cd translating-images-into-maps
$ gdown --folder https://drive.google.com/drive/folders/1-1dZXeHnPiuqX-w8ruJHqfxBuMYMONRT?usp=sharing
```

This contains the ground truth maps which have already been generated for
the mini dataset, the input images and intrinsics.

### Using the code:
To train a model with the configuration in the paper, simply run:
```bash
python train.py  
```

### Pretrained model
Pretrained models and their configs required to load/train them can be downloaded from here:
````
https://drive.google.com/drive/folders/13-WobzEg9MGcT-tceXE3kwgEv8Q-kUwU?usp=sharing (old)
https://drive.google.com/drive/folders/11zXPS8_o8Ql7QwnqmUGskwoRsBpBRxNp?usp=sharing (new)
````


### Citation
If you find this code useful, please cite the following papers:
```
@inproceedings{saha2022translating,
  title={Translating Images into Maps},
  author={Saha, Avishkar and Mendez, Oscar and Russell, Chris and Bowden, Richard},
  booktitle={2022 IEEE International Conference on Robotics and Automation (ICRA)},
  year={2022},
  organization={IEEE}
}
@inproceedings{saha2021enabling,
  title={Enabling spatio-temporal aggregation in birds-eye-view vehicle estimation},
  author={Saha, Avishkar and Mendez, Oscar and Russell, Chris and Bowden, Richard},
  booktitle={2021 IEEE International Conference on Robotics and Automation (ICRA)},
  pages={5133--5139},
  year={2021},
  organization={IEEE}
}
```
