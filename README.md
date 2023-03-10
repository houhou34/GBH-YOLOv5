## GBH-YOLOv5 implementation in Pytorch.
---
## Contents
1. [Project description](#Project)
2. [Required environment](#Required)
3. [Training](#Training)
4. [Testing](#Testing)
5. [Acknowledgements](#Acknowledgements)

## Project description
This project is based on the improved and optimized model of YOLOv5s, and its task is to detect defects on the surface of photovoltaic panels. In this study, the YOLOv5 model was improved to achieve 97.8% performance on PV Multi-Defect dataset.

## Required environment

Pytorch == 1.8.1  
python == 3.8  
Cuda == 11.1
  
### Install the project environment
```python
pip install -r requirements.txt
```

### Check whether the dependent environment is normal.
```python
python detect.py --source ./data/images/ --weights weights/yolov5s.pt
```

## Training

### Data preparation
Download PV Multi-Defect images (train, val) and labels. Link: https://github.com/houhou34/PV-Multi-Defect-Datasets.  
Download weights. Link: https://pan.baidu.com/s/1ApCScpr1CZ_AeVJH7crgCw Extraction code: lmn8   

### Start training
```python
python train.py
```

## Testing
The optimal weight obtained from the training was used for the test.
```python
python detect.py --source ./testfiles/img1.jpg --weights runs/train/exp/weights/best.pt
```


## Acknowledgements
https://github.com/ultralytics/yolov5  
https://github.com/robintzeng/Pytorch-CSPNet


