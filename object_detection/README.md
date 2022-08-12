
tutorial.ipynb is the official from https://github.com/ultralytics/yolov5

build_label_txt.ipynb is for building label from open-image v6 datasets

split_train_val.ipynb is to split the datasets to training, validation and test sets

using 'python --weights yolov5.pt --data  data.yaml' to train

one of the example for running training on server

nohup python -m torch.distributed.run --nproc_per_node 2 train.py --batch 8 --data data/open-image.yaml --weights yolov5m.pt --project ./yolov5_train --name yolov5m_train_sgd2 --batch-size 16 --epochs 350 --optimizer SGD > yolo_train.log 2>&1 & echo $! > yolo_train.pid


other file is form https://github.com/ultralytics/yolov5
