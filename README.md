# 🖥️ ATM
The Paper that needs to be used 

## RL
### RL的基础方法
#### 1、DPO

1. introduction：通过直接优化偏好数据来训练模型，无需单独的奖励模型
2. paper: [https://arxiv.org/abs/2305.18290
](https://arxiv.org/abs/2305.18290)

#### 2、IPO

1. introduction：通过修改损失函数来解决DPO存在的问题，主要是损失的变化，IPO使用的是平方损失
2. paper: [https://arxiv.org/abs/2305.18290
](https://arxiv.org/abs/2305.18290)

#### other

1、基于动作分块的强化学习, 从全局考虑强化学习
   paper：[https://arxiv.org/abs/2507.07969](https://arxiv.org/abs/2507.07969)
   code:[https://github.com/ColinQiyangLi/qc?tab=readme-ov-file](https://github.com/ColinQiyangLi/qc?tab=readme-ov-file)

2、从死胡同中拯救对话：面向任务型对话策略优化的有效探索
  paper：[https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00717/125484](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00717/125484)

## Reward的相关论文

### Self-Evolved Reward Learning for LLMs
1. introduction：提出自进化奖励学习（Self-Evolved Reward Learning，SER）,大型语言模型的自进化奖励学习
2. paper: [https://arxiv.org/abs/2411.00418
](https://arxiv.org/abs/2411.00418)
3. code: [https://github.com/microsoft/DKI_LLM/tree/main](https://github.com/microsoft/DKI_LLM/tree/main)


 ## 上下文的工作的的相关论文

### content to content
1. introduction：
2. code: [https://github.com/RUCAIBox/Opt-Visor](https://github.com/RUCAIBox/Opt-Visor)

## ATM related work

### CoMat ★★★
1. Aligning Text-to-Image Diffusion Model with Image-to-Text Concept Matching
2. paper: [https://arxiv.org/abs/2404.03653](https://arxiv.org/abs/2404.03653)
3. code: [https://github.com/CaraJ7/CoMat](https://github.com/CaraJ7/CoMat)


### paper idea and some thinking
1. 使用rm_training [https://github.com/microsoft/DKI_LLM/blob/main/SER/rm_training/rm_training.py] 来替换 强化学习中的reward function
2. 在rm_training 的 value 考虑添加交叉注意力， 文本嵌入和图像嵌入，找到语句中的关键词与图像中的对应  然后再到pool 再forward到 head。
3. 依旧是一个核心问题：我的目的是减少迭代次数，最终目的用户作为reinforncement learning来引导的梯度走向，那其实应该是有一个初始图和一个对应的文字。
4. 还有一个 毕竟走死胡同的 RL
