[English](NotGoodIdeas.md)<br>**简体中文 · English–Chinese**

本双语文件依据英文版 `NotGoodIdeas.md` 翻译整理；原文件保持不变，以便后续同步更新。

[Zhihu link](https://www.zhihu.com/question/347847220/answer/26536819499)<br>[知乎链接](https://www.zhihu.com/question/347847220/answer/26536819499)

When reviewing papers or reading them, I have become aware of numerous not good practices, and I wish to document these.<br>在评审或阅读论文的过程中，我注意到了许多不良做法，因此希望将它们记录下来。

### Computational Power Overwhelming 算力碾压

1.1 Increase the batch size to seemingly align the number of iterations.<br>1.1 增大批量大小，让迭代次数看起来与其他方法一致。

1.2 Train for more epochs without explicitly stating it, report the training duration in terms of iterations instead of epochs, or vice versa, to obscure the lack of alignment.<br>1.2 在不明确说明的情况下训练更多轮次，并用迭代次数而非训练轮次来报告训练时长，或反过来，以掩盖训练量并未对齐的事实。

1.3 Keep the number of epochs constant but reuse samples multiple times to cover more data surreptitiously.<br>1.3 保持训练轮次不变，却多次重复使用样本，从而暗中覆盖更多数据。

1.4 Reduce the downsampling frequency in the model, increasing the computational load significantly, yet only compare parameter counts with others.<br>1.4 降低模型中的下采样频率，大幅增加计算量，却只与其他方法比较参数量。

1.5 Pile on computational power in domains where computational load and parameter count are disregarded.<br>1.5 在不重视计算量和参数量的领域直接堆砌算力。

1.6 Briefly mention high-computation components and only analyze the efficiency of other components.<br>1.6 对高计算量组件一笔带过，只分析其他组件的效率。

1.7 Use reparameterization to inflate the model size, making training slower but disregarding the inference overhead.<br>1.7 使用重参数化扩大模型规模，使训练速度变慢，却不考虑推理开销。

1.8 Employ EMA (Exponential Moving Average) or model ensembles to boost performance, and if possible, self-distillation.<br>1.8 使用 EMA（指数移动平均）或模型集成来提升性能，如果条件允许，再加入自蒸馏。

1.9 Select an extremely small training set, allowing focus solely on overfitting.<br>1.9 选择极小的训练集，以便专注于过拟合。

### Hyperparameters 超参数

2.1 Manipulate experimental results by switching between cosine learning rate schedules and fixed learning rates (the latter stages of cosine schedules often lead to rapid performance gains, so prematurely reducing the learning rate can make training appear more efficient).<br>2.1 通过在余弦学习率调度与固定学习率之间切换来操纵实验结果（余弦调度的后期往往会带来快速的性能提升，因此提前降低学习率可以让训练显得更高效）。

2.2 Slightly increase the learning rate while decreasing the baseline's learning rate.<br>2.2 略微提高自己方法的学习率，同时降低基线方法的学习率。

2.3 Conceal various hyperparameters within the code as "magic numbers."<br>2.3 将各种超参数作为“魔数”隐藏在代码中。

2.4 Cherry-pick random seeds.<br>2.4 挑选结果有利的随机种子。

### Minor Tweaks 微小改动

If one tweak is important, it should be stated in the paper. Many papers conceal their tweaks.<br>如果某项改动很重要，就应该在论文中明确说明。许多论文却会隐藏这些改动。

3.1 Replace all ReLU activations with Swish or Leaky ReLU/PReLU.<br>3.1 将所有 ReLU 激活函数替换为 Swish 或 Leaky ReLU/PReLU。

3.2 Add SE (Squeeze-and-Excitation) layers throughout the model, as they generally improve performance; incorporate inexpensive attention connections.<br>3.2 在模型各处加入 SE（Squeeze-and-Excitation）层，因为它们通常能提升性能；同时加入计算成本较低的注意力连接。

3.3 Replace parameter-free components like pooling and resizing with learnable ones to gain extra capacity.<br>3.3 将池化、尺寸调整等无参数组件替换为可学习组件，以获得额外的模型容量。

3.4 Arbitrarily add skip connections between modules and concatenate additional features, as it rarely hurts.<br>3.4 随意在模块之间加入跳跃连接并拼接额外特征，因为这样通常不会让结果变差。

3.5 Add Batch Normalization (BN) where it's absent, remove it where it's present, or experiment with other normalization techniques like Group Normalization (GN), Instance Normalization (IN), Layer Normalization (LN), or Weight Normalization (WN).<br>3.5 在没有 Batch Normalization（BN）的地方加入它，在已有 BN 的地方移除它，或者尝试 Group Normalization（GN）、Instance Normalization（IN）、Layer Normalization（LN）或 Weight Normalization（WN）等其他归一化技术。

3.6 Augment the training set to align with the test set distribution, altering the training set's characteristics.<br>3.6 对训练集进行数据增强，使其与测试集分布对齐，从而改变训练集的特性。

### Incremental Designs 增量式设计

4.1 Incorporate peculiar GAN losses or consistency losses, which are difficult to assess but can fill pages with formulas.<br>4.1 引入奇特的 GAN 损失或一致性损失；它们虽然难以评估，却可以用大量公式填满论文篇幅。

4.2 Elaborate on techniques mentioned briefly in others' papers, adding "magical" formula transformations to extend the manuscript.<br>4.2 将其他论文中简略提及的技术展开描述，再加入“神奇”的公式变换，以扩充稿件篇幅。

4.3 When designing a new component x, create a learnable parameter beta initialized to 0, and add beta * x to the model instead of x alone. In the worst case, beta remains 0, leaving the model unchanged.<br>4.3 设计新组件 x 时，创建一个初始化为 0 的可学习参数 beta，并向模型中加入 beta * x，而不是直接加入 x。最坏的情况下，beta 始终为 0，模型便不会发生变化。

4.4 Extend the previous point by designing multiple components and combining them with learnable parameters.<br>4.4 在上一条的基础上继续扩展：设计多个组件，再通过可学习参数将它们组合起来。

4.5 Further extend by incorporating Neural Architecture Search (NAS).<br>4.5 再进一步，引入神经架构搜索（NAS）。

4.6 Utilize pre-trained parameters from other models to elevate the starting point and potential upper bound of the model, akin to adding more data and annotations.<br>4.6 使用其他模型的预训练参数，提高模型的起点与潜在性能上限，其效果类似于加入更多数据和标注。

4.7 Implement complex curriculum learning or elaborate distillation techniques (feature-level, cross-modal, etc.). If others struggle to reproduce the results, attribute it to the need for hyperparameter tuning.<br>4.7 采用复杂的课程学习或精巧的蒸馏技术（特征级、跨模态等）。如果别人难以复现实验结果，就将原因归结为需要调节超参数。

4.8 Regardless of utility, apply a reinforcement learning framework to imbue the model with more autonomy.<br>4.8 无论是否有用，都套用一个强化学习框架，让模型显得更具自主性。

### Evaluation Methods 评估方法

5.1 Measure ten metrics but only report the three showing improvement.<br>5.1 评测十项指标，却只报告其中有所提升的三项。

5.2 Conduct experiments on ten datasets but discard the five without favorable results.<br>5.2 在十个数据集上开展实验，却舍弃结果不理想的五个数据集。

5.3 Deliberately misalign the testing method with others' training scenarios to lower the baseline, e.g., inverting RGB channels to sabotage competitors.<br>5.3 故意让测试方法与其他工作的训练设定不匹配，以压低基线结果，例如颠倒 RGB 通道来破坏竞争方法的表现。

5.4 Invent novel evaluation metrics or modify existing ones, such as measuring PSNR on the Y channel while comparing it to RGB measurements.<br>5.4 发明新的评估指标或修改现有指标，例如在 Y 通道上计算 PSNR，却与基于 RGB 计算的结果比较。

5.5 Identify trivial yet overlooked scenarios to demonstrate substantial improvements.<br>5.5 找出无关紧要但常被忽略的场景，以展示大幅提升。

5.6 Compare a large model against others' smaller models without reporting their larger counterparts, or compare a model trained for a specific metric against untrained ones.<br>5.6 用自己的大模型与他人的小模型比较，却不报告对方更大规模的版本；或者将针对特定指标训练过的模型与未针对该指标训练的模型进行比较。

5.7 Test on different hardware and report the results together.<br>5.7 在不同硬件上进行测试，却将结果放在一起报告。

5.8 For recent large language models, surreptitiously add hints to test prompts, comparing few-shot and zero-shot performance.<br>5.8 对于近期的大语言模型，暗中在测试提示中加入线索，再将少样本性能与零样本性能进行比较。

5.9 Indirectly overfit to the test set by leaking data or random seeds, or include test samples in upstream pre-training.<br>5.9 通过泄露数据或随机种子间接过拟合测试集，或者在上游预训练中包含测试样本。

5.10 Introduce real-world scenarios or out-of-distribution (OOD) samples to the test set, causing significant drops in baseline performance. Then, apply augmentations or dropout to recover the lost performance, attributing the gains to other factors.<br>5.10 在测试集中引入真实世界场景或分布外（OOD）样本，使基线性能大幅下降；随后使用数据增强或 dropout 恢复损失的性能，却将提升归因于其他因素。

5.11 Use private test sets with subjective human judgment, allowing arbitrary claims of improvement.<br>5.11 使用依赖主观人工判断的私有测试集，从而可以任意宣称性能有所提升。

5.12 If objective comparisons fail, resort to subjective ones, and if subjective comparisons fail, selectively present favorable results (cherry-picking).<br>5.12 如果客观比较不占优势，就改用主观比较；如果主观比较也不占优势，就选择性展示有利结果。

### Ultimate Methods 终极手段

6.1 Replicate someone else's method but rename it entirely.<br>6.1 复现他人的方法，却彻底换一个名字。

6.2 Report high performance but only provide a README when asked for the source code.<br>6.2 宣称性能很高，但在别人索要源代码时只提供一份 README。

6.3 Begin writing the paper without conducting experiments, conveniently surpassing the state-of-the-art by a narrow margin.<br>6.3 尚未开展实验便开始撰写论文，最后恰好以微弱优势超过当前最佳水平。

**Reiterating, the above are cautionary examples meant to serve as a guide against deceptive practices.**<br>**再次强调，以上内容均为警示性反例，旨在提醒大家避免欺骗性做法。**
