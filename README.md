# BERT中文评论文段情感识别


## 实验环境

Python3.10

请确保安装以下依赖库：

- torch: 请参考[PyTorch官方网站](https://pytorch.org/get-started/locally/)安装
- datasets: 安装方式为 `pip install datasets`
- transformers: 安装方式为 `pip install transformers`
- lime: 安装方式为 `pip install lime`
- tkinter: 通常情况下tkinter是Python标准库的一部分，无需额外安装。


## 数据集下载

本实验使用的数据集为ChnSentiCorp情感分析数据集，可以通过以下链接下载：

- [ChnSentiCorp](https://huggingface.co/datasets/lansinuote/ChnSentiCorp)

代码中直接连接网络数据库，若不下载至本地需保持连接外网。

## 运行方式

安装依赖包；
打开中文分类.ipynb文件，依次运行代码块。


## 实验结果

在训练过程中，模型在训练集上的性能逐渐提升。以下是关键训练步骤的准确率和损失值的汇总：

| Iteration | Loss    | Accuracy   |
|-----------|---------|------------|
| 0         | 0.7289  | 43.75%     |
| 5         | 0.6516  | 75%        |
| 10        | 0.6336  | 62.5%      |
| 15        | 0.6248  | 62.5%      |
| 20        | 0.5915  | 75%        |
| ...       | ...     | ...        |
| 295       | 0.4023  | 93.75%     |
| 300       | 0.4661  | 81.25%     |

通过观察训练步骤，可以注意到模型的损失值逐渐下降，而准确率逐步提高。在训练的后期阶段，模型达到了较高的准确率，表明其在训练集上学到了有效的表示。

在验证集上进行测试，模型表现如下：

| Iteration | Accuracy   |
|-----------|------------|
| 1         | 93.75%     |
| 2         | 90.63%     |
| 3         | 84.38%     |
| 4         | 81.25%     |
| 5         | 78.13%     |
| 6         | 84.38%     |
| 7         | 87.50%     |
| 8         | 81.25%     |
| 9         | 84.38%     |
| 10        | 87.50%     |

通过测试，可以看到模型在验证集上表现良好，准确率相对较高。这进一步验证了模型在训练集上学到的知识在验证集上的泛化能力。

在样例测试中也有很好的情感识别效果。


天津大学 陆亮 2024.1.17
