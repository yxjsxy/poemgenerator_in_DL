# 基于 LSTM 的古诗生成

使用 Keras 和 LSTM-RNN 学习古诗文本，探索随机生成、藏头诗和给定开头续写。

## 内容

- `poem_model.ipynb`：训练与生成实验。
- `data_utils.py`：数据处理。
- `config.py`：语料、权重路径及训练参数。
- `poetry.txt`：诗歌语料。

## 使用方法

```bash
git clone https://github.com/yxjsxy/poemgenerator_in_DL.git
cd poemgenerator_in_DL
python3 -m venv .venv
source .venv/bin/activate
pip install jupyterlab
jupyter lab
```

打开 `poem_model.ipynb`，根据导入语句配置兼容的 Keras/TensorFlow 版本。运行前将 `config.py` 的语料路径指向实际的 `poetry.txt`：默认配置指向 `dataset/poetry.txt`，与根目录语料位置不同。

按 Notebook 顺序预处理、训练或加载自己已有的权重，再调用其中的诗歌生成函数。`poetry_model.h5` 是配置中的权重文件名，并非仓库已包含的预训练模型。

## 限制

此项目保留历史实验结构，没有依赖锁和统一命令行入口。旧版 Keras API 可能需要兼容环境或迁移。输出不保证格律、事实、语义或原创性；运行时间取决于训练配置与设备。
