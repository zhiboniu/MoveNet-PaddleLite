# movenet_deploy

movenet cpp deploy based on PaddleLite;

movenet model transformed from tensorflow;



## 简介

movenet是近年的优秀开源模型代表，原模型以Tensorflow模型格式开源。

这里经转换后得到Paddle存储格式的模型。

本文件夹使用转换后的Paddle格式模型，基于PaddleLite实现c++部署。可实现移动端单张图片或图片文件夹的关键点预测功能。

部署时所需文件结构展示：

```
movenet_deploy/
|-- model_det/
|   |--movenet.nb                 movenet模型文件
|   |--infer_cfg.json             检测器模型配置文件
|-- movenet                       生成的移动端执行文件
|-- runtime_config.json           移动端执行时参数配置文件
|-- libpaddle_light_api_shared.so Paddle-Lite库文件
```



## movenet部署模型下载地址

### 完整测试工程文件夹包

下载后可直接在移动端部署测试, 除上述工程部署文件结构中提到的文件外，还包括两个文件夹[model_det_singlepose]、[model_det_multipose],分别是[model_det]文件夹的单人模型版本和多人模型版本。

[movenet_deploy.tar.gz](https://bj.bcebos.com/v1/paddledet/models/keypoint/movenet_deploy.zip)

### PaddleLite部署模型单独下载

只使用paddlelite格式的模型，自己编译可执行文件

[movenet_s_paddlelite](https://bj.bcebos.com/v1/paddledet/models/keypoint/model_det_singlepose.zip)
[movenet_m_paddlelite](https://bj.bcebos.com/v1/paddledet/models/keypoint/model_det_multipose.zip)

### 经onnx转换后的Paddle模型单独下载

paddle原始格式的模型，自己转paddlelite格式

[movenet_s_paddle](https://bj.bcebos.com/v1/paddledet/models/keypoint/movenet_s_paddle.tar.gz)
[movenet_m_paddle](https://bj.bcebos.com/v1/paddledet/models/keypoint/movenet_m_paddle.tar.gz)

## movenet原模型下载地址

[movenet_singlepose](https://tfhub.dev/google/movenet/singlepose/lightning/4)
[movenet_multipose](https://tfhub.dev/google/movenet/multipose/lightning/1)

## 完整部署操作步骤及使用说明

[deploy_guide](deploy_guide.md)
