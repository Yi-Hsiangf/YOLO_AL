# Active-Learning for YOLOv5
## Additional Usage
Preprocessing the data from voc (xml) to yolo (txt) version.
Please move the reader file to the directory that contain the dataset.
For example, you put the Autumn dataset at the directory /home/data/data/2020_Autumn, you should put the reader.py at /home/data/data.
```sh
# By default, the reader preprocess the dataset 2020_Autumn and split the train val in 0.7 ratio, if can change the dataset by giving the parameter --dataset and --split
$ python reader.py --dataset 2020_Autumn --split 0.7
```

Train with LLAL algorithm
```sh
# Train YOLOv5s on Autumn for 3 epochs.
$ python train.py --img 640 --batch 16 --epochs 3 --data autumn.yaml --weights yolov5s.pt --AL True
```

Train with Random selection
```sh
# Train YOLOv5s on Autumn for 3 epochs.
$ python train.py --img 640 --batch 16 --epochs 3 --data autumn.yaml --weights yolov5s.pt --AL False
```
