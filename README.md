### 大作业

### 环境配置

大作业需要安装的环境：jupyter notebook，python3.7。

大作业需要安装的库已经放在了requirements.txt文件中，运行pip install -r requirements.txt
安装即可，强烈建议使用anaconda新建一个python3.7的虚拟环境，在环境中安装避免不必要的麻烦。

除了requirements.txt中的必要库，还需要运行

```
conda install -n your-environment-name libpython
conda install -n your-environment-name -c msys2 m2w64-toolchain
```

这是编译cpython文件需要的库，因为卷积神经网络需要有效的实现，运行所需的函数都使用cpython写
好了，在使用之前还需要进入setup.py所在文件夹，使用运行如下指令进行编译：

```
python setup.py build_ext --inplace
```

数据集需要下载并解压到annp/dataset/文件夹下。

### 内容

#### 全连接神经网络（ 20 分）

依照FullConnectedNetwork.ipynb中的要求：

1. 实现affine layer的前向传播和反向传播并验证你的结果。
2. 实现ReLU激活函数的前向传播和反向传播
3. 利用你实现的affine layer和ReLU激活函数构建一个两层的全连接神经网络
4. 训练你实现的两层全连接神经网络，使测试结果的准确率达到50%以上
5. 构建多层的全连接网络，满足FullConnectedNetwork.ipynb中的测试要求

#### 归一化（ 20 分）

依照BatchNormalization.ipynb中的要求：

1. 实现batch normalization的前向传播和反向传播并验证你的结果
2. 修改你之前实现的全连接神经网络，添加batch normalization并验证你的结果，简要分析batch
normalization对神经网络的影响。
3. 实现layer normalization的前向传播和反向传播并验证你的结果
4. 修改你之前实现的全连接神经网络，添加layer normalization，对比batch normalization的结果
并分析两者的差异性

附加项：探究并分析weight initialization和batch size对batch normalization的影响。探究并分析batch
size对layer normalization的影响。（ 5 分）

#### CNN（ 20 分）

依照ConvolutionalNetwork.ipynb中的要求：

1. 实现CNN的前向传播和反向传播
2. 实现max pooling的前向传播和反向传播
3. 实现一个三层卷积神经网络
4. 实现spatial batch normalization

#### 实现ConvNet（ 40 分）

根据ConvolutionalNetwork.ipynb中Train your best model中的要求，利用annp文件夹中的模
块实现用于分类cifar-10数据集的卷积神经网络。需要注意的是，只能用annp文件夹中的模块实现你的
模型，不允许使用额外的深度学习框架。请各位同学仔细阅读annp文件夹中每个模块的用法。这一部分
的分数取决于你的实验结果以及对模型，方法以及结果的分析。


### 提交作业方式
一步一步跟随notebook:`FullyConnectedNets.ipynb`,`BatchNormalization.ipynb`,`ConvolutionalNetworks.ipynb`的指引，补齐代码。

并在notebook中保留相应的输出结果。

最后将final-project文件夹打包为压缩文件（注意：数据集文件无需提交，防止压缩包过大），以`期末大作业_姓名_学号`的格式发送至邮箱norwa99@163.com

### 截止日期
2022年12月31日23:59