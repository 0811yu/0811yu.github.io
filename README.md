<div align="center">
 
  ![image](https://user-images.githubusercontent.com/101705236/181425227-d0594cb6-81be-489f-84d0-04b190bb742e.png)

</div>

# Improved YOLO-v5 model for boosting face mask recognition accuracy under heterogeneous computing modalities

<div align="center">

<b><font size="5">Google Colab</font></b>
    <sup>
      <a href="https://colab.research.google.com/">
        <i><font size="4">HOT</font></i>
      </a>
    </sup>
    &nbsp;&nbsp;&nbsp;&nbsp;
    <b><font size="5">Jeston Nano</font></b>
    <sup>
      <a href="https://www.nvidia.cn/autonomous-machines/embedded-systems/jetson-nano/">
        <i><font size="4">TRY IT OUT</font></i>
      </a>
    </sup>
    <b><font size="5">NVIDIA GeForce RTX 3050</font></b>
    <sup>
      <a href="https://www.nvidia.cn/geforce/graphics-cards/30-series/rtx-3050/">
        <i><font size="4">GET IT</font></i>
      </a>
    </sup>

  ![](https://img.shields.io/badge/python-3.8-blue)
  [![](https://img.shields.io/badge/pytorch-1.9.0-blue)](https://pytorch.org/)
  [![](https://img.shields.io/badge/torchvision-0.10.0-orange)](https://pypi.org/project/torchvision/)
  ![](https://img.shields.io/conda/pn/conda-forge/python?label=windows)
  

  [🛠️Installation Dependencies](#Dependencies) |
  [🎤Introduction](#Introduction) |
 
  [👀Download Dataset](https://0811yu.github.io) |
  
  [🌊a new evaluation standard](https://github.com/0811yu/0811yu.github.io) |
  [🚀heterogeneous computing modalities](https://github.com/0811yu/0811yu.github.io) |
  
  [🤔The limit detection distance of the model](https://github.com/0811yu/0811yu.github.io) |
 

</div>

## Dependencies:

 - Python 3.8
 - [PyTorch](https://pytorch.org/) 1.9.0
 - [Torchvision](https://pypi.org/project/torchvision/) 0.10.0
 - [OpenVINO](https://docs.openvino.ai/)
 - Windows 10  Ubuntu 18.04 
 - [Google Colab](https://colab.research.google.com/)
 - NVIDIA GeForce RTX 3050  Jeston Nano

## Introduction

We improved the YOLO-v5s V6.0 version, added the CA mechanism to its backbone network, used BiFPN as the feature pyramid network, and embedded ASFF into the head, and finally replaced the initial CIoU with the new bounding box loss function SIou. 
We trained the model on the AIZOO dataset, and verified it on the dataset downloaded from the Internet and the dataset we made. The final results show that our improved model is effective on multiple face datasets. Finally, we test the trained model on local machine, Google Colab and Jeston Nano.
In order to test the performance of the model more comprehensively, we propose a new evaluation standard Scale, the limit distance of the test model.

## Ours face mask dataset-HBNU-MD
We have established a website for our dataset, which gives a detailed introduction to the dataset, you can click the link below to download the dataset.
<a href="https://0811yu.github.io/#home">Click here to view and download the dataset</a>
### HBNU-MD example
<p><img class="wide" src="./COCO - Common Objects in Context_files/Dataset_example.png"></p>
</div>

## Three devices
We tested our proposed model on three devices: local machine, Google Colab cloud computing platform, and Jeston Nano edge computer



## Our proposed evaluation standard
In order to measure the maximum detection ability of the model, We established a new evaluation standard, namely setting a limit scale. The calculation formula and experimental results are as follows

<div align="center">

</div>

A combination method of cluster analysis and regression analysis from a quantitative perspective was designed to specifically analyze how the inference time varies with batch size in the above Table shown in Figure below.


## Result of experiment
It showed the top-1 accuracy versus the number of images processed per second (with batch size 1) on the Google Colab computing platform. For a scatter plot of the relationship between top-1 accuracy and FPS in Intel NCS2, please see the paper.


## Embed the edge computer into the UGV
We embed the edge computer into the UGV for testing. The introduction of getting off the car is as follows. You can also watch the equipment used and the testing process through the video through the link below.
### UGV
<div>
<p><img class="wide" src="./COCO - Common Objects in Context_files/UGV.png"></p>
</div>
You can see our test of the model through the link below
<a href="https://www.bilibili.com/video/BV1B44y1D7Tu/spm_id_from=333.1007.top_right_bar_window_history.content.click&vd_source=3e566f0cb06b6542b1efd377a512e51c">Click here</a>

 


 
