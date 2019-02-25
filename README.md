# NSFW Model

This repo contains code for running Not Suitable for Work (NSFW) classification.

[online demo](http://ai.midday.me/)

## Usage

#### script 

```bash
python nsfw_predict.py /tmp/test/test.jpeg
```

result : 
```bash
{'class': 'sexy', 'probability': {'drawings': 0.008320281, 'hentai': 0.0011919827, 'neutral': 0.13077603, 'porn': 0.13146976, 'sexy': 0.72824186}}
```

can find the meaning of every label at repo [nsfw_data_scrapper](https://github.com/alexkimxyz/nsfw_data_scrapper)

#### Deploy by TensorFlow Serving

your have to install [Tensorflow Serving](https://www.tensorflow.org/serving/) first

start the server
```bash
./start_tensorflow_serving.sh
```

test server
```bash
python serving_client.py /tmp/test/test.jpeg
```


## Train

train code at [resnet](./resnet)

train a new model

1. convert source to tfrecord user ```convert_image_to_tfrecord.py```
2. train a model from scratch or fine tune

the model code copy from [Tensorflow offical model](https://github.com/tensorflow/models/tree/master/official/resnet)


## Data

you can find the detail at repo [nsfw_data_scrapper](https://github.com/alexkimxyz/nsfw_data_scrapper)


# NSFW Model

This repo contains code for running Not Suitable for Work (NSFW) classification.

[online demo](http://ai.midday.me/)

## Usage

#### script 

```bash
python nsfw_predict.py /tmp/test/test.jpeg
```

result : 
```bash
{'class': 'sexy', 'probability': {'drawings': 0.008320281, 'hentai': 0.0011919827, 'neutral': 0.13077603, 'porn': 0.13146976, 'sexy': 0.72824186}}
```

can find the meaning of every label at repo [nsfw_data_scrapper](https://github.com/alexkimxyz/nsfw_data_scrapper)

#### Deploy by TensorFlow Serving

your have to install [Tensorflow Serving](https://www.tensorflow.org/serving/) first

start the server
```bash
./start_tensorflow_serving.sh
```

test server
```bash
python serving_client.py /tmp/test/test.jpeg
```


## Train

train code at [resnet](./resnet)

train a new model

1. convert source to tfrecord user ```convert_image_to_tfrecord.py```
2. train a model from scratch or fine tune

the model code copy from [Tensorflow offical model](https://github.com/tensorflow/models/tree/master/official/resnet)


## Data

you can find the detail at repo [nsfw_data_scrapper](https://github.com/alexkimxyz/nsfw_data_scrapper)

有人上手了！

近日， GitHub出现一个名为“NSFW Model”的项目。通俗一点来说，就是一个鉴黄模型。


这个模型，使用的数据来自前不久量子位介绍的那个数据集，内含多20万张“不可描述”图片。



同时，这个模型也被项目的贡献者做成了Demo。

既然有了Demo，那肯定是免不了测试一番……

Demo效果

Demo网站十分简单，进去之后能做什么一目了然。

上传图片之后，是自动给出结果，不需要点击其他按钮。但有时候不会给出结果…..还有待完善。

结果是数据集中提到的5种类别的可能性。分别是：hentai、sexy、neutral、drawings、porn。具体每个类别代表的意思，如下图所示：



好了，开始第一个测试：


这个图有71%的可能性是hentai；16%的可能性是porn。你觉得准吗？

再来一个：


71%的可能性是sexy。

但下面这个，就有点不好说了。


porn到了76%，19%是hentai。按照这个标准，《超体》别想正常上映了……

但整体上，这个模型还是能工作的，比如整个漫画，就很好的识别出来了，比如其他的一些，也能识别出来（但图片就不好放了）。


至于准确率怎么样，没法给出定论。如果你有兴趣，可以去体验下这个Demo。地址：

http://ai.midday.me/

话说话来，看到这个模型，你有没有想自己上手体验一下？GitHub有相关的开源代码。

请收好项目地址：

https://github.com/rockyzhengwu/nsfw

最后，数据集地址：

https://github.com/alexkimxyz/nsfw_data_scrapper

One More Thing

在Demo网站的下方，写了一句爱因斯坦的话：

Two things are infinite: the universe and human stupidity; and I’m not sure about the universe.

只有两样东西是无限的，就是宇宙，还有人类的愚蠢，不过我对前者还没什么把握。


 
 
