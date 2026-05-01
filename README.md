# LSTM-中英文机器翻译

​本项目实现了一个基于LSTM的序列到序列（Seq2Seq）架构的神经网络机器翻译系统，能够将英语翻译成中文。项目采用双向LSTM作为编码器，单向LSTM作为解码器，并引入了注意力机制来提升翻译质量。

## 技术特点：

- **编码器**：双向LSTM（BiLSTM），能够捕获前后文信息
- **解码器**：单向LSTM，支持注意力机制
- **注意力机制**：全局注意力机制，帮助解码器关注源序列的不同部分
- **词嵌入**：可学习的词嵌入层，维度为256
- **数据处理**：使用jieba进行中文分词，支持词汇表过滤和特殊标记

## 项目结构

```
LSTM-chinese_english_translation/
├── DATA_LICENSE.md        # 数据集声明
├── LICENSE                # 开源协议
├── LSTM-机器翻译.ipynb     # 主程序代码（Jupyter Notebook）
├── README.md              # 项目说明文档
└── data.xls               # 中英平行语料数据集
```

## 环境依赖

- 请点击具体jupyter notebook文件`LSTM-机器翻译.ipynb`查看。

## 模型参数

| 参数           | 值    |
| -------------- | ----- |
| 嵌入维度       | 256   |
| 隐藏层维度     | 512   |
| LSTM层数       | 2     |
| Dropout        | 0.3   |
| 批量大小       | 64    |
| 最小词频       | 2     |
| 最大词汇表大小 | 50000 |

## 使用方法

1. 打开 `LSTM-机器翻译.ipynb` 文件
2. 按顺序运行各个代码单元格
3. 模型将自动加载数据、训练并评估

## 数据集

使用 `data.xls` 作为训练数据，包含中英平行句对。

数据集来自：`https://www.kaggle.com/datasets/thespringcomes/translationcmn3`

## 训练说明

- 支持GPU加速（CUDA）
- 使用随机种子保证结果可复现
- 支持模型保存和加载
- 包含训练过程的可视化

## 作者信息

**谙弆悕博士（Ailan Anjuxi）**

- 邮箱：anjuxi.ME@outlook.com
- SIP电话：sip:anjuxi@sip.linphone.org

---

*本项目仅供学习和研究使用*
