# Lab 3 — CNN training (AlexNet / VGG16 / ResNet50)

Computer Vision 实验三：从头训练三个卷积网络并对比。

## 内容

| 路径 | 说明 |
|---|---|
| `lab3_colab.ipynb` | 训练主程序（在 Google Colab 上运行）|
| `testset/` | 自建的 50 张测试图（10 类 × 5 张）与标签 |

## 使用方法

1. 在 Colab 里打开 `lab3_colab.ipynb`；
2. 顶部把 `GH_USER` 与 `GH_REPO` 改成你自己的 GitHub 用户名与本仓库名；
3. 运行时选择 T4 GPU；
4. 依次运行全部单元。

## 数据

训练与验证数据来自 ImageNette（ImageNet 的十个类别子集），
通过 HuggingFace 在运行时下载，不放在仓库里。

测试集的 50 张图由本人从 Wikimedia Commons 收集并标注，
与训练集无重叠。

## 说明

- 三个模型均使用 `weights=None`，即**不使用任何预训练权重**，全部从头训练；
- 输入统一为 128×128（标准为 224，为降低计算量而缩小）；
- 三个模型超参数完全相同，保证对比公平。
