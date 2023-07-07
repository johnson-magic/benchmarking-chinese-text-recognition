# Getting Started

1. clone the repo
   ```
   git clone --recursive https://github.com/johnson-magic/benchmarking-chinese-text-recognition
   ```
2. install packages
   
   2.1 install dependencies expect warp-ctc
   ```
   pip install -r requirements.txt
   ```
   
   2.2 install warp-ctc
   
   we recommend you to use pytorch-ctc, because we find pytroch-ctc has faster training speed and and considerable performance compared to warp-ctc. If you still want to use warp-ctc, you can jump to this
   github [repositorie](https://github.com/johnson-magic/warp-ctc-pytorch1.x), which relies on pytorch1.12.

4. run
   ```
   bash train.sh 0 "20230707" {train_data_path} {test_data_path} 100 

   0 stands for gpu id, only support single gpu now;
   "20230707" stands for exp_name;
   ```



## Dependencies
Use the configuration file "model_name.yaml" to create the environment of the corresponding baseline. When creating the environment for CRNN, the [warp_ctc_pytorch](https://github.com/SeanNaren/warp-ctc/tree/pytorch_bindings/pytorch_binding) should be installed additionally.
```python
conda env create -f model_name/model_name.yaml
```

## Pre-trained Model
Download the trained weights of each baseline at [GoogleDrive](https://drive.google.com/drive/folders/14v3hHhq4AOVEYY1hQfA1d1vI2HtZQZey?usp=sharing)

## Training
Use the following command for training. Please remember to modify the parameters (*e.g.*, the path to training datasets, the experimental name, etc.).
```python
sh model_name/train.sh
```

## Testing
Use the following command for testing.
```python
sh model_name/test.sh
```
