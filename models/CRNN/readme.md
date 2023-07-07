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
