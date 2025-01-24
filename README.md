# End-to-end object detection by using query-selection encoder with hierarchical feature-aware attention

[[📖 Paper]()] 

## News
* ***[1/24/2025]*** At present, our paper is under review. We are in the process of finalizing the code and documentation to ensure that it is fully functional and user-friendly. All of the code will be publicly available through this github repository soon.

   

## Introduction

![framework](figures/framework.png)
In this paper, we introduce a novel query-selection encoder (QSE) designed for end-to-end object detectors to improve training convergence speed and detection accuracy. QSE is composed of multiple encoder layers stacked on top of the backbone. A lightweight head network is added after each encoder layer to continuously optimize features in a cascading manner, providing
more positive supervision for efficient training. Additionally, a hierarchical feature-aware attention (HFA) mechanism
is devised in each encoder layer, including in-level feature attention and cross-level feature attention, to enhance the
interaction between features from different levels. HFA can effectively suppress similar feature representations and
highlight the discriminative ones thereby accelerating the feature selection process. Our method is highly versatile
in accommodating both CNN-based and transformer-based detectors.

![performance](figures/performance.png) 

## Model Zoo

## Running

### Install
We implement QSE using [MMDetection V2.25.3](https://github.com/open-mmlab/mmdetection/releases/tag/v2.25.3) and [MMCV V1.5.0](https://github.com/open-mmlab/mmcv/releases/tag/v1.5.0).
The source code of MMdetection has been included in this repo and you only need to build MMCV following [official instructions](https://github.com/open-mmlab/mmcv/tree/v1.5.0#installation).
We test our models under ```python=3.7.11,pytorch=1.11.0,cuda=11.3```. Other versions may not be compatible. 

### Data
The COCO dataset and LVIS dataset should be organized as:
```
QSE
└── data
    └── coco
       ├── annotations
       │      ├── instances_train2017.json
       │      └── instances_val2017.json
       ├── train2017
       └── val2017
      
```

### Training

### Testing


## Cite our work


## License

This project is released under the MIT license. Please see the [LICENSE](LICENSE) file for more information.
