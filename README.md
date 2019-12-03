# multi-task-learning
MONDEIQUE multi task learning (MTL) category classification using Tensorflow

## How to install 
```
pip install -r requirements.txt
```
## How to run
- 아래와 같은 순서로 진행한다.
1. Download Image & CSV data from data-explorer
> data-explorer 로 부터 training image 와 해당 category info를 추출한다. 
2. data-augmentation with few datas
> data_augmentation.ipynb jupyter file 을 이용해 augment 과정을 거친다. 
3. make labeling.csv
> augment DataFrame과 기존 CroppedImage DataFrame을 이용해서 새로운 labeling.csv를 생성한다.
4. run tensorflow MTL code
> Basic MTL code 를 customized 하여 실행시킨다. 

## Data
1. Images
> CroppedImage + Augmented CroppedImage (Rotate / Noise / Flip 중 random 하게 n번)
2. CSV
> 각 CroppedImage의 filename 과 해당 category source_id
## Data Structure
```
|
|-- data
      |-- images
            |-- cropped-bag-images-dev
            |-- aug_data (Data 수가 부족할 때 해당 directory 이용)
                 |-- trapezoid
                 |-- half_circle
      |-- csv
            |-- shape_labeling
            |-- aug_shape_labeling 
            |-- training
            |-- test
|-- pre-processing_csv.ipynb
|-- tf_MTL.ipynb (multi task learning)
|-- tf_STL.ipynb (single task learning)
|-- data_augmentation.ipynb 
```

## TODO

- [ ] model restore for testing
- [ ] serving_inference_fn() coding
