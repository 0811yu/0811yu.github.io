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

@font-face{
font-family:"Times New Roman";
}

@font-face{
font-family:"宋体";
}

@font-face{
font-family:"Calibri";
}

@font-face{
font-family:"Wingdings";
}

p.MsoNormal{
mso-style-name:正文;
mso-style-parent:"";
margin:0pt;
margin-bottom:.0001pt;
mso-pagination:none;
text-align:justify;
text-justify:inter-ideograph;
font-family:'Times New Roman';
mso-fareast-font-family:宋体;
font-size:10.5000pt;
mso-font-kerning:1.0000pt;
}

span.10{
font-family:'Times New Roman';
}

span.msoIns{
mso-style-type:export-only;
mso-style-name:"";
text-decoration:underline;
text-underline:single;
color:blue;
}

span.msoDel{
mso-style-type:export-only;
mso-style-name:"";
text-decoration:line-through;
color:red;
}

table.MsoNormalTable{
mso-style-name:普通表格;
mso-style-parent:"";
mso-style-noshow:yes;
mso-tstyle-rowband-size:0;
mso-tstyle-colband-size:0;
mso-padding-alt:0.0000pt 5.4000pt 0.0000pt 5.4000pt;
mso-para-margin:0pt;
mso-para-margin-bottom:.0001pt;
mso-pagination:widow-orphan;
font-family:'Times New Roman';
font-size:10.0000pt;
mso-ansi-language:#0400;
mso-fareast-language:#0400;
mso-bidi-language:#0400;
}
@page{mso-page-border-surround-header:no;
	mso-page-border-surround-footer:no;}@page Section0{
margin-top:72.0000pt;
margin-bottom:72.0000pt;
margin-left:90.0000pt;
margin-right:90.0000pt;
size:595.3000pt 841.9000pt;
layout-grid:15.6000pt;
mso-header-margin:42.5500pt;
mso-footer-margin:49.6000pt;
}
div.Section0{page:Section0;}</style></head><body style="tab-interval:21pt;text-justify-trim:punctuation;" ><!--StartFragment--><div class="Section0"  style="layout-grid:15.6000pt;" ><table class=MsoNormalTable  border=1  cellspacing=0  style="border-collapse:collapse;width:100.0000%;border:none;
mso-border-left-alt:0.5000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;mso-border-right-alt:0.5000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;mso-border-insideh:0.5000pt solid windowtext;mso-border-insidev:0.5000pt solid windowtext;
mso-padding-alt:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;" ><tr><td width=11.0200%  valign=top  style="width:11.0200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:2.2500pt solid windowtext;mso-border-top-alt:2.2500pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  style="line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >Datasets</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=2.7200%  valign=top  style="width:2.7200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:2.2500pt solid windowtext;mso-border-top-alt:2.2500pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=27.0600%  valign=top  colspan=3  style="width:27.0600%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:2.2500pt solid windowtext;mso-border-top-alt:2.2500pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >AIZOO</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=2.7200%  valign=top  style="width:2.7200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:2.2500pt solid windowtext;mso-border-top-alt:2.2500pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=9.8600%  valign=top  style="width:9.8600%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:2.2500pt solid windowtext;mso-border-top-alt:2.2500pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=17.1800%  valign=top  colspan=2  style="width:17.1800%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:2.2500pt solid windowtext;mso-border-top-alt:2.2500pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >Internet</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=3.9800%  valign=top  colspan=2  style="width:3.9800%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:2.2500pt solid windowtext;mso-border-top-alt:2.2500pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=6.6000%  valign=top  style="width:6.6000%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:2.2500pt solid windowtext;mso-border-top-alt:2.2500pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=18.8600%  valign=top  colspan=2  style="width:18.8600%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:2.2500pt solid windowtext;mso-border-top-alt:2.2500pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >Ours</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td></tr><tr><td width=11.0200%  valign=top  style="width:11.0200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=2.7200%  valign=top  style="width:2.7200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=8.7400%  valign=top  style="width:8.7400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >I</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >mages</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=8.1000%  valign=top  style="width:8.1000%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >Train</font></span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.2200%  valign=top  style="width:10.2200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >Validat</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >e</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=2.7200%  valign=top  style="width:2.7200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=9.8600%  valign=top  style="width:9.8600%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >Images</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=6.9400%  valign=top  style="width:6.9400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >Train</font></span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.2400%  valign=top  style="width:10.2400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  style="line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >Validate</font></span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=2.7200%  valign=top  style="width:2.7200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=7.8600%  valign=top  colspan=2  style="width:7.8600%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >Images</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=8.0200%  valign=top  style="width:8.0200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  style="line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >Train</font></span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.8400%  valign=top  style="width:10.8400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:1.0000pt solid windowtext;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:1.0000pt solid windowtext;
mso-border-bottom-alt:0.5000pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >Validat</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >e</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td></tr><tr><td width=11.0200%  valign=top  style="width:11.0200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >Face</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=2.7200%  valign=top  style="width:2.7200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=8.7400%  valign=top  style="width:8.7400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >6057</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=8.1000%  valign=top  style="width:8.1000%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >10598</font></span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.2200%  valign=top  style="width:10.2200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >1011</font></span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=2.7200%  valign=top  style="width:2.7200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=9.8600%  valign=top  style="width:9.8600%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >1200</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=6.9400%  valign=top  style="width:6.9400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >1956</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.2400%  valign=top  style="width:10.2400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >339</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=3.9800%  valign=top  colspan=2  style="width:3.9800%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=6.6000%  valign=top  style="width:6.6000%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >2048</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=8.0200%  valign=top  style="width:8.0200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >5240</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.8400%  valign=top  style="width:10.8400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:0.5000pt solid windowtext;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >568</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td></tr><tr><td width=11.0200%  valign=top  style="width:11.0200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >M</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >ask</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=2.7200%  valign=top  style="width:2.7200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=8.7400%  valign=top  style="width:8.7400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >1815</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=8.1000%  valign=top  style="width:8.1000%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >2890</font></span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.2200%  valign=top  style="width:10.2200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >2015</font></span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=2.7200%  valign=top  style="width:2.7200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=9.8600%  valign=top  style="width:9.8600%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >400</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=6.9400%  valign=top  style="width:6.9400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >2308</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.2400%  valign=top  style="width:10.2400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >1023</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=3.9800%  valign=top  colspan=2  style="width:3.9800%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=6.6000%  valign=top  style="width:6.6000%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >7136</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=8.0200%  valign=top  style="width:8.0200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >11783</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.8400%  valign=top  style="width:10.8400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:none;
mso-border-bottom-alt:none;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >2859</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td></tr><tr><td width=11.0200%  valign=top  style="width:11.0200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >T</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >otal</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=2.7200%  valign=top  style="width:2.7200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=8.7400%  valign=top  style="width:8.7400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >7872</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=8.1000%  valign=top  style="width:8.1000%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >13488</font></span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.2200%  valign=top  style="width:10.2200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >3026</font></span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=2.7200%  valign=top  style="width:2.7200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=9.8600%  valign=top  style="width:9.8600%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >1600</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=6.9400%  valign=top  style="width:6.9400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >4264</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.2400%  valign=top  style="width:10.2400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >1362</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=3.9800%  valign=top  colspan=2  style="width:3.9800%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></td><td width=6.6000%  valign=top  style="width:6.6000%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >9</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" >184</span><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=8.0200%  valign=top  style="width:8.0200%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >17023</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td><td width=10.8400%  valign=top  style="width:10.8400%;padding:0.0000pt 5.4000pt 0.0000pt 5.4000pt ;border-left:none;
mso-border-left-alt:none;border-right:none;mso-border-right-alt:none;
border-top:none;mso-border-top-alt:none;border-bottom:2.2500pt solid windowtext;
mso-border-bottom-alt:2.2500pt solid windowtext;" ><p class=MsoNormal  align=center  style="text-align:center;line-height:200%;" ><span style="font-family:宋体;mso-ascii-font-family:'Times New Roman';mso-hansi-font-family:'Times New Roman';
mso-bidi-font-family:'Times New Roman';line-height:200%;font-size:9.0000pt;
mso-font-kerning:1.0000pt;" ><font face="Times New Roman" >3427</font></span><span style="font-family:'Times New Roman';mso-fareast-font-family:宋体;line-height:200%;
font-size:9.0000pt;mso-font-kerning:1.0000pt;" ><o:p></o:p></span></p></td></tr></table><p class=MsoNormal ><span style="mso-spacerun:'yes';font-family:'Times New Roman';mso-fareast-font-family:宋体;
font-size:10.5000pt;mso-font-kerning:1.0000pt;" ><o:p>&nbsp;</o:p></span></p></div><!--EndFragment--></body></html>

## Three devices
We tested our proposed model on three devices: local machine, Google Colab cloud computing platform, and Jeston Nano edge computer



## Our proposed evaluation standard
In order to measure the maximum detection ability of the model, We established a new evaluation standard, namely setting a limit scale. The calculation formula and experimental results are as follows

<div align="center">

</div>




## Result of experiment



## Embed the edge computer into the UGV
We embed the edge computer into the UGV for testing. The introduction of getting off the car is as follows. You can also watch the equipment used and the testing process through the video through the link below.
### UGV
<div>
<p><img class="wide" src="./COCO - Common Objects in Context_files/UGV.png"></p>
</div>
You can see our test of the model through the link below
<a href="https://www.bilibili.com/video/BV1B44y1D7Tu/?vd_source=3e566f0cb06b6542b1efd377a512e51c">Click here</a>

 


 
