# Object Detection

## YOLO (refer to [here](https://github.com/marvis/pytorch-yolo3/blob/master/train.py))

#### 4. Train YOLO
- Specify `train_file` and `test_file` in `yolo/cfg/voc.data` or rename them as `my_train.txt` and `my_test.txt`.
```
python yolo/train.py yolo/cfg/voc.data yolo/cfg/yolo-voc.cfg yolo/darknet19_448.conv.23
```
- Train YOLO with the configurations in `yolo/cfg/yolo-voc.cfg` and the pre-trained weights in `yolo/darknet19_448.conv.23`. 
- Trained weights are stored in `backup/`.


#### 5. Inference
```
python yolo/valid.py yolo/cfg/voc.data yolo/cfg/yolo-voc.cfg backup/000100.weights
```
- Inference on the testing data with the trained weights.
