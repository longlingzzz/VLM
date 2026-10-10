# start 全库调研：CVPR 2026 扩展清单

更新：2026-09-27。回到[总报告](start全库调研-2026-09-27.md)。

## 1. 范围与证据等级

`start/01 C3` 引用外部 [cvpr2026-clip-papers.md](/Users/longlingzzz/CVLearning/docs/learning/research/cvpr2026-clip-papers.md)。本次展开其 35 个 CLIP 条目和 10 个微调条目，共 45 行；不是把历史清单当作会议全集，也不保证原分类正确。另登记历史“16 篇长尾”中点名的 6 篇，以及 4 篇相邻工作。

【本次已核实｜清单检查】外部清单确有这 45 个具名条目。其“标题含 CLIP 共 34 篇、排除 4 篇后 35 篇”的算术和筛选口径不自洽。历史“4042 篇中仅 16 篇长尾、零篇严格竞品”的结论缺可重跑检索记录，不能作为已确认的研究空白。

**本页主要是书目、摘要和研究关系调研，不是 55 篇消融精读。** “原始摘要”表示取得作者预印本摘要；“官方摘要/论文片段”主要来自原始出处的搜索索引，证据等级为【搜索级】；“作者仓库”只支持作者所述身份和方法概要。TANGO 仅核补充算法 1，CHIPS 沿用上一轮 S05。CVF 页面直接读取多次返回 403，不能用已有链接声称全文已读。ReAttnCLIP 单列待确认。

## 2. 45 个具名条目的逐项调研

下表“关系与边界”为基于所读材料的【研究判断】；没有长尾受控实验的条目只作邻近机制来源。会议入口来自旧清单；另有原始来源时同时列出。

| ID | 论文与原始入口 | 核查层级 | 主要内容 | 研究关系与边界 |
|---|---|---|---|---|
| C01 | [MoECLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Park_MoECLIP_Patch-Specialized_Experts_for_Zero-shot_Anomaly_Detection_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.03101) | 原始摘要 | 面向零样本异常检测，以图像块路由至专门专家。 | 可借局部证据与适配器设计；异常检测的正常/异常不等于类别频率长尾。 |
| C02 | [IsoCLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Magistri_IsoCLIP_Decomposing_CLIP_Projectors_for_Efficient_Intra-modal_Alignment_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.19862) | 原始摘要 | 分解 CLIP 投影器以改善模态内对齐。 | 与 C27 的反方结论一起阅读；不能由几何对齐直接推出尾类收益。 |
| C03 | [Reconstructing CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Liu_Reconstructing_CLIP_for_Open-Vocabulary_Dense_Perception_CVPR_2026_paper.html) | 官方摘要片段 | 面向开放词汇稠密感知重构 CLIP 表示。 | 局部图文对齐邻近；尚未核其尾类数据或逐图属性实验。 |
| C04 | [ReAttnCLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Niu_ReAttnCLIP_Training-Free_Open-Vocabulary_Remote_Sensing_Image_Segmentation_via_Re-defined_Attention_in_CLIP_CVPR_2026_paper.html) | 待确认 | 历史清单称以重定义注意力实现免训练遥感分割。 | 所给会议页访问受阻，独立检索尚未闭合身份；本行方法只保留为交接记录。 |
| C05 | [SynCLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Xie_SynCLIP_Synonym-Coherent_Language-Image_Pretraining_for_Robust_Open-Vocabulary_Dense_Perception_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2607.11008) | 原始摘要 | 以同义表达的一致性改进开放词汇稠密感知，包含空间注意一致性与表征约束。 | 可控制同一属性的改写鲁棒性；同义一致不等于属性在图中为真。 |
| C06 | [PowerCLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Kawamura_PowerCLIP_Powerset_Alignment_for_Contrastive_Pre-Training_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2511.23170) | 原始摘要 | 对区域与短语的组合进行幂集对齐，增强组合表示。 | 可借细粒度属性组合；需另验证长尾与证据覆盖。 |
| C07 | [Role-SynthCLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Huangfu_Role-SynthCLIP_A_Role-Play_Driven_Diverse_Synthetic_Data_Approach_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2511.05057) | 原始摘要 | 以角色扮演生成多样描述，在图文训练中增加文字视角。 | 同图多描述不能作为新增独立视觉样本，适合文字增量对照。 |
| C08 | [FB-CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Hu_FB-CLIP_Fine-Grained_Zero-Shot_Anomaly_Detection_with_Foreground-Background_Disentanglement_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.19608) | 原始摘要 | 通过前景/背景解耦改进细粒度零样本异常检测。 | 可借前景支持与背景捷径诊断，任务与类别长尾有别。 |
| C09 | [Guiding Diffusion-based Reconstruction with Contrastive Signals](https://openaccess.thecvf.com/content/CVPR2026/html/Han_Guiding_Diffusion-based_Reconstruction_with_Contrastive_Signals_for_Balanced_Visual_Representation_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.04803) | 原始摘要 | 以对比信号指导扩散重建，平衡判别性和细节保留。 | 题名 Balanced 指表示目标的平衡，不能读成类别频率平衡。 |
| C10 | [Concept Regions Matter](https://openaccess.thecvf.com/content/CVPR2026/html/Agarwal_Concept_Regions_Matter_Benchmarking_CLIP_with_a_New_Cluster-Importance_Approach_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2511.12978) | 原始摘要 | 以区域聚类重要性分析 CLIP，并构造前景/背景变化的 COVAR 评测。 | 可启发属性区域干预；预测重要性不是独立视觉事实标注。 |
| C11 | [Explaining CLIP Zero-shot Predictions Through Concepts](https://openaccess.thecvf.com/content/CVPR2026/html/Ozdemir_Explaining_CLIP_Zero-shot_Predictions_Through_Concepts_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.28211) | 原始摘要 | 通过语言对齐的概念投影解释 CLIP 零样本预测。 | 适合作诊断候选；概念激活不能直接用作可见性真值。 |
| C12 | [CLIP Is Shortsighted](https://openaccess.thecvf.com/content/CVPR2026/html/Lavoie_CLIP_Is_Shortsighted_Paying_Attention_Beyond_the_First_Sentence_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2602.22419) | 原始摘要 | 研究首句捷径及长描述利用不足，通过描述构造和句子采样处理。 | 文本长度、属性位置必须纳入控制；不是长尾类别实验。 |
| C13 | [Ultrasound-CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Jin_Ultrasound-CLIP_Semantic-Aware_Contrastive_Pre-training_for_Ultrasound_Image-Text_Understanding_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2604.01749) | 原始摘要 | 用超声领域层级语义体系和结构化文本改进对比预训练。 | 文本知识结构化来源；领域知识丰富不等于逐图有证据。 |
| C14 | [WikiCLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Ning_WikiCLIP_An_Efficient_Contrastive_Baseline_for_Open-domain_Visual_Entity_Recognition_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.09921) | 原始摘要 | 面向开放域实体识别，将语言知识与视觉引导的知识适配相结合。 | 与类别知识注入直接相邻；需单独控制知识正确性和可见性。 |
| C15 | [b-CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Zohra_b-CLIP_Text-Conditioned_Contrastive_Learning_for_Multi-Granular_Vision-Language_Alignment_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2512.12678) | 原始摘要 | β-CLIP 使用多粒度文字与文本条件化图像聚合进行对齐。 | 旧 b-CLIP 是题名转写，勿重复计数；细粒度对齐不自动解决尾类缺图。 |
| C16 | [EthoCLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Jing_EthoCLIP_Ontology-Enhanced_Video-Language_Pretraining_for_Animal_Behavior_Understanding_CVPR_2026_paper.html) | 官方论文首页 | 本体增强的视频语言预训练，用于动物行为理解。 | 目前只到题名/首页证据，未核具体损失与消融；行为本体可作邻近知识组织来源。 |
| C17 | [CHIPS](https://openaccess.thecvf.com/content/CVPR2026/html/Zhuang_CHIPS_Efficient_CLIP_Adaptation_via_Curvature-aware_Hybrid_Influence-based_Data_Selection_CVPR_2026_paper.html) | 既有原文核查 | 曲率感知的混合影响分数用于 CLIP 数据选择。 | 见 start 补充 S05；医学收益伴随部分通用指标回落，不能称全面无损。 |
| C18 | [Boosting Visual Reprogramming for CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Wu_Boosting_Visual_Reprogramming_for_CLIP_with_Dual_Granularity_Alignment_CVPR_2026_paper.html)；[本次来源](https://github.com/iLearn-Lab/CVPR26-DGA) | 作者仓库 | 以双粒度对齐增强 CLIP 视觉重编程。 | 方法归入输入/提示适配对照；作者仓库不替代消融表。 |
| C19 | [Subspace Alignment for CLIP-based Continual Learning](https://openaccess.thecvf.com/content/CVPR2026/html/Zhang_Subspace_Alignment_for_CLIP-based_Continual_Learning_via_Canonical_Correlation_Analysis_CVPR_2026_paper.html) | 官方摘要片段 | 以典型相关分析处理 CLIP 持续学习的子空间对齐。 | 研究跨任务漂移；持续学习遗忘与类别频率偏差分开。 |
| C20 | [Alert-CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Zhu_Alert-CLIP_Abnormality-aware_Latent-Enhanced_Representation_Tuning_of_CLIP_for_Video_Anomaly_CVPR_2026_paper.html) | 官方摘要片段 | 面向视频异常检测，进行异常感知的潜在表示调整及多层次对齐。 | 局部事件证据邻近；不沿用异常任务数字为长尾识别数字。 |
| C21 | [GS-CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Deng_GS-CLIP_Zero-shot_3D_Anomaly_Detection_by_Geometry-Aware_Prompt_and_Synergistic_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2602.19206) | 原始摘要 | 结合三维几何提示与多个二维视角进行零样本三维异常检测。 | 零样本任务协议不等于整个方法没有训练或外部数据成本。 |
| C22 | [DLVP-CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Zhang_DLVP-CLIP_Enhancing_Fine-Grained_Zero-Shot_Anomaly_Detection_via_Dynamic_Local_Visual_CVPR_2026_paper.html) | 官方论文片段 | 通过动态局部视觉提示改善细粒度异常检测。 | 有助于设计局部提示对照；尚无本次核实的长尾消融。 |
| C23 | [Beyond Text](https://openaccess.thecvf.com/content/CVPR2026/html/Qiu_Beyond_Text_Visual_Description_Assembly_by_Probabilistic_Model_for_CLIP-based_CVPR_2026_paper.html) | 官方论文片段 | 用概率模型组装视觉描述，服务于 CLIP 弱监督语义分割。 | 区域与类别语义匹配近邻；分割监督口径须另行核对。 |
| C24 | [MedCLIPSeg](https://openaccess.thecvf.com/content/CVPR2026/html/Koleilat_MedCLIPSeg_Probabilistic_Vision-Language_Adaptation_for_Data-Efficient_and_Generalizable_Medical_Image_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2602.20423) | 原始摘要 | 以概率视觉语言适配提高医学图像分割的数据效率与泛化。 | 可借不确定性与少数据适配思路；不能仅凭 VLM 一词归为生成式多模态大模型。 |
| C25 | [Looking Beyond the Window](https://openaccess.thecvf.com/content/CVPR2026/html/Lee_Looking_Beyond_the_Window_Global-Local_Aligned_CLIP_for_Training-free_Open-Vocabulary_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.23030) | 原始摘要 | 以全局—局部对齐处理免训练开放词汇分割的窗口上下文问题。 | 可借裁剪后证据变化诊断；需计多窗口推理成本。 |
| C26 | [Leveraging Class Distributions in CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Yang_Leveraging_Class_Distributions_in_CLIP_for_Weakly_Supervised_Semantic_Segmentation_CVPR_2026_paper.html) | 官方摘要片段 | 利用图像块的类别分布及分布间关系改进弱监督分割。 | 这里 class distributions 不等于数据集的类别频次先验；不能当作长尾重平衡。 |
| C27 | [Reevaluating the Intra-Modal Misalignment Hypothesis in CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Herzog_Reevaluating_the_Intra-Modal_Misalignment_Hypothesis_in_CLIP_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.16100) | 原始摘要 | 重新检验 CLIP 模态内失配假说，强调任务歧义等评测因素。 | 是 C02 的必要反方；对齐是否有效需在同任务同协议下检验。 |
| C28 | [From Weights to Concepts](https://openaccess.thecvf.com/content/CVPR2026/html/Gentile_From_Weights_to_Concepts_Data-Free_Interpretability_of_CLIP_via_Singular_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.24653) | 原始摘要 | 用权重的奇异值分解实现无数据的概念解释。 | 无需解释数据不等于解释具有因果性或能判定逐图支持。 |
| C29 | [CLIP-like Model as a Foundational Density Ratio Estimator](https://openaccess.thecvf.com/content/CVPR2026/html/Uchiyama_CLIP-like_Model_as_a_Foundational_Density_Ratio_Estimator_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2506.22881) | 原始摘要 | 将 CLIP 类模型置于密度比估计框架，连接联合与边际分布。 | 可作数据选择理论来源；相似度不自动是校准后的类别概率。 |
| C30 | [When CLIP Sees More, It Fights Back Harder](https://openaccess.thecvf.com/content/CVPR2026/html/Kim_When_CLIP_Sees_More_It_Fights_Back_Harder_Multi-View_Guided_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2606.06938) | 原始摘要 | 多视角引导测试时自适应反攻击，提升对抗鲁棒性。 | 属于测试时计算；须与训练节省分账。 |
| C31 | [CLIPoint3D](https://openaccess.thecvf.com/content/CVPR2026/html/Singha_CLIPoint3D_Language-Grounded_Few-Shot_Unsupervised_3D_Point_Cloud_Domain_Adaptation_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2602.20409) | 原始摘要 | 语言引导的少样本无监督三维点云域适配。 | 少样本、域偏移和类别长尾是不同变量。 |
| C32 | [FluoCLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Park_FluoCLIP_Stain-Aware_Focus_Quality_Assessment_in_Fluorescence_Microscopy_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2602.23791) | 原始摘要 | 染色感知的荧光显微图像聚焦质量评估。 | 可提供视觉质量因素线索，不属于直接长尾识别竞品。 |
| C33 | [DINO Eats CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/He_DINO_Eats_CLIP_Adapting_Beyond_Knowns_for_Open-set_3D_Object_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2604.19432) | 原始摘要 | 以 DINO 为视觉表示基础，结合 CLIP 语义知识进行开放集三维检索。 | 反对无条件假定 CLIP 最适合所有视觉任务；不证明当前尾类任务应换底座。 |
| C34 | [VRCLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Zhang_VRCLIP_Multimodal_Canonical_Correlation_Alignment_for_CLIP-Driven_Vision-Radio_Person_Re-Identification_CVPR_2026_paper.html) | 官方摘要片段 | 对齐视觉与无线电表征，用于人员重识别。 | 核心任务涉及无线电模态，不能和普通图文分类直接横比。 |
| C35 | [PPM-CLIP](https://openaccess.thecvf.com/content/CVPR2026/html/Wang_PPM-CLIP_Probabilistic_Prompt_Modeling_for_Generalizable_AI-Generated_Image_Detection_CVPR_2026_paper.html) | 官方摘要片段 | 概率提示建模用于可泛化的人工智能生成图像检测。 | 提示分布建模近邻；真假二分类不等于尾类稀缺。 |
| C36 | [AGFT](https://openaccess.thecvf.com/content/CVPR2026/html/Cui_AGFT_Alignment-Guided_Fine-Tuning_for_Zero-Shot_Adversarial_Robustness_of_Vision-Language_Models_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.29410) | 原始摘要 | 在对抗微调中保留跨模态对齐和原模型的预测知识。 | 可借微调先验保留对照；对抗扰动不是无支持文本监督。 |
| C37 | [The Geometry of Robustness](https://openaccess.thecvf.com/content/CVPR2026/html/Chopra_The_Geometry_of_Robustness_Optimizing_Loss_Landscape_Curvature_and_Feature_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.27139) | 原始摘要 | 联合研究损失曲率和特征流形对齐，处理分布内、域外及对抗鲁棒性权衡。 | 曲率用于模型优化，不能直接当作影响函数选样的有效性证明。 |
| C38 | [TANGO](https://openaccess.thecvf.com/content/CVPR2026/html/Ma_TANGO_Text-Anchored_Guided_Optimization_for_Robust_Fine-tuning_Vision-Language_Models_under_CVPR_2026_paper.html)；[本次来源](https://openaccess.thecvf.com/content/CVPR2026/supplemental/Ma_TANGO_Text-Anchored_Guided_CVPR_2026_supplemental.pdf) | 原文方法片段 | 补充算法 1：冻结文本锚，每轮更新干净样本集合与标签，以干净监督及正则调整视觉模型。 | 明确是噪声标签学习近邻；文本锚独立于噪声标签不等于绝对可靠真值。 |
| C39 | [STAR](https://openaccess.thecvf.com/content/CVPR2026/html/Fu_STAR_Test-Time_Adaptation_Can_Enhance_Universal_Prompt_Learning_for_Vision-Language_CVPR_2026_paper.html) | 官方摘要片段 | 在含域外样本的目标数据上进行通用测试时提示学习，处理类别多样性与伪标签不确定性。 | 这是适配而非单纯多裁剪集成；协议含测试时更新，不能与普通静态评测混用。 |
| C40 | [PACT](https://openaccess.thecvf.com/content/CVPR2026/html/Wang_PACT_Phase-Like_Transition_Constraints_in_Adapter-Based_Continual_Learning_of_Vision-Language_CVPR_2026_paper.html) | 官方论文片段 | 在适配器持续学习中施加类相变约束。 | 可作为容量与遗忘机制近邻；具体消融与长尾适用性未核。 |
| C41 | [Implicit Modality Decomposition](https://openaccess.thecvf.com/content/CVPR2026/html/Zhang_Parameter-Efficient_Adaptation_for_MLLMs_via_Implicit_Modality_Decomposition_CVPR_2026_paper.html) | 官方论文首页 | 通过隐式模态分解进行多模态大语言模型的参数高效适配。 | 模态不平衡不等于类别频率长尾；需核任务与监督再迁移。 |
| C42 | [Sparse Spectral LoRA](https://openaccess.thecvf.com/content/CVPR2026/html/Nejatimanzari_Sparse_Spectral_LoRA_Routed_Experts_for_Medical_VLMs_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2604.01310) | 原始摘要 | 医学模型的路由 LoRA 专家由不重叠奇异值分解片段初始化，并配合残差补偿。 | 参数少不等于总训练成本低；医学跨任务结果不能直接代表自然图像尾类。 |
| C43 | [Random Graph Adapter](https://openaccess.thecvf.com/content/CVPR2026/html/Jiang_Beyond_Graph_Model_Reliable_VLM_Fine-Tuning_via_Random_Graph_Adapter_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2507.10355) | 原始摘要 | 随机图文本适配器描述类别文本表示的多样性。 | 旧清单列入 MLLM 不准确；其文本特征适配路线不能直接当作生成式指令微调。 |
| C44 | [FairLLaVA](https://openaccess.thecvf.com/content/CVPR2026/html/Bhosale_FairLLaVA_Fairness-Aware_Parameter-Efficient_Fine-Tuning_for_Large_Vision-Language_Assistants_CVPR_2026_paper.html)；[本次来源](https://arxiv.org/abs/2603.26008) | 原始摘要 | 面向 LLaVA 的公平性感知参数高效微调。 | 人口群体公平与类别样本频率不同；不能无定义地互换公平指标与尾类准确率。 |
| C45 | [Condensed TTA](https://openaccess.thecvf.com/content/CVPR2026/html/Ge_Condensed_Test-Time_Adaptation_of_VLMs_for_Action_Recognition_CVPR_2026_paper.html) | 官方论文片段 | 通过语义压缩与缓存支持视频动作识别的测试时适配。 | VLM 动作识别不自动属于生成式 MLLM；需核具体模型与更新预算。 |

## 3. 历史长尾清单：6 个具名条目及 4 个邻近条目

这 10 行是历史记录中可识别的集合，**不是已补齐全部“16 篇长尾”**。外部问题记录未给出其余 10 个题名，不以自行搜得的其他论文填充原集合。以下多数只到原始摘要或官方片段；没有逐篇核定骨干，因此撤回“六篇全都基于 CLIP”的概括。

| ID | 论文 / 原始来源 | 本次整理的研究内容 | 关系与可引用边界 |
|---|---|---|---|
| L01 | [CUE](https://arxiv.org/abs/2605.01309) | 处理类别概念混淆与共享特征问题，并延伸到多标签情形。 | 原始摘要；不能简化成普通 logit adjustment。是否改善属性零覆盖需新实验。 |
| L02 | [CPT](https://arxiv.org/abs/2605.11939) | 聚类不变语义原型、局部神经塌缩及旋转约束。 | 原始摘要/补充片段含基类—新类少样本协议；不能仅因历史归类就认定已实测类别频率长尾。 |
| L03 | [FedPuReL](https://arxiv.org/abs/2605.02247) | 联邦长尾场景中的梯度净化、平衡全局学习和残差个性化。 | 已读原始摘要；客户端分布、通信成本与集中式训练不同。 |
| L04 | [AdaPrior](https://openaccess.thecvf.com/content/CVPR2026/supplemental/Bhat_AdaPrior_Bayesian-Inspired_Adaptive_CVPR_2026_supplemental.pdf) | 贝叶斯启发的自适应先验校准；补充算法涉及模型先验与验证数据。 | 原文算法片段；应核对训练/验证先验来源，不能默认无需验证数据。 |
| L05 | [CAR](https://arxiv.org/abs/2603.16732) | 用混淆结构与谱范数约束处理最差类别性能。 | 原始摘要；最差类鲁棒性与平均尾类指标须分开，不能因名称假定 CLIP 骨干。 |
| L06 | [SAMN](https://arxiv.org/abs/2606.02526) | 以相邻违例合并算法直接施加范数单调约束。 | 已读原始摘要；无需额外正则超参数不等于整套训练无超参数。 |
| L07 | [SearchAD](https://arxiv.org/abs/2604.08008) | 稀有图像数据整理与检索评测，结合目标定位线索。 | 原始摘要；属于数据搜集/检索，不等于现有全标注集训练剪枝。 |
| L08 | [Den-TP](https://github.com/RYNing/DenTP) | 用密度平衡整理轨迹预测训练数据。 | 作者来源；与总报告 D23 同一条目，不能重复计数，误差单位不是准确率。 |
| L09 | [FairFAL](https://openaccess.thecvf.com/content/CVPR2026/papers/Zong_Federated_Active_Learning_Under_Extreme_Non-IID_and_Global_Class_Imbalance_CVPR_2026_paper.pdf) | 极端非独立同分布和全局类别不平衡下的联邦主动学习；表 2 比较选择、伪标签与查询组件。 | 原文 §6.2/表 2 片段；主要预算是标注与通信，不能只按训练轮数比较。 |
| L10 | [DBG](https://arxiv.org/abs/2605.01468) | 通过决策边界生成处理头尾纠缠。 | 原始摘要；生成数据与挑选已有图像是不同干预，但应比较同预算效果。 |

## 4. 对当前研究的作用

【研究判断】这一批论文最值得直接接入当前实验设计的不是所有“CLIP”论文，而是：Role-SynthCLIP 的同图多文字对照、WikiCLIP 的知识适配、β-CLIP 的多粒度对齐、Concept Regions Matter 的区域干预、TANGO 的文本锚噪声学习。它们分别约束文字增量、局部证据、教师偏差等新颖性；目前没有据这些摘要确认它们已经解决用户提出的尾类属性视觉覆盖问题。

IsoCLIP 与 Reevaluating Intra-Modal Misalignment 必须成对保留；前者提出对齐方法，后者质疑将某些失败统一归因于模态内失配。对当前研究也应采用同样标准：既测文本先验，也测图像本身造成的错误。

正式写相关工作前还需取得全文并核对任务、数据、模型、损失和消融。特别是 ReAttnCLIP 的身份、历史“16 篇”的未命名成员及原始筛选流程，本轮没有闭合。

