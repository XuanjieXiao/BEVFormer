# Step-by-step installation instructions

Following https://mmdetection3d.readthedocs.io/en/latest/getting_started.html#installation



**a. Create a conda virtual environment and activate it.**
```shell
conda create -n open-mmlab python=3.8 -y
conda activate open-mmlab
```

**b. Install PyTorch and torchvision following the [official instructions](https://pytorch.org/).**
```shell
pip install torch==1.9.1+cu111 torchvision==0.10.1+cu111 torchaudio==0.9.1 -f https://download.pytorch.org/whl/torch_stable.html
# Recommended torch>=1.9

```

**c. Install gcc>=5 in conda env (optional).**
```shell
conda install -c omgarcia gcc-6 # gcc-6.2
```

**c. Install mmcv-full.**
```shell
pip install mmcv-full==1.4.0
#  pip install mmcv-full==1.4.0 -f https://download.openmmlab.com/mmcv/dist/cu115/torch1.11.0/index.html
```

**d. Install mmdet and mmseg.**
```shell
pip install mmdet==2.14.0
pip install mmsegmentation==0.14.1
```

**e. Install mmdet3d from source code.**
```shell
git clone https://github.com/open-mmlab/mmdetection3d.git
cd mmdetection3d
git checkout v0.17.1 # Other versions may not be compatible.
python setup.py install
```

**f. Install timm.**
```shell
pip install timm
```


**g. Clone BEVFormer.**
```
git clone https://github.com/zhiqi-li/BEVFormer.git
```

**h. Prepare pretrained models.**
```shell
cd bevformer
mkdir ckpts

cd ckpts & wget https://github.com/zhiqi-li/storage/releases/download/v1.0/r101_dcn_fcos3d_pretrain.pth
```

note: this pretrained model is the same model used in [detr3d](https://github.com/WangYueFt/detr3d)

```
pip install mmcv-full==1.4.0 -f https://download.openmmlab.com/mmcv/dist/cu113/torch1.10.0/index.html
pip install mmdet==2.14.0 -i http://pypi.douban.com/simple/ --trusted-host pypi.douban.com
pip install mmsegmentation==0.14.1 -i http://pypi.douban.com/simple/ --trusted-host pypi.douban.com
pip install python-dateutil==2.8.2
pip install pyzmq==23.0
```
