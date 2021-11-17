# MoveNet-PaddleLite

Adapted from [PaddleDetection](https://github.com/PaddlePaddle/PaddleDetection);

Movenet cpp deploy based on [PaddleLite](https://github.com/PaddlePaddle/Paddle-Lite);

Movenet model transformed from tensorflow;



## 简介

Movenet是近年的优秀开源模型代表，原模型以Tensorflow模型格式开源。

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

**注：Paddle-Lite需使用最新版本v2.10，低版本不支持，也可从下面完整测试工程文件夹包种获取**




## movenet部署模型下载地址

### 完整测试工程文件夹包

下载后可直接在移动端部署测试, 除上述工程部署文件结构中提到的文件外，还包括两个文件夹[model_det_singlepose]、[model_det_multipose],分别是[model_det]文件夹的单人模型版本和多人模型版本。

[movenet_deploy.tar.gz](https://bj.bcebos.com/v1/paddledet/models/keypoint/movenet_deploy.zip)



### 模型单独下载地址

| 模型类别                 | singlepose模型                                               | multipose模型                                                |
| ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| PaddleLite部署模型       | [movenet_s_paddlelite](https://bj.bcebos.com/v1/paddledet/models/keypoint/model_det_singlepose.zip) | [movenet_m_paddlelite](https://bj.bcebos.com/v1/paddledet/models/keypoint/model_det_multipose.zip) |
| 经onnx转换后的Paddle模型 | [movenet_s_paddle](https://bj.bcebos.com/v1/paddledet/models/keypoint/movenet_s_paddle.tar.gz) | [movenet_m_paddle](https://bj.bcebos.com/v1/paddledet/models/keypoint/movenet_m_paddle.tar.gz) |
| movenet原始模型          | [movenet_singlepose](https://tfhub.dev/google/movenet/singlepose/lightning/4) | [movenet_multipose](https://tfhub.dev/google/movenet/multipose/lightning/1) |



## 完整部署操作步骤及使用说明

[deploy_guide](deploy_guide.md)
