# tensorflow
TensorFlow学习

一、简介
使用 TensorFlow, 你必须明白 TensorFlow:
  使用图 (graph) 来表示计算任务.
  在被称之为 会话 (Session) 的上下文 (context) 中执行图.
  使用 tensor 表示数据
  通过 变量 (Variable) 维护状态.
  使用 feed 和 fetch 可以为任意的操作(arbitrary operation) 赋值或者从其中获取数据.
  
TensorFlow 是一个编程系统, 使用图来表示计算任务. 图中的节点被称之为 op (operation 的缩写). 一个 op 获得 0 个或多个 Tensor, 执行计算, 产生 0 个或多个 Tensor. 每个 Tensor 是一个类型化的多维数组. 简而言之，图是由op构成，然后op之间由Tensor进行流动交互。

一个 TensorFlow 图描述了计算的过程. 为了进行计算, 图必须在 会话 里被启动. 会话 将图的 op 分发到诸如 CPU 或 GPU 之类的 设备 上, 同时提供执行 op 的方法. 这些方法执行后, 将产生的 tensor 返回. 在 Python 语言中, 返回的 tensor 是 numpy ndarray 对象; 在 C 和 C++ 语言中, 返回的 tensor 是 tensorflow::Tensor 实例.

详细见http://www.tensorfly.cn/tfdoc/get_started/basic_usage.html 

二、MNIST数据集训练

MNIST是在机器学习领域中的一个经典问题。该问题解决的是把28x28像素的灰度手写数字图片识别为相应的数字，其中数字的范围从0到9.
http://yann.lecun.com/exdb/mnist/提供了训练集与测试集数据的下载。
train-images-idx3-ubyte.gz包含 训练集图片 - 55000 张 训练图片, 5000 张 验证图片
train-labels-idx1-ubyte.gz包含 训练集图片对应的数字标签
t10k-images-idx3-ubyte.gz包含  测试集图片 - 10000 张 图片
t10k-labels-idx1-ubyte.gz包含  测试集图片对应的数字标签

首先选用简单的两层神经网络，训练分类成功率可以达到95%，代码见2.1




