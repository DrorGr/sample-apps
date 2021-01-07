
# Object Detection Demos

`COCO mAP TFYolov3: 36.0`
`COCO mAP TFMobileNet: 28.6`


## Get Started
To Download tf-yolov3 or mobilenet model:

```
sh download_mobilenet.sh
sh download_tfyolov3.sh
```

## install Trueface sdk
`sudo pip install https://github.com/getchui/offline_sdk/releases/download/0.61/trueface-0.0.6.1-cp27-cp27mu-linux_x86_64.whl`

Get your platform wheel url from the following page:<br/>
https://github.com/getchui/offline_sdk/releases

### Run Demo
```
export TF_TOKEN={your_token}
python demo.py
```


#### CPU vs GPU
Change the context in the class initializer:

CPU
```
object_recognition = ObjectRecognizer(ctx='cpu',
                      model_path="./tf-object_detection-mobilenet/model.trueface",
                      params_path="./tf-object_detection-mobilenet/model.params",
                      license=os.environ['TF_TOKEN'],
                      classes="./tf-object_detection-mobilenet/classes.names")
```

GPU
```
object_recognition = ObjectRecognizer(ctx='gpu',
                      model_path="./tf-object_detection-mobilenet/model.trueface",
                      params_path="./tf-object_detection-mobilenet/model.params",
                      license=os.environ['TF_TOKEN'],
                      classes="./tf-object_detection-mobilenet/classes.names")
```

You can define the index of gpu to by adding a `gpu` param to the initializer.


# Demo with MJPEG Streaming
```
export TF_TOKEN={your_token}
python demo_with_mjpeg_streaming.py
```
Navigate to http://localhost:8086.
<br />
<br />
You can use the streaming url in a simple img tag, ex:

`<img src="http://localhost:8086" />`



