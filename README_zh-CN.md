[English](README.md)<br>**简体中文 · English–Chinese**

本双语文件译自上游英文 README，保留完整英文并附上中文译文；README.md 保持不变，以便后续同步上游更新。

# Writing AI Conference Papers: A Handbook for Beginners AI 会议论文写作：新手指南

**We believe that what this article needs the most is peer review, and we warmly welcome valuable suggestions in any form.**<br>**我们认为，本文最需要的是同行评审，诚挚欢迎大家以任何形式提出宝贵建议。**

Author: [hzwer](https://github.com/hzwer), [DingXiaoH](https://github.com/DingXiaoH)<br>作者：[hzwer](https://github.com/hzwer)、[DingXiaoH](https://github.com/DingXiaoH)

知乎 [1](https://zhuanlan.zhihu.com/p/593195527)-[2](https://zhuanlan.zhihu.com/p/639732057)-[3](https://zhuanlan.zhihu.com/p/627032371)｜[跃问中翻](https://yuewen.cn/share/145749938443137024?utm_source=share&utm_content=web_linkcopy&version=2) | [豆包总结](https://www.doubao.com/thread/w750d882cf0af6419) | [公众号](https://mp.weixin.qq.com/s/MjeBZDV6xapuA_L6ODpVcA)<br>知乎 [1](https://zhuanlan.zhihu.com/p/593195527)-[2](https://zhuanlan.zhihu.com/p/639732057)-[3](https://zhuanlan.zhihu.com/p/627032371)｜[跃问中文翻译](https://yuewen.cn/share/145749938443137024?utm_source=share&utm_content=web_linkcopy&version=2) | [豆包总结](https://www.doubao.com/thread/w750d882cf0af6419) | [公众号文章](https://mp.weixin.qq.com/s/MjeBZDV6xapuA_L6ODpVcA)

**Abstract.** *Crafting a research manuscript can pose significant challenges for novices, particularly when time is scarce before the deadline and the authors lack experience in academic submissions. An ill-prepared manuscript can be a source of distress for both collaborators and readers, frequently leading to rejection or necessitating substantial revisions. In this article, we'll share some tips for beginners who want to write AI conference papers. Our goal is for this article to be a guide for beginners, making it easier to share academic achievements.*<br>**摘要。** *撰写研究论文稿件对新手而言可能是一项艰巨的挑战，尤其是在临近截稿期、时间紧迫，而作者又缺乏学术投稿经验的情况下。准备不足的稿件会让合作者和读者都感到困扰，往往导致拒稿，或需要大幅修改。本文将为希望撰写 AI 会议论文的新手分享一些建议。我们希望本文能成为新手的入门指南，帮助大家更顺利地分享学术成果。*

## Introduction 引言

> **Background.** The GPU cluster has been running for half a year, and you feel that the results are already significant. You realize that the deadline for an upcoming conference is less than a month away, yet you have only written some course assignment reports. How far in advance should the first draft be completed to avoid missing the deadline? What distinguishes a good research paper from a bad one? What should be done before starting to write? These questions plague you like a nightmare, leaving you staring at the blank Overleaf homepage. Luckily, this article is written for you. <br>**背景。** GPU 集群已经运行了半年，你觉得实验结果已经相当可观。此时你发现，距离即将召开的某个会议的截稿期已经不到一个月，而你此前只写过一些课程作业报告。初稿应该提前多久完成，才能避免错过截稿期？好的研究论文与差的论文有什么区别？动笔之前应该做些什么？这些问题如噩梦般困扰着你，让你只能盯着空白的 Overleaf 首页发呆。幸运的是，本文正是为你而写的。

In this article, we will discuss the aspects related to writing conference papers, with a focus on common pitfalls, catering to novices. Our article mainly consists of two parts: **[completing a paper](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#build-a-paper-from-scratch)** and **[refining its details](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#readability-improvement)**. We aim to provide practical guidance that will enable novices to navigate the complexities of academic writing and contribute to the field with clarity and confidence. Sincerely, we recommend the [Resource List of Writing Tips](https://vision.sjtu.edu.cn/writing.html) curated by Chao Ma.<br>本文面向新手，讨论会议论文写作的各个方面，重点介绍常见的误区。本文主要分为两部分：**[完成一篇论文](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#build-a-paper-from-scratch)**与**[打磨论文细节](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#readability-improvement)**。我们希望提供实用的指导，帮助新手应对学术写作中的复杂问题，清晰、自信地表达自己的研究，为本领域作出贡献。我们也诚挚推荐 Chao Ma 整理的[写作建议资源清单](https://vision.sjtu.edu.cn/writing.html)。

## Build a Paper from Scratch 从零开始完成一篇论文

This section outlines writing an AI paper from scratch, covering core idea, whole framework, introduction and related work.<br>本节概述如何从零开始撰写一篇 AI 论文，涵盖核心思想、整体框架、引言和相关工作。

### Find the Core Idea 找到核心思想
You may have interesting findings and experimental results, but you're unsure how to define the core theme. *The key contribution of most published papers falls into exactly one out of the following three categories (from [Nowozion](https://www.nowozin.net/sebastian/blog/ten-tips-for-writing-cs-papers-part-1.html)):*<br>你可能已经有了一些有趣的发现和实验结果，却还不确定如何提炼核心主题。*大多数已发表论文的关键贡献，恰好属于以下三类中的一类（引自 [Nowozion](https://www.nowozin.net/sebastian/blog/ten-tips-for-writing-cs-papers-part-1.html)）：*

*Insight: you have an explanation for something that is already there.*<br>*洞见：你能解释某种已存在的现象。*

*Performance: you can do something better.*<br>*性能：你能把某件事做得更好。*

*Capability: you can do something that could not be done before.*<br>*能力：你能做到以前做不到的事。*

Identify the core advantages of your work and emphasize them early in the paper. This way, readers can read the remaining parts with expectations. You can further expand the overall novelty from other aspects as well. **Novelty seems to be elusive, what is it?** Key research topics, efficient solutions, and innovative technical contributions are the primary elements that contribute to a paper's novelty. For instance, numerous early influential works of deep learning emerged from foundational model research due to their potential to impact the entire field. The RAFT/NeRF methods have attracted a large number of researchers due to their outstanding performance, and they involve a lot of engineering handling beyond their core ideas. Techniques such as "Batch Normalization" and "Residual Learning" are esteemed for their effectiveness. By emphasizing the novelty of your work, you'll be able to discern which aspects are worth the effort and which are inconsequential details.<br>找出你的工作的核心优势，并在论文开篇就加以强调。这样，读者就能带着期待阅读后续内容。你也可以从其他方面进一步丰富工作的整体新颖性。**新颖性似乎难以捉摸，它究竟是什么？** 重要的研究课题、高效的解决方案和创新性的技术贡献，是构成论文新颖性的主要要素。例如，早期许多具有影响力的深度学习工作都源于基础模型研究，因为这类研究有可能影响整个领域。RAFT/NeRF 方法凭借出色的性能吸引了大量研究者；除了核心思想，它们还包含许多工程处理。像“Batch Normalization”和“Residual Learning”这样的技术，则因其有效性而备受推崇。明确并突出工作的新颖性，有助于你分辨哪些方面值得投入精力，哪些只是无关紧要的细节。

> A little squiggle of paint by Picasso can be as beautiful as an intricate painting by Rembrandt. —— [Novelty in Science](https://medium.com/@black_51980/novelty-in-science-8f1fd1a0a143) (highly recommended for readers)<br>Picasso 随手画下的一小笔，也可以像 Rembrandt 精心绘制的复杂画作一样美。—— [科学中的新颖性](https://medium.com/@black_51980/novelty-in-science-8f1fd1a0a143)（强烈推荐读者阅读）

***Take-away: Clearly understand the increment over previous methods and find one or two core ideas.***<br>***要点：明确理解相较于以往方法的增量，找到一两个核心思想。***

When readers read papers, they seek novel insights. A good paper should have strong points that are easy to remember. You should refine your central ideas until you're confident that people will be eager to learn about them and share them widely. It is particularly worth noting that some ideas may be great, but if they lack originality, it may not be advisable to describe them in detail in the paper. When writing a paper, the focus should be on providing novel, unique, and valuable insights to attract readers' attention and inspire their interest.<br>读者阅读论文，是为了获得新的洞见。一篇好论文应该有让人容易记住的亮点。你应当不断提炼核心思想，直到确信大家会愿意了解它们，并广泛分享。尤其需要注意的是，有些想法即使很好，如果缺乏原创性，也未必适合在论文中详细展开。写论文时，应着重提供新颖、独特且有价值的洞见，以吸引读者的注意力，激发他们的兴趣。

Don't underestimate the novelty of your own work. Delve deep to uncover the underlying principles. If the ResNet paper were rewritten as: "We designed a model using a large number of $3\times3$ convolutions (inspired by VGGNet) and parallel shortcuts (simplified from GoogleNet) **based on** the former two", then it will also become a paper without novelty. The story told by the ResNet paper is to propose a problem, abstract the underlying principles, propose its own solutions and specific implementations, and verify them experimentally. This might not totally reflect [their research process](https://www.zhihu.com/question/406913672/answer/1339549216), but it effectively showcases their discoveries.<br>不要低估自己工作的新颖性，要深入挖掘其背后的原理。如果把 ResNet 论文改写为：“我们使用大量的 $3\times3$ 卷积（受 VGGNet 启发）和平行的快捷连接（由 GoogleNet 简化而来），**基于**前述两者设计了一个模型”，那么它也会变成一篇缺乏新颖性的论文。ResNet 论文的叙事方式是：提出问题，抽象出背后的原理，提出自己的解决方案与具体实现，再通过实验加以验证。这未必完全反映了[他们的研究过程](https://www.zhihu.com/question/406913672/answer/1339549216)，却有效地展示了他们的发现。

***Take-away: Discovering new phenomena and sharing new ideas matter more than performance gains.***<br>***要点：发现新现象、分享新思想，比性能提升更重要。***

A good number of excellent papers often show strong results in experiments. This can make people think that good results are all that matters in a paper. But actually, experimental results are just proof of new discoveries. Small improvements in results don't always mean new knowledge. When you write a paper, think first about what new things readers can learn from your work—not just about showing off better results than others.<br>许多优秀论文往往有出色的实验结果，这容易让人以为好结果就是论文的一切。但实际上，实验结果只是新发现的证据，结果上的小幅提升并不总意味着产生了新知识。写论文时，应先思考读者能从你的工作中学到什么新东西，而不只是展示比别人更好的结果。

In addition, as Kaiming He points out, researchers should focus on the future rather than solely on past "state-of-the-art." By applying Occam's Razor—seeking simple yet effective solutions—and validating research in real scenarios while forecasting experimental outcomes and future needs, researchers can reduce "overfitting" in their studies. Rather than meticulously refining experimental designs and metrics solely for immediate validation, it's more valuable to consider the long-term correctness and relevance of the work during the paper-writing process. The enduring, correct discoveries sustain their influence over time. By stripping away convoluted techniques used merely for paper publication and identifying straightforward, effective solutions, researchers increase the likelihood of their work generalizing to future scenarios.<br>此外，正如 Kaiming He 所指出的，研究者应当着眼未来，而不应只关注过去的“state-of-the-art”。运用奥卡姆剃刀原则，寻求简单而有效的解决方案，并在真实场景中验证研究，同时预判实验结果和未来需求，有助于减少研究中的“过拟合”。与其仅为眼前的验证而精细打磨实验设计和指标，不如在论文写作过程中更多考虑工作的长期正确性和相关性。经得住时间检验的正确发现，才能持续产生影响。剥离那些仅为发表论文而采用的繁复技巧，找出直接有效的解决方案，能提高研究成果泛化到未来场景的可能性。

### Construct the Framework 构建整体框架
***Take-away: Abstract - Introduction - Main body, which are gradually unfolded. Each part is self-complete.***<br>***要点：摘要—引言—正文，逐层展开，每一部分都应自成一体。***

The typical structure of a paper includes 1. an abstract, 2. an introduction, and 3. the main body, which encompasses sections such as related work, methodology, experiments, discussion, conclusion, and references. We can break down this structure into three levels. At each level, you should aim to convey a comprehensive research narrative. Each level serves as an expansion of the preceding one. With this understanding, let's explore how to effectively present a research story. For those who are starting out, it's advisable to focus on completing the main body of the paper first.<br>论文的典型结构包括 1. 摘要、2. 引言和 3. 正文；正文涵盖相关工作、方法、实验、讨论、结论和参考文献等部分。我们可以将这一结构分为三个层次，每个层次都应力求完整地讲述研究，每一层都是对上一层的扩展。理解这一点后，我们再来探讨如何有效地呈现研究。对于初学者，建议先集中精力完成论文正文。

***Take-away: Consider the target audience, introduce the valuable findings rather than the tortuous research process.***<br>***要点：考虑目标读者，介绍有价值的发现，而不是曲折的研究过程。***

While adhering to the core ideas, start outlining the content you intend to present in your paper. Begin by creating a simple slide to demonstrate your research approach and achievements to your peers, colleagues, or mentors, in order to assess their understanding. It may be beneficial to intentionally seek feedback from researchers unfamiliar with your work to identify potential gaps in comprehension. Unlike the experimental process, it is advisable to emphasize valuable novelties and avoid presenting incomplete or complex aspects of your research. Researchers all understand the pain of research, but the bitter portrayal is only suitable for the postscript of the project. Continuously review and refine your presentation from the reader's perspective until it is easily understandable.<br>围绕核心思想，开始梳理论文要呈现的内容。可以先制作一张简明的幻灯片，向同行、同事或导师展示你的研究思路和成果，以了解他们能否理解。主动向不熟悉你工作的研究者征求反馈，有助于找出理解上的障碍。论文呈现不同于实验过程的记录，建议突出有价值的新发现，避免展示研究中尚不完整或过于复杂的部分。研究者都理解科研的艰辛，但对苦难的描绘只适合放在项目后记中。要不断从读者的角度审视、打磨表述，直到内容易于理解。

It may also be necessary to supplement your work with additional experiments if you feel that your experimental rationale lacks rigor. At the same time, it is advisable to conduct thorough literature research, ideally identifying several papers with highly relevant topics. Consider these as potential competitors to your paper and examine them for areas of improvement. Reflect on which aspects would captivate the community and accentuate them, while minimizing the inclusion of clichéd content. <br>如果你觉得实验论证还不够严谨，可能还需要补充实验。同时，建议开展充分的文献调研，最好找出几篇主题高度相关的论文。将它们视为你的论文的潜在竞争者，分析还有哪些可以改进的地方。思考哪些方面最能吸引学术共同体，并加以突出，同时尽量减少陈词滥调。

***Take-away: Around the contribution statements, conduct a solid analysis in the result section.***<br>***要点：围绕贡献陈述，在结果部分开展扎实的分析。***

Many readers will initially assess the method's effectiveness by examining the results before deciding to read the entire paper. They will look to see if your contribution aligns with the experimental findings. Even with strong confidence in your method's efficacy, you will likely need additional comparative and ablation experiments. It's important to create more tables and visuals, selecting the most significant aspects to present. Honesty and objectivity are crucial; overstating claims is particularly undesirable. If concerned about overclaiming, discussing with peers is advisable.<br>许多读者会先查看结果，初步判断方法是否有效，再决定是否阅读全文。他们会关注你声称的贡献是否与实验发现相符。即使你对方法的有效性很有信心，通常仍需要补充对比实验和消融实验。应多制作一些表格和可视化图，并挑选最重要的内容进行展示。诚实、客观至关重要，尤其应避免夸大论断。如果担心自己的表述言过其实，可以与同行讨论。

### Write an Introduction 撰写引言
With the above materials, you can start trying to write the introduction. Regarding the structure of the introduction, we directly quote from the textbook (from [Elena](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3178846/)):<br>有了上述材料，就可以开始尝试撰写引言。关于引言的结构，我们直接引用教材中的表述（引自 [Elena](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3178846/)）：

**Move 1. Establish a research territory**<br>**步骤 1. 确立研究领域**

a. Show that the general research area is important, central, interesting, and problematic in some way;<br>a. 说明这一总体研究领域为何重要、处于核心地位、富有趣味，以及在某些方面存在哪些问题；

**Move 2. Find a niche**<br>**步骤 2. 找到研究切入点**

a. Indicate a gap in the previous research, or extend previous knowledge in some way.<br>a. 指出以往研究中的空白，或从某个方面拓展已有知识。

**Move 3. Occupy the niche**<br>**步骤 3. 围绕切入点展开研究**

a. Outline purposes or state the nature of the present research;<br>a. 概述本研究的目的，或说明本研究的性质；

b. List research questions or hypotheses;<br>b. 列出研究问题或假设；

c. Announce principle findings;<br>c. 陈述主要发现；

d. State the value of the present research;<br>d. 说明本研究的价值；

e. Indicate the structure of the research paper.<br>e. 介绍论文的结构。

**Additional suggestions:**<br>**补充建议：**

a. Knuth: *Keep the reader upper-most in your mind;*<br>a. Knuth：*始终把读者放在心中最重要的位置；*

b. Cut to the chase and don't write too much irrelevant to the paper's topic. The novel and interesting aspects of the paper should appear as early as possible;<br>b. 开门见山，不要写太多与论文主题无关的内容。论文中新颖、有趣的部分应尽早出现；

c. Dedicate more space to describing original and novel ideas;<br>c. 用更多篇幅介绍原创且新颖的思想；

d. Respect the work of predecessors, and affirm historical contributions before pointing out shortcomings;<br>d. 尊重前人的工作，先肯定其历史贡献，再指出不足；

e. Consider using a "page one figure" to highlight the most important aspects of the paper and catch the reader's attention.<br>e. 可以考虑在论文首页放一张图，突出论文最重要的内容，吸引读者注意。

As we mentioned earlier, the main body is actually an extended version of the introduction. Typically, supplementing the introduction with additional experimental details forms the main body of the paper.<br>如前所述，正文实际上是引言的扩展版。通常，在引言的基础上补充更多实验细节，就构成了论文正文。

### Describe the Related Work 阐述相关工作
***Take-away: The mediocre approach is to describe the correct history, while the better approach is to focus on how different methods relate to what you do.***<br>***要点：平庸的写法是准确地叙述历史，更好的写法是着重说明不同方法与你的工作有何关联。***

The part may not be included in the context of the introduction. A paper typically has a separate section dedicated to discussing related work, including some background work and competing work. Find three or four topics that are most relevant to your paper, and outline the historical evolution under each topic. Do not list all the negative aspects of other techniques, but rather explain how you improve upon them. You can first write a literature review that is independent of your work. When classifying and ordering the previous methods (for example, refer to a certain method as a pioneer), it is important to pay attention to the correctness of discussion. If you are not confident enough, check the "related work" sections of the papers you referenced. Finally, rewrite this section from a more appropriate angle to reflect the unique aspects of your paper. <br>这一部分未必包含在引言中。论文通常会单设一节讨论相关工作，包括一些背景性工作和竞争性工作。找出与你的论文最相关的三四个主题，并梳理每个主题下的历史发展脉络。不要罗列其他技术的所有缺点，而应解释你如何在其基础上改进。你可以先写一份独立于自身工作的文献综述。在对以往方法进行分类和排序时（例如，将某个方法称为先驱），要注意论述的准确性。如果把握不足，可以查阅所引用论文的“相关工作”部分。最后，再从更合适的角度改写这一节，体现出你的论文的独特之处。

## Readability Improvement 提升可读性
> "Writing endures through the ages, its merits and faults known only to the author's heart. (文章千古事，得失寸心知）" —— [Du Fu](https://en.wikipedia.org/wiki/Du_Fu)<br>“文章千古事，得失寸心知。”—— [Du Fu](https://en.wikipedia.org/wiki/Du_Fu)

> "The best writing instruction ever: Good writing is bad writing rewritten. I got it from Stephen King. Where Stephen King got it, I don't know. I'm giving it to you. You tell your students." —— [Robert Weiss](https://robweiss.faculty.biostat.ucla.edu/writing_advice_2)<br>“我听过的最好的写作指导是：好文章都是差文章改出来的。这话是我从 Stephen King 那里学来的。Stephen King 又是从哪里学来的，我不知道。现在我把它告诉你，你再告诉你的学生。”—— [Robert Weiss](https://robweiss.faculty.biostat.ucla.edu/writing_advice_2)

***Take-away: The more prominent part, the more time you invest in it.***<br>***要点：越显眼的部分，越值得投入时间。***

Next, we will mainly discuss the polishing of the details. At present, AI assistants like [ChatGPT](https://chatgpt.com) and [Claude](https://www.anthropic.com/news/claude-3-5-sonnet) can easily help authors address the basic issues in English writing. We also recommend that authors in the Chinese region use [跃问](https://yuewen.cn/chats/new) or [豆包](https://www.doubao.com/chat/). You can have the AI generate multiple versions and choose the most suitable one. When utilizing these tools, remember that prioritize clarity over style.<br>接下来，我们主要讨论如何打磨细节。目前，[ChatGPT](https://chatgpt.com) 和 [Claude](https://www.anthropic.com/news/claude-3-5-sonnet) 等 AI 助手已经能够轻松帮助作者解决英语写作中的基础问题。我们也推荐中国地区的作者使用[跃问](https://yuewen.cn/chats/new)或[豆包](https://www.doubao.com/chat/)。你可以让 AI 生成多个版本，再选择最合适的一版。使用这些工具时，请记住：清晰比文采更重要。

Let's move on to discuss the issues that are not easy to handle automatically. We will measure the readability of papers using the following concepts: logical strength, defensibility, confusion time, and information density. Based on these concepts, some practical suggestions and techniques are described to improve the readability.<br>下面讨论不易自动处理的问题。我们将从逻辑强度、可辩护性、困惑时间和信息密度几个方面衡量论文的可读性，并据此介绍一些提升可读性的实用建议与技巧。

### Enhance Logical Strength 增强逻辑强度
***Take-away: Do not misuse or abuse connectives.***<br>***要点：不要误用或滥用连接词。***

In academic writing, logical coherence is more crucial than elegant vocabulary. Logical coherence is rooted in the logic itself, not in the connectives. We should view connectives as enhancements that smooth language, rather than using them to artificially construct sentence logic. Misalignment between connectives and actual logic can be confusing and greatly diminish readability. Here are a few specific examples:<br>在学术写作中，逻辑连贯比词汇优美更重要。逻辑连贯源于逻辑本身，而非连接词。我们应将连接词视为使语言更流畅的辅助，而不是用它们人为构造句子之间的逻辑关系。连接词与实际逻辑不符，会令人困惑，并大幅降低可读性。下面是几个具体例子：

> We argue that problem A is critical. To this end, we propose method B.<br>我们认为问题 A 至关重要。为此，我们提出了方法 B。

"To this end" refers to which end? In fact, the previous context only presents a viewpoint without specifying any actions or goals, so the use of this connective is inherently incorrect. Connectives must be grammatically correct.<br>“为此”究竟是为了什么？实际上，前文只提出了一个观点，并没有明确任何行动或目标，因此这里使用这个连接词本身就是错误的。连接词的使用必须符合语法。

> The system comprises three modules. First of all, Module A is .... Second, Module B is .... Last but not least, Module C is ....<br>该系统由三个模块组成。首先，模块 A 是……其次，模块 B 是……最后但同样重要的是，模块 C 是……

Here, several connectives impose a certain order on these three things that originally have no order relationship. We should not use connectives to create logical relationships. It would be better to introduce the three modules separately.<br>这里，几个连接词给原本没有顺序关系的三件事强加了某种顺序。我们不应使用连接词来制造逻辑关系，分别介绍这三个模块会更好。

### Consider Defensibility 考虑可辩护性
When we write, we should think about how readers might find fault with every sentence we write. If they believe something that seems wrong, they might doubt the whole paper. To enhance the paper's trustworthiness, we need to minimize the likelihood of being challenged.<br>写作时，我们应当思考读者可能会如何质疑笔下的每一句话。如果读者认定某处说法有误，就可能对整篇论文产生怀疑。为了增强论文的可信度，我们需要尽量减少可能受到质疑的地方。

***Take-away: Make statements based on references and facts.***<br>***要点：以参考文献和事实为依据作出陈述。***

When we write "Problem A is a pain point in this field and has not been solved yet," we should consider that the reader may ask, "Why is this a pain point? How serious are the consequences? Does this consequence have a significant impact on the final performance?" This requires the addition of appropriate references.<br>当我们写下“问题 A 是本领域尚未解决的痛点”时，应考虑到读者可能会问：“为什么这是一个痛点？后果有多严重？这些后果会显著影响最终性能吗？”这就需要补充适当的参考文献。

> It is reported that problem A results in ... [1,2,3] and ... [4,5], which are critical to ... because ... [6, 7, 8].<br>据报道，问题 A 会导致……[1,2,3] 和……[4,5]；这些对……至关重要，因为……[6, 7, 8]。

When discussing the results of a paper, it is even more necessary to be rigorous:<br>讨论论文结果时，更需要严谨：

> The performance improves, which is attributed to the fact that XXX...<br>性能有所提升，这是因为 XXX……

The evidence should be presented prominently;<br>应当在显眼的位置给出证据；

> The improvement may be explained by the fact that XXX...<br>这一提升可能是因为 XXX……

Some indirect evidence such as visualizations can be shown.<br>可以展示可视化结果等间接证据。

Be as objective as possible and avoid exaggerating.<br>尽可能保持客观，避免夸大。

### Shorten Confusion Time 缩短困惑时间
"Confusion time" is the sum of the time readers spend on each "hmm, what's this?" to "oh, I get it" moment during the reading process. The shorter the total confusion time of a paper, the higher the readability, and the more peaceful the reader will be.<br>“困惑时间”是读者在阅读过程中，每次从“嗯，这是什么？”到“哦，我明白了”所花费时间的总和。一篇论文的总困惑时间越短，可读性就越高，读者的心态也就越平和。

***Take-away: Explain a concept as close as possible when it is proposed.***<br>***要点：在尽量靠近概念首次提出的位置解释它。***

It is recommended to directly explain the essence of a component after giving its name; for example, "We propose XXX, which is implemented with a two-layer multilayer perceptron (MLP)." If a concept is not easy to explain, it can be supplemented by referring to literature.<br>建议在给出一个组件的名称后，直接解释其本质。例如：“我们提出了 XXX，它由一个两层多层感知机（MLP）实现。”如果一个概念不容易解释，可以通过引用文献加以补充。

***Take-away: Resolve relative pronoun ambiguity.***<br>***要点：消除关系代词的指代歧义。***

If it is not possible to make a long sentence completely unambiguous, it should be broken down into short sentences. A large proportion of the readership is not native speakers, and fancy sentence structures do not earn extra points.<br>如果无法让一个长句完全没有歧义，就应将它拆成短句。相当一部分读者并非以英语为母语，花哨的句式不会带来额外加分。

***Take-away: Frequently use topic sentences, preferably at the beginning of paragraphs.***<br>***要点：多用主题句，最好放在段落开头。***

The reader may not be able to quickly understand all the details, at which point the main information can be quickly obtained by the reader through the topic sentences, to avoid affecting the overall reading experience.<br>读者未必能迅速理解所有细节，此时可以通过主题句快速获取主要信息，避免影响整体阅读体验。

### Increase Information Density 提高信息密度
"Information density" refers to the efficiency with which text provides effective information to readers. Low information density may cause readers to lose focus and question the expertise.<br>“信息密度”是指文字向读者传达有效信息的效率。信息密度低，可能使读者注意力涣散，并对作者的专业性产生怀疑。

***Take-away: Get to the point as soon as possible.***<br>***要点：尽快切入主题。***

The beginning of each section may talk about the history. Try not to be lengthy. "Do not write irrelevant content, nor should you write about things that most readers are already familiar with." Discussing the development of human writing skills, would certainly deter the vast majority of our readers.<br>每一节的开头可能需要介绍历史背景，但应尽量避免冗长。“不要写无关的内容，也不要写大多数读者早已熟悉的内容。”如果本文开始讨论人类写作能力的发展史，肯定会劝退绝大多数读者。

***Take-away: Both text and charts should be appropriately detailed or concise.***<br>***要点：文字和图表都应详略得当。***

Use an appropriate layout that balances text and visuals. Avoid common pitfalls like featuring a large chart with only a few key points highlighted. Or a very long passage describing the experimental details and hyper-parameters, which should really be placed in the appendix.<br>采用合适的版式，平衡文字与图表。避免常见的问题，例如放一张很大的图，却只突出少数几个要点；或用很长的篇幅描述实验细节和超参数，而这些内容其实应放在附录中。

***Take-away: Important explanations and elucidations should be as close to the charts as possible.***<br>***要点：重要的解释和说明应尽量靠近图表。***

The ideal situation is that each chart can be understood independently of the main text. In the caption, try to clearly state the theme and key conclusions. If there are abbreviations in the chart, it is best to have an explanation. <br>理想情况下，每张图表都应能脱离正文而被独立理解。图表说明应尽量清楚地交代主题和关键结论。如果图表中有缩写，最好予以解释。

If you want to emphasize a certain result in Table 5, it is best for the sentence analyzing that result to be on the same page as Table 5, and it is best to have the words "Table 5" before and after that sentence. This is because readers may not carefully read the text you write, but first look at the charts and then look for text related to the content of the charts. When they see a striking result in Table 5 and become curious, they may use the search function in the PDF reader to search for "Table 5". <br>如果你想强调表 5 中的某个结果，分析该结果的句子最好与表 5 放在同一页，而且最好在该句前后出现“表 5”字样。这是因为读者未必会仔细阅读你写的文字，而可能先看图表，再寻找与图表内容相关的文字。当他们看到表 5 中某个醒目的结果并产生好奇时，可能会使用 PDF 阅读器的搜索功能搜索“Table 5”。

Do not expect readers to figure out for themselves from a complex table who should be compared with whom to draw conclusions. We should put the content we want to compare. If such a table is difficult to design, it is worth repeating a certain result (usually a baseline that needs to be compared with several groups of results) several times, even if it means sacrificing the elegance. No one will reject your paper because the tables are not elegant, but it is very annoying if the table is not clear.<br>不要指望读者自行从复杂的表格中弄清楚，应该比较哪些结果才能得出结论。我们应当把希望读者比较的内容放在一起。如果这样的表格难以设计，即使要牺牲美观，也值得将某个结果重复列出几次（通常是需要与多组结果进行比较的基线）。没有人会因为表格不够优雅而拒绝你的论文，但表格不清楚确实很令人困扰。

### Detail Checklist 细节检查清单
First and foremost, avoid making mistakes. Prioritize the rigor of the paper before considering its aesthetics. The following is a checklist that can help authors improve their writing:<br>首先要避免犯错。应先确保论文的严谨性，再考虑美观。下面的检查清单可以帮助作者改进写作：

- [ ] Go through the charts to ensure the story is complete. Strive to improve the quality of the charts and make them self-explanatory.<br>逐一检查图表，确保研究叙事完整。努力提高图表质量，使其不依赖正文也能被理解。
- [ ] Check for any inconsistencies in symbols, abbreviations, and references.<br>检查符号、缩写和参考文献是否存在不一致。
- [ ] Whether the level of detail in the text and charts is appropriate?<br>文字和图表的详略是否得当？
- [ ] Place important information in prominent positions.<br>将重要信息放在显眼的位置。
- [ ] Can the text and legends in the figure be larger?<br>图中的文字和图例能否再大一些？
- [ ] Can the understanding speed of tables be improved by using methods such as column division, bolding text, and deleting redundancy?<br>能否通过分列、加粗文字、删除冗余内容等方式，让读者更快理解表格？
- [ ] Can the reproducibility be improved? For example, by providing details and key code in the appendix.<br>能否提高可复现性？例如，在附录中提供细节和关键代码。

We will list more minor items in the [Appendix](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#appendix).<br>我们将在[附录](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#appendix)中列出更多细节检查项。
## Conclusion 结语
***Take-away: Good luck!***<br>***要点：祝你好运！***

As this manuscript stands without the benefit of peer review, it undoubtedly contains numerous imperfections. The concepts presented herein are primarily derived from widely shared community knowledge, which we have endeavored to synthesize and simplify for the benefit of newcomers to the community. Our goal is to provide a concise yet comprehensive guide that can ease the learning curve for those embarking on the journey of writing AI conference papers. If this document serves as a beacon of clarity and direction for any reader, we would consider our efforts successful. *Leaving a star will be a great encouragement to us.*<br>本文尚未经过同行评审，无疑还存在许多不足。文中观点主要来自学术共同体广泛共享的知识，我们尝试对其进行梳理和简化，以帮助刚刚加入这一共同体的新手。我们的目标是提供一份简明而全面的指南，帮助初次撰写 AI 会议论文的作者降低入门难度。如果本文能为任何一位读者理清思路、指明方向，我们便认为这些努力是值得的。*点一颗星将是对我们莫大的鼓励。*

## Appendix 附录
In the Appendix, several topics are covered:<br>附录涵盖以下几个主题：

[Checklist for Last Few Hours](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#checklist-for-last-few-hours): It provides a checklist to ensure the paper is in order before submission.<br>[最后几小时的检查清单](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#checklist-for-last-few-hours)：提供一份检查清单，确保论文在提交前各方面准备妥当。

[AI Paper Production and Publication](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#ai-paper-production-and-publication): It outlines the process of paper submission, review, and publication in AI conferences.<br>[AI 论文的撰写与发表](https://github.com/hzwer/WritingAIPaper?tab=readme-ov-file#ai-paper-production-and-publication)：概述 AI 会议论文的投稿、评审与发表流程。

[Common Negative Review Comments](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#common-negative-review-comments): It lists common criticisms reviewers might have and suggestions for revision.<br>[常见的负面评审意见](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#common-negative-review-comments)：列出评审人可能提出的常见批评，以及相应的修改建议。

[If the Paper Is Not Accepted](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#if-the-paper-is-not-accepted): It offers advice on dealing with rejection and improving the paper for future submissions.<br>[如果论文未被录用](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#if-the-paper-is-not-accepted)：介绍如何应对拒稿，以及如何改进论文以便再次投稿。

[AI Conference List](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#ai-conference-list): Some information of notable AI conferences that you might find useful.<br>[AI 会议列表](https://github.com/hzwer/WritingAIPaper/tree/main?tab=readme-ov-file#ai-conference-list)：提供一些知名 AI 会议的信息，供你参考。

### Checklist for the Last Few Hours 最后几小时的检查清单
- [ ] Check that various numbers are not copied incorrectly.<br>检查各类数字是否抄写有误。
- [ ] Search for question marks to check for latex errors.<br>搜索问号，检查是否存在 LaTeX 错误。
- [ ] Make sure that all charts are mentioned in the main text and that the order of mentions matches the order in which the charts appear.<br>确保正文提及了所有图表，且提及顺序与图表的出现顺序一致。
- [ ] The caption is very noticeable. Avoid grammatical errors, and it is recommended to use a period at the end.<br>图表说明十分显眼，应避免语法错误，并建议在末尾加句号。
- [ ] Vectorize the charts. <br>将图表转为矢量格式。
- [ ] Check that all formulas are complete, they are easily overlooked in the editing process.<br>检查所有公式是否完整；编辑过程中很容易忽略它们。
- [ ] Go through all the subtitles and unify the capitalization style.<br>通读所有小标题，统一大小写风格。
- [ ] Confirm that there are no figures outside the main body pages.<br>确认没有图片落在正文页范围之外。
- [ ] Check for anonymity. You may need to delete acknowledgments. If you have submitted code or a demo, you must also pay great attention to anonymity.<br>检查匿名性。可能需要删除致谢。如果提交了代码或演示，也必须格外注意匿名性。
- [ ] **Ensure the number of pages is correct to avoid being desk rejected.**<br>**确保页数符合要求，避免被直接拒稿。**

### AI Paper Production and Publication AI 论文的撰写与发表

This section mainly introduces the process of producing papers and the review process. A conference paper usually runs about eight pages in a two-column layout, or over ten pages in a single-column layout, based on the conference's specifications. Authors prepare and submit their paper along with supplementary materials like code and demo videos by the given deadline.<br>本节主要介绍论文的撰写流程和评审流程。根据会议的具体要求，会议论文通常采用约八页的双栏排版，或十多页的单栏排版。作者需要在规定的截稿期前，准备并提交论文，以及代码、演示视频等补充材料。

Provided there are no critical oversights, such as neglecting to anonymize the submission, substantial formatting issues, or surpassing the page limit — any of which could result in an immediate rejection (known as a "desk reject") — the paper proceeds to the review phase. Following approximately two months, authors receive feedback from typically three reviewers in the form of comments and an overall score for their paper. Many of these reviewers have published work in related domains and might be cited in the submitted paper. With the initial review outcomes, authors must craft a brief rebuttal, generally one page, to address queries or provide additional findings. Roughly half of the papers are withdrawn during this rebuttal phase. Reviewers then deliberate for a week or two (commonly on a private platform) based on the rebuttal, indicating whether their concerns have been alleviated and discussing the paper's merits. Usually, reviewers align on a positive or negative stance, though occasionally, the area chair decides.<br>如果没有重大疏漏，例如未对稿件进行匿名处理、存在严重格式问题或超过页数限制——这些问题都可能导致直接拒稿——论文就会进入评审阶段。大约两个月后，作者通常会收到三位评审人的反馈，包括评审意见和论文的总体评分。这些评审人中有不少在相关领域发表过论文，他们的工作也可能被投稿论文引用。收到初步评审结果后，作者需要撰写一份简短的答辩，通常为一页，用于回应问题或提供补充结果。约有一半的论文会在这一答辩阶段被撤回。随后，评审人会根据答辩展开一到两周的讨论（通常在非公开平台上进行），说明自己的疑虑是否已被消除，并讨论论文的优点。通常，评审人会形成肯定或否定的一致意见，但偶尔也会由领域主席作出决定。

The final acceptance outcome necessitates waiting for approximately another month, after which it will be revealed via the email system. Typically, acceptance rates range from one-sixth to one-quarter of submitted manuscripts. Authors then revise their work based on reviewer feedback before submitting the final, camera-ready version for publication. The majority of papers, however, face rejection and are returned to the authors. These authors may opt to resubmit following the previously mentioned process or decide to discontinue work on the paper. It is worth noting that most papers undergo an extensive period of refinement and revision, colloquially dubbed the "Fibonacci Submission Approach." (Recommendation: [a Chinese lecture by Boxin Shi](https://hub.baai.ac.cn/view/8659)).<br>最终录用结果通常还需要再等待约一个月，之后会通过邮件系统公布。一般而言，录用的稿件约占投稿总数的六分之一到四分之一。作者随后根据评审意见修改论文，再提交用于发表的终稿。然而，大多数论文会遭到拒绝并退回作者。作者可以选择按前述流程再次投稿，也可以决定不再继续这篇论文。需要注意的是，大多数论文都经历了漫长的打磨和修改过程，俗称“斐波那契投稿法”。（推荐：[Boxin Shi 的中文讲座](https://hub.baai.ac.cn/view/8659)。）

### Common Negative Review Comments 常见的负面评审意见
We have listed some common negative reviews and suggested revisions (in italics).<br>我们列出了一些常见的负面评审意见及修改建议（以斜体标注）。

- Criticizing the author for being unprofessional: Important references are missing; the paper structure is messy, and some essential elements are lacking, such as not submitting supplementary video results for a video-related study; the experimental setup is significantly different from previous work. <br>批评作者不够专业：遗漏重要参考文献；论文结构混乱，缺少某些必要内容，例如视频相关研究没有提交补充视频结果；实验设置与以往工作存在显著差异。

*Refer to the reference list of recent papers to fill in the gaps, and the configuration should be aligned.*<br>*参考近期论文的参考文献列表，补齐遗漏文献，并对齐实验配置。*

- Questioning the validity: The reported results do not conform to common sense and are not credible; exaggerating one's own achievements or making some obviously incorrect assertions; there are flaws in the experimental setup or argumentation. <br>质疑有效性：报告的结果不符合常识，缺乏可信度；夸大自身成果，或作出某些明显错误的断言；实验设置或论证存在缺陷。

*Conduct more experiments, refine the expression, and strive for rigor.*<br>*补充实验，打磨表述，力求严谨。*

- Not respecting previous work: Not citing the latest results, conducting low-benchmark experiments; excessively demeaning the work of predecessors; confusing one's own work with the contributions of predecessors. <br>不尊重以往工作：未引用最新成果，实验采用的比较基准偏低；过度贬低前人的工作；混淆自己的工作与前人的贡献。

*Compare more with existing work tables, conduct more paper research, and if you say others have done a poor job, provide evidence.*<br>*多与已有工作的结果表进行对照，开展更多文献调研；如果认为别人做得不好，就要提供证据。*

- Lack of novelty: The story is not well written, the logic is not clear, or most of it is known knowledge; feeling that the work is incremental and does not contribute much. In other words, the effect is not impressive.<br>缺乏新颖性：研究叙事不佳，逻辑不清，或大部分内容都是已有知识；让人觉得工作只是增量改进，贡献有限。换言之，效果不够突出。

*Discuss with some peers, and highlight the strengths.*<br>*与同行讨论，突出工作的优势。*

- Poor paper presentation quality: Many grammatical errors, poor writing, poor English level; difficult to understand, lacking some details. <br>论文呈现质量差：语法错误多，写作质量差，英语水平欠佳；难以理解，缺少一些细节。

*Use AI tools or [Grammarly](https://www.grammarly.com) to revise, and ask friends for help to read.*<br>*使用 AI 工具或 [Grammarly](https://www.grammarly.com) 修改，并请朋友帮忙通读。*

- Disagreement on the approach: Not approving of the experimental design or not believing in this technical route.<br>不认同研究思路：不认可实验设计，或不相信这条技术路线。

*Conduct more experiments or cite similar expressions in relevant literature to support your argument, and try to win over other reviewers.*<br>*补充实验，或引用相关文献中的类似表述来支持论点，并尝试争取其他评审人的支持。*

### If the Paper is Not Accepted 如果论文未被录用
> Review process is highly random. But there is one golden rule that withstands the test of time and randomness - **badly written papers get bad reviews. Period.** It doesn’t matter if the idea is good, result is good, citations are good. Not at all. Writing is critical — and this is ironic because engineers are the worst-trained writers among all disciplines in a university. You need to discipline yourself: leave time for writing, think deeply about writing, and write it over and over again till it’s as polished as you can think of. (Fei-Fei Li)<br>评审过程具有很强的随机性。但有一条金科玉律经得起时间和随机性的考验——**写得差的论文会得到差评。就是这样。** 无论想法多好、结果多好、引用多好，都无济于事。写作至关重要；讽刺的是，在大学各学科中，工程师恰恰是最缺乏写作训练的群体。你需要严格要求自己：为写作留出时间，深入思考如何写作，反复重写，直到打磨至你所能想到的最好状态。（Fei-Fei Li）

There are many papers that stayed on arXiv after being rejected and now have a huge impact [1](https://arxiv.org/abs/1503.02531);[2](https://arxiv.org/abs/1907.11692);[3](https://arxiv.org/abs/1704.04861);[4](https://arxiv.org/abs/1606.06160). [Many great works have been rejected and even got extremely negative comments.](https://www.reddit.com/r/MachineLearning/comments/vywfx3/d_are_there_any_rejected_papers_that_ended_up/) The review process is especially painful for novices, who may be putting all their eggs in one basket. The paper will be significantly improved throughout the process. If this process helps you produce a truly good paper, you can benefit from and be proud of it for many years to come. Remember, the paper is only the initial step or a small part of the overall work.<br>许多论文被拒后留在 arXiv 上，如今却产生了巨大影响 [1](https://arxiv.org/abs/1503.02531);[2](https://arxiv.org/abs/1907.11692);[3](https://arxiv.org/abs/1704.04861);[4](https://arxiv.org/abs/1606.06160)。[许多伟大的工作都曾被拒，甚至收到过极为负面的评价。](https://www.reddit.com/r/MachineLearning/comments/vywfx3/d_are_there_any_rejected_papers_that_ended_up/) 对新手而言，评审过程尤其痛苦，因为他们可能把全部希望都寄托在这一篇论文上。但在整个过程中，论文也会得到显著改进。如果这个过程帮助你写出一篇真正优秀的论文，你将在未来多年受益于它，并为之自豪。请记住，论文本身只是整个工作的起点，或其中的一小部分。

### AI Conference List AI 会议列表
The schedule can usually be found on [AI Conference Deadlines](https://aideadlin.es/?sub=CV,ML,NLP). The acceptance rate can be found on [Conference-Acceptance-Rate](https://github.com/lixin4ever/Conference-Acceptance-Rate).<br>会议日程通常可以在 [AI 会议截稿期](https://aideadlin.es/?sub=CV,ML,NLP)网站上查到。录用率可以在[会议录用率汇总](https://github.com/lixin4ever/Conference-Acceptance-Rate)中查到。

Note: Acceptance rates and submission dates vary. Always check the official conference website for the most current information.<br>注意：录用率和投稿日期会有所变化。请务必查看会议官方网站，以获取最新信息。

| Conference Name 会议名称 | Typical Submission Month 通常投稿月份 | Recent Acceptance Rate 近期录用率 |
| --- | --- | --- |
| IJCAI | January 一月 | ~14% |
| ICML | January 一月 | ~27% |
| ICCV/ECCV | March 三月 | ~27% |
| BMVC | April 四月 | ~26% |
| ACMMM | April 四月 | ~26% |
| NeurIPS | May 五月 | ~26% |
| EMNLP | May 五月 | ~23% |
| WACV | June and August 六月和八月 | ~45% |
| ACCV | July 七月 | ~33% |
| AAAI | July 七月 | ~24% |
| ICASSP | September 九月 | ~45% |
| ICLR | September 九月 | ~31% |
| NAACL | September 九月 | ~23% |
| ICRA | September 九月 | ~45% |
| AISTATS | October 十月 | ~28% |
| CVPR | November 十一月 | ~24% |
| ACL | Rolling Review 滚动评审 | ~23% |
