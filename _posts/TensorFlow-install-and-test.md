---
layout: post
title:  "hello jekyll!"
date:   2015-02-10 15:14:54
categories: jekyll
tags: jekyll
excerpt: TensorFlow 安装教程及测试
mathjax: true
---
安装python3.5.x

下载：python3.5.2
第一个Install Now是默认安装在c盘的，第二个是自己选择安装路径。 
我选择第二个，同时将Add Python 3.5 to PATH勾选上。 
我没有勾选最后一项，虽然安装成功了，但是运行的时候报错，所以最好都选上。然后开始进行安装。 
安装成功后
安装tensorflow
进入CMD运行
```shell
 pip install tensorflow
# 或
> pip install --upgrade https://storage.googleapis.com/tensorflow/windows/cpu/tensorflow-0.12.0rc0-cp35-cp35m-win_amd64.whl
```
安装成功后测试
打开idle把下列代码保存为test.py文件
```python
import tensorflow as tf

# 创建常量
hello = tf.constant('Hello,world!')

# 创建会话
sess = tf.Session()

# 执行
result = sess.run(hello)

# 关闭会话
sess.close()

# 输出结果
print(result)
```
按F5
如果出现以下结果则安装成功

b'Hello,world!'
