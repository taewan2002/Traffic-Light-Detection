# Traffic Light Detection with YOLOv5

This repository contains the implementation of a traffic light detection model fine-tuned using YOLOv5 on a custom dataset. The dataset is provided by [Roboflow](https://universe.roboflow.com/trafficlight-7r04p/traffic-light-prnso/dataset/8).

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Setup](#setup)
- [Training](#training)
- [Results](#results)

## Introduction

Traffic light detection is a critical component in autonomous driving systems. This project aims to fine-tune a pre-trained YOLOv5 model to accurately detect traffic lights in images.

## Dataset

![](https://github.com/taewan2002/cs224n/assets/89565530/55cb8e51-24e5-4e77-a739-c122e261e71d)

![](https://github.com/taewan2002/cs224n/assets/89565530/a79d426c-9130-4fe5-a293-e6ead5609084)

![](https://github.com/taewan2002/cs224n/assets/89565530/481cf6c8-3a75-41cb-bf0e-de3971e369d9)

![](https://github.com/taewan2002/cs224n/assets/89565530/a6f34f56-14d9-4a13-8eb6-4375b46fbc04)

The dataset used for this project is available on Roboflow and includes images and annotations for traffic lights. You can download the dataset from [here](https://universe.roboflow.com/trafficlight-7r04p/traffic-light-prnso/dataset/8).

## Setup

To get started, clone this repository and install the necessary dependencies:

[notebook](https://github.com/taewan2002/Traffic-Light-Detection/blob/main/main.ipynb)

```bash
git clone https://github.com/ultralytics/yolov5.git
```

and split train-valid dataset

## Training

Use the following command to start training:

```bash
python train.py --img 360 --batch 256 --epochs 50 --data ../data.yaml --cfg models/yolov5s.yaml --weights yolov5s.pt --name traffic_light_yolov5s_results --entity taewan2002 --project traffic_light_yolov5s
```

![](https://github.com/taewan2002/cs224n/assets/89565530/d1dbdc2e-c712-4a97-bb57-28aed6da30b9)

![](https://github.com/taewan2002/cs224n/assets/89565530/7368d591-88c7-4ca3-98fd-2e2f87e00964)

![](https://github.com/taewan2002/cs224n/assets/89565530/6bb61205-da66-47ee-851c-5848752bf96a)

## Results

[wandb link](https://wandb.ai/taewan2002/traffic_light_yolov5s/runs/res0rm6q?nw=nwusertaewan2002)

Test modal with this camera

![](https://github.com/taewan2002/cs224n/assets/89565530/ed0112cd-3204-43a2-ad00-d3a7d814985a)

Convert the model

![](https://github.com/taewan2002/cs224n/assets/89565530/fad1e4f2-a087-4905-baef-cd54316e9fb1)

Apply the model

![](https://github.com/taewan2002/cs224n/assets/89565530/9b40f86c-27e9-4a46-9ed1-8039957501dc)

Test the model with camera

| ![](https://github.com/taewan2002/cs224n/assets/89565530/e764e2aa-71d5-4525-9c4b-17b4c9869752) | ![](https://github.com/taewan2002/cs224n/assets/89565530/71bca738-edea-42a3-9803-c6277a947058) | ![](https://github.com/taewan2002/cs224n/assets/89565530/fee043d5-3857-4c9f-b6eb-02e5a6a50d7d) |
|---|---|---|

It works well!!

## More Work

How about vision-language model (VLM), PaliGemma-3b [link](https://huggingface.co/spaces/big-vision/paligemma)

![](https://github.com/taewan2002/Traffic-Light-Detection/assets/89565530/25333457-28b9-4af6-b023-d5ed318076d6)


![](https://github.com/taewan2002/Traffic-Light-Detection/assets/89565530/3665fc97-905d-4a6c-8f9d-c085a177dd9c)
