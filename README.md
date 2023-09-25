# TransColor : Medical Image Colorization Based on Transformer with Content and Structure Preservation

*Authors: [Liming Xu]([LimingXuM3 (Bryan Xu) (github.com)](https://github.com/LimingXuM3)), Dengping Zhao, Bochuan Zheng, Weisheng Li and Xianhua Zeng

In this paper, we propose a transformer-based model to achieve the task of grey-scale medical image colorization based on real human slice images. Compared to the state-of-the-art methods, we can improve the coloring effect and make the synthetic image more realistic.

## Results presentation 

> ![Results](https://github.com/UniqueZhao/TransColor/blob/main/Figure/FlowChart.jpg?raw=true)
>
> </p>Compared with the state-of-the-art methods, we can improve the coloring effect, make the synthetic image more realistic and have better feature representation ability.  <br>

## FlowChart

> ![FlowChart](https://github.com/UniqueZhao/TransColor/blob/main/Figure/Result.jpg?raw=true)
>
> Flowchart of TransColor can be viewed as the following four steps: (1) Segment reference image and original image into patches, and generate patch sequences by linear projection, (2) feed original image sequence with CAPE and reference image sequence with SAPE into style Transformer encoder, respectively, (3) stylise content sequence according to style sequence in multi-layer Transformer decoder, and (4) obtain synthetic image with real physical colors using 3-layer CNN decoder.

## Experiment

### Requirements

* python 3.8
* pytorch 1.5.1
* PIL, numpy, scipy
* tqdm  <br> 

### Testing 

Pretrained models: [vgg-model](https://drive.google.com/file/d/1BinnwM5AmIcVubr16tPTqxMjUCE8iu5M/view?usp=sharing),  [vit_embedding](https://drive.google.com/file/d/1C3xzTOWx8dUXXybxZwmjijZN8SrC3e4B/view?usp=sharing), [decoder](https://drive.google.com/file/d/1fIIVMTA_tPuaAAFtqizr6sd1XV7CX6F9/view?usp=sharing), [Transformer_module](https://drive.google.com/file/d/1dnobsaLeE889T_LncCkAA2RkqzwsfHYy/view?usp=sharing)   <br> 
Please download them and put them into the floder  ./experiments/  <br> 

```
python test.py 
```

### Training  

[Real human slice dataset](https://www.nlm.nih.gov/research/visible/photos.html) is collected from color frozen section images from the US National  Library of Medicine’s Visual Human Project (VHP)  <br>  
[grey-scale medical images](http://www.med.harvard.edu/AANLIB/) are derived from Brain datasetThe Whole Brain Atlas (harvard.edu) <br>  

```
python train.py  --batch_size 8
```

### Reference

If you find our work useful in your research, please cite our paper using the following BibTeX entry ~ Thank you ^ . ^. Paper Link [pdf](website)<br> 

```

```