# 下载yolov5
-- git clone https://github.com/ultralytics/yolov5.git
或者在 https://github.com/ultralytics/yolov5 上下载zip包
-- 安装requirement.txt文件

# 测试自带的权重文件
python .\detect.py --source .\data\images --weights .\weight\yolov5n-7-k5.pt

# 收集数据集
从自然环境中收集数据集，但是图片最好具有多样性，采集在不同的天气、不同的时间、不同的光照强度、不同角度、不同来源的图片。
具体要求可搜索：YOLO官方推荐数据集需求。

# 标记数据集
使用labelImg 标记数据集，生成label

# 训练数据集
!python train.py --batch-size 2 --epochs 200 --data det_sample/leaf/data.yaml --weights weight/yolov5n-7-k5.pt

# 测试
!python .\detect.py --source C:\Users\gf66\Pictures\luoye --weights runs/train/exp15/weights/best.pt

# 训练的比较好的一个weight
python .\detect.py --source C:\Users\gf66\Pictures\luoye --weights runs/train/leaf_det_model/weights/best.pt

python .\detect.py --source C:\Users\gf66\Pictures\luoye --weights runs/train/exp16/weights/best.

python train.py --batch-size 8 --epochs 200 --data Mydataset/Mydata.yaml --weights Myweights/yolov5n.pt


python train.py --data Mydataset/Mydata.yaml --epochs 300 --weights '' --cfg yolov5x.yaml  --batch-size 8
python detect.py --source Mytest --weights runs/train/exp8/weights/best.pt