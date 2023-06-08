# SO-VITS-SVC

## 1、日常记录

运行的为https://github.com/svc-develop-team/so-vits-svc Branch4.0分支

对应需要下载G_0.pth和D_0.pth，在https://huggingface.co/langeheris/Sovits-4.0-Pretrained-Model/tree/main中下载，待确定是否正确，在logs/44k文件夹中

之前还在https://huggingface.co/Rinccc/sovits_pretrained/tree/main下载了一个版本，在logs/44k文件夹下命名为G(D)_0-old.pth

## 2、环境安装

conda create -n sovits-svc python=3.9

conda activate sovits-svc

pip install -r requirements_win.txt

参考https://blog.csdn.net/Sucial/article/details/130232821单独下载torch、torchaudio\torchvision安装包，单独下载

## 3、语音数据集

1.下载音乐

2.在https://github.com/Anjok07/ultimatevocalremovergui中下载软件，提前干声（无背景音乐的声音）

3.在https://github.com/openvpi/audio-slicer中下载软件（https://github.com/flutydeer/audio-slicer为gui版本），将干声音频切片。



## 4.训练流程

1.将采集的语音数据放入dataset_raw文件夹下，以speaker名称作为子文件夹名。另外在dataset_raw/config.json中加入该speaker信息

2.python resample.py

3.python preprocess_flist_config.py

4.python preprocess_hubert_f0.py

5.python train.py -c configs/config.json -m 44k





音乐合成其他案例

https://github.com/microsoft/muzic







