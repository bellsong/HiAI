# [Stable Diffusion](https://github.com/CompVis/stable-diffusion) 介绍和使用

Stable Diffusion是一个文本到图像的潜在扩散模型，由CompVis、Stability AI和LAION的研究人员和工程师创建。它使用来自LAION-5B数据库子集的512x512图像进行训练。使用这个模型，可以生成包括人脸在内的任何图像，因为有开源的预训练模型，所以我们也可以在自己的机器上运行它。

Stable Diffusion是目前AIGC在生成图片方向上非常优秀一个工具，质量高，速度快，成本低等优点，可以说是AI生成图片领域的六边形战士。

如果你足够聪明和有创造力，你可以创造一系列的图像，然后形成一个视频。例如，Xander Steenbrugge使用它和上图所示的输入提示创建了下面这段令人惊叹的[《穿越时间》](https://avoid.overfit.cn/post/b4dfff8d1d1a4808a296c33b2e8a952b)视频。


## stable-diffusion-webui 

stable-diffusion-webui 是方便使用stable diffusion的一个开源工具 https://github.com/AUTOMATIC1111/stable-diffusion-webui

### 功能说明

stable-diffusion-webui 的功能很多，主要有如下 2 个：

* 文生图（text2img）：根据提示词（Prompt）的描述生成相应的图片。
* 图生图（img2img）：将一张图片根据提示词（Prompt）描述的特点生成另一张新的图片。

### 使用说明

1. 如何本地部署 Stable Diffusion
2. WebUI页面布局和参数配置
3. 如何更换底模型
4. 如何添加Lora模型以及如何避免易错点
5. 如何引入ControlNet
6. 如何重现生成的图片
7. 如何使用Stable Diffusion Reimagine 

####  本地如何部署 Stable Diffusion

1. 下载源码：https://github.com/AUTOMATIC1111/stable-diffusion-webui

####  搭建运行环境

####  配置运行环境

####  模型

模型文件有 2 种格式，分别是 .ckpt（Model PickleTensor） 和 .safetensors（Model SafeTensor），据说 .safetensors 更安全，这两种格式 stable-diffusion-webui 都支持。

将下载好的模型文件放到 stable-diffusion-webui\models\Stable-diffusion 目录下。

### 文生图 text2img 参数说明

| 参数 | 说明 |
| :--- | :--- |  
| Prompt | 提示词（正向）|
| Negative prompt| 消极的提示词（反向）|
| Width & Height | 要生成的图片尺寸。尺寸越大，越耗性能，耗时越久。|
| CFG scaleAI |  对描述参数（Prompt）的倾向程度。值越小生成的图片越偏离你的描述，但越符合逻辑；值越大则生成的图片越符合你的描述，但可能不符合逻辑。| 
| Sampling method | 采样方法。有很多种，但只是采样算法上有差别，没有好坏之分，选用适合的即可。| 
| Sampling steps | 采样步长。太小的话采样的随机性会很高，太大的话采样的效率会很低，拒绝概率高(可以理解为没有采样到,采样的结果被舍弃了)。Seed随机数种子。生成每张图片时的随机种子，这个种子是用来作为确定扩散初始状态的基础。不懂的话，用随机的即可。| 

### [AI绘画的精准控图(ControlNet)](https://juejin.cn/post/7209542304863502396)


## 参考

* [stable-diffusion](https://github.com/CompVis/stable-diffusion)

* https://github.com/AUTOMATIC1111/stable-diffusion-webui

* [Stable Diffusion的入门介绍和使用教程](https://avoid.overfit.cn/post/b4dfff8d1d1a4808a296c33b2e8a952b)
