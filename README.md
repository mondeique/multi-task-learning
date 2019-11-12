# multi-task-learning
MONDEIQUE multi task learning (MTL) category classification using Tensorflow

## How to install 
```
pip install -r requirements.txt
```
## How to run 
### Download Image & CSV data from data-explorer
- data-explorer 로 부터 training image 와 해당 category info를 추출한다.
### data-augmentation with few datas
- data_augmentation.ipynb jupyter file 을 이용해 augment 과정을 거친다. 
### run tensorflow MTL code
- MTL code 를 customized 하여 실행시킨다. 

## Data
1. Images
> CroppedImage 
2. CSV
> 각 CroppedImage의 filename 과 해당 category source_id
## Data Structure
```
|
|-- data
      |-- images
            |-- training (training/evaluation)
            |-- test (test images)
      |-- csv
            |-- training
            |-- test
|-- pre-processing_csv.ipynb
|-- tf_MTL.ipynb (main training file)
|-- data_augmentation.ipynb 
```
