**DETR**: Object Detection with Transformers - Finetuning Model with COCO Dataset.
========
Using PyTorch and DETR opensource github codebase we are developing a system to train already Trained DETR Model. 

Installation and Set-up guide-
========

# Clone detr repo
!git clone https://github.com/facebookresearch/detr.git 

# Install all required libraries (In google collab it is not needed except ! pip install albumentations==0.4.6)
pip install -r requirements.txt

## Data preparation
- Download and extract coco dataset
    
    We expect the directory structure to be the following:
    ```
    path/to/dataset/
      train/_annotations.json    # train images
      test/_annotations.json      # test images
    ```

- Run a dataformat.ipynb or dataformat.py file to convert _annotations.json file to .csv file with required field.
calling method- 

    convert_coco_json_to_csv1("bccd/valid/_annotations.coco.json") [change the path accordingly]
    
    Note- Post running this file please make sure to remove .json & .csv file from image folder.
    
    required directory structure should be- dataset/train/train [storage of all .jpeg image]
                                            dataset/train/train.csv [storage of all image metadata]

Note- Please replace hat data train and test folder and replace existing one as it is kept.

## Below file being used for hyper tuning model while training.
# Below code load configuration from "config.ini" file  
                                           
# code-line : config.read("/content/drive/My Drive/detr_finetune/conf/config.ini")

## Training and Evaluation-
Run All the block of code to run and evaluate the model.
