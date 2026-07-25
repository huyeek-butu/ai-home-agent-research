# 开源持续学习的大模型：以家庭 AI Agent 为落地场景（范式·主权·权力格局 2024–2026）

> 【公众号发布提示】微信会屏蔽外链，文中引用已去除超链接，仅保留来源名称；完整来源见文末「参考文献」（已附 URL），请读者自行复制访问。
> 【封面建议】用一张「范式革命—数据主权—权力格局」三层主线示意图作首图；正文可导入秀米/135 编辑器排版。


**日期**：2026-07-25

---


## 引言

开源持续学习的大模型（Continual Learning for Open-Source LLMs）正从论文走向可部署的技术现实：具备抗灾难性遗忘能力的开源模型、面向端侧化的本地训练方法，以及围绕权重持续演化的开源生态，共同重塑"模型发布即冻结"的传统范式（Guo 等, 2025；LearnAIForge, 2026）。2024–2026 年间，持续学习机制在架构式、正则化式与回放式三类路径上取得实质进展（Kirkpatrick 等, 2017；Wang 等, 2023），端侧开源模型推理已成常态，端侧微调亦获工程实证（Song & Tang, 2025）。本报告的重点是开源持续学习的大模型技术本身（持续学习机制、开源模型、端侧化与开源生态），家庭 AI Agent 仅作为落地观察场景——用以检验这些大模型技术从论文走向消费级现实的一条典型路径，而非主题核心。

需要强调，用户原创笔记提出的三条强断言——预训练壁垒贬值、订阅瓦解、RAG 消亡——均属受争议命题，本报告在各章以平衡方式呈现，引言与结论据此保持审慎定调。本报告基于 2024–2026 权威外部来源，沿"范式革命—数据主权—权力格局—新风险与护栏—安卓时刻"五条主线，系统检视开源持续学习的大模型在机制可行性、开源生态与端侧化边界上的真实进展。市场叙事（如 Edge AI 高速增长，BCC Research, 2025）与技术落地间存在明显落差：机制上抗遗忘已可证（Guo 等, 2025），但"工程可行"不等于消费级现实，云边混合架构下云端训练仍居价值高地（TrendForce, 2026）。本报告旨在厘清愿景与实证之间的距离，而非为任何单一立场背书。

---

## 1. 第1章 范式革命与端侧化机制可行性

### 论点

有产业分析认为，大模型不应止步于"部署即冻结"的静态快照，而应在家庭场景中部署后持续进化、因环境而异，成为本地化的"生命体"；家庭微观常识可被编码进模型权重，去云端化则让数据主权回归用户。此类主张属愿景性判断，须以实证边界校准。本章核心命题：持续学习在机制上已能缓解灾难性遗忘，开源模型端侧推理已成常态，端侧微调在工程上已获初步实证——但其可行性存在明确的算力、能耗、显存与散热边界，且"数据主权回归"伴随本地安全对齐的新风险。

### 论据 ① 持续学习核心机制与生成式模型综述

生成式模型在适配新任务时普遍存在"灾难性遗忘"。Guo 等（2025）系统综述了面向 LLM、MLLM、VLA 与扩散模型的持续学习方法，按类脑记忆机制分为架构式、正则化式与回放式三类；Shi 等（2026）综述进一步将 LLM 持续学习划分为垂直连续与水平连续。经典正则化方法中，EWC（Kirkpatrick 等, 2017）通过 Fisher 信息矩阵保护重要权重，LwF（Li & Hoiem, 2017）借知识蒸馏让旧任务输出约束新任务；回放则保留少量旧样本或生成样本。参数高效方向，O-LoRA（Wang 等, 2023）用正交约束使各任务 LoRA 彼此独立以隔离遗忘；On-device LoRA 与元学习则进一步降低端侧更新开销（注：此二项暂无本次来源池链接，保留为待补来源断言）。2025 年业界亦提出参数化 RAG 思路（EmergentMind, 2025），将知识直接固化进权重而非仅检索。

### 论据 ② 开源模型端侧化趋势（推理常态）

据主流开源模型 2025 综述（LearnAIForge, 2026），2025 年主流开源模型 Llama、Mistral、Qwen2.5、Gemma3、Phi-4 均可通过 Ollama、llama.cpp 在本地运行。但需校准边界：7B–14B 级别在消费级硬件即可推理，而 70B+ 被明确判为"消费级硬件不现实，需多卡或服务器"。另据Apple 设备端基础模型 2025 更新，其 2025 年设备端基础模型为约 3B 参数、解码器权重 2bpw 量化。

### 论据 ③ 端侧训练工程实证

据Apple 的 MeBP（2025），其在 iPhone 15 Pro Max 上以低于 1GB 内存微调 0.5B–4B 模型。算力侧，NVIDIA Jetson AGX Thor 官方规格提供最高 2070 FP4 TFLOPS（约 2 PetaFLOPS）、128GB 显存、40–130W 功耗。小米 Miloco（2025）以 MiMo-VL-Miloco-7B 端侧视觉语言模型为核心，将米家摄像头画面在本地完成理解。美的于 2026 年 3 月发布"自进化家居智能体 MevoX"（北京商报, 2026），"自进化"目前属产业叙事，尚待技术披露。

### 数据摘要（端侧可行性关键指标）

| 主体 / 指标 | 关键数据 | 边界说明 | 出处 |
|---|---|---|---|
| MeBP（Apple） | iPhone 15 Pro Max 上 <1GB 内存微调 0.5B–4B 模型 | Apple 仅向开发者开放 rank-32 适配器、无用户级持续个人化 | MeBP（Apple, 2025） |
| NVIDIA Jetson AGX Thor | 2070 FP4 TFLOPS、128GB 显存、40–130W | 侧重边缘推理与实时控制，未描述设备侧训练工作流；需主动散热 | Jetson Thor 官方规格 |
| Apple 设备端基础模型 2025 | 约 3B 参数、2bpw 量化 | 仅向开发者开放 rank-32 适配器 | Apple On-Device FMs（2025） |
| 消费级端侧推理门槛 | 7B–14B 可推理；70B+ 需多卡/服务器 | 开源模型经 Ollama/llama.cpp 本地运行成常态 | LearnAIForge（2026） |
| 小米 Miloco | MiMo-VL-Miloco-7B 端侧 VLM | 视觉数据不出户 | Xiaomi Miloco（2025） |

### 分析：受争议命题

#### 命题 A——"端侧训练已可行"

支持证据：MeBP 在手机上 <1GB 微调 0.5B–4B；Miloco 端侧 VLM 已落地。边界：① 规模受限 0.5B–7B；② Apple 官方文档强调其 3B 模型仅向开发者开放 rank-32 适配器；③ Jetson Thor 需 40–130W 主动散热；④ Jetson 定位侧重边缘推理。

#### 命题 B——"去云端化使数据主权回归用户"

支持：本地推理使数据不出户。受争议：① 开放权重模型普遍存在对齐剥离漏洞，可被"灾难性越狱"（Huang 等, 2023）与相关对齐攻击（Yi 等, 2024）利用；② 业界已推出LlamaFirewall（2025）等本地护栏；③ 数据不出户仅解决传输隐私。

### 小结

机制上，持续学习已为多模态生成模型提供抗遗忘工具箱（Guo 等, 2025）；工程上，端侧微调在手机与家居边缘盒获初步实证（MeBP, 2025；Miloco, 2025）。"部署后自主进化、数据主权回归"的愿景须在算力/能耗/显存/散热四重边界内重新表述：当前可行的，是 0.5B–7B 量级、低频、用户或开发者授权的轻量持续适配；跨越此边界，仍需云端协同或专用边缘算力支撑。

---

## 2. 第2章 持续学习对家庭 Agent 三阶段路径的颠覆重塑

### 论点

家庭 Agent 的演进长期遵循"软件管家 → 家庭 AI 服务器 → 具身智能"的经典三阶段路径，且传统上由厂商季度更新驱动、呈线性推进。有产业分析认为，开源持续学习（Continual Learning, CL）正将每一阶段从"被动工具"重塑为"在本地持续进化的关系/能力主体"，从而打破线性节奏。本章的论证立场是：这一重塑在研究与边缘硬件层面得到**不同程度**的事实支撑，但并非均匀的消费级现实——阶段一（养成人格）在记忆层证据充分、在权重层受争议；阶段二（本地训练场）已有原型级验证；阶段三（Sim-to-Real 本地学习）研究势头强劲，但落地仍以仿真训练＋边缘部署为主。

### 论据

**阶段一：从"MCP 工具编排器"到"关系主体/养成人格"。** 当前家庭 Agent 的典型形态仍是工具编排器。小米 2025 年发布的 Xiaomi Miloco（Local Copilot）以 MiMo-VL-Miloco-7B 端侧视觉语言模型为核心，通过标准化 MCP 协议打通米家与 Home Assistant 生态、连接近 10 亿台 IoT 设备，代表了"软件管家"的编排范式 智东西, 2025。而持续学习对它的重塑，指向"在交互中养成只属于该家庭的独特记忆权重"。北邮 BAI-LAB 团队 2025 年开源的 MemoryOS 提供了分层人格记忆架构（短/中/长期人格记忆），可随每次对话自动更新用户画像与长期知识，在 LoCoMo 基准上 F1 提升 49.11% MemoryOS, 2025。Zylos Research（2026）亦指出，生产级个人智能体可通过外部记忆层持续描摹用户偏好与风格。这为正向支撑。

**阶段二：从"推理中枢/数据缓存"到"进化熔炉/本地训练场"。** 有观点认为家庭 AI 服务器将从缓存与推理升级为本地训练场，需 On-device Training 芯片、更高显存带宽与"可塑参数 vs 冻结常识"的记忆分层。事实层面，Apple 的 MeBP（Song & Tang, 2025）已在 iPhone 15 Pro Max 上以低于 1GB 显存对 0.5B–4B 模型做反向传播微调，较零阶优化收敛更快、效果更好 MeBP, 2025。边缘训练硬件亦在就位：NVIDIA Jetson AGX Thor 提供 128GB 显存、可跑 100B+ 模型 NVIDIA Jetson, 2025；Qualcomm RB3 Gen2 结合 Edge Impulse 支持"采集—训练—微调—部署"全流程 Qualcomm, 2025。记忆分层方面，O-LoRA 正交子空间学习与 EWC（弹性权重巩固）可在不破坏既有常识的前提下容纳新任务 Zylos, 2026; Guo 等, 2025。

**阶段三：具身智能以本地持续学习跨越 Sim-to-Real 鸿沟。** 有观点认为扫地机、机械臂、人形服务机器人将通过本地持续学习"特化"为竞争力。研究支撑强劲：NVIDIA Isaac GR00T N1 作为视觉-语言-动作（VLA）模型支持端到端模仿学习，Jetson 边缘可实现 sub-30ms 实时控制回路 NVIDIA Jetson, 2025；其 R²D² 研究（CoRL 2025）中 NeRD 支持真实数据微调与零样本 Sim-to-Real，VT-Refine 以约 30 条真实演示＋仿真 RL 微调后部署真机 NVIDIA R²D², 2025。清华与中国信通院《具身智能发展报告(2025)》提出 RLinf 框架，明确指向"真机强化学习训练" 清华/CAICT, 2025；逐际动力 LimX DreamActor 打通"仿真预训练—真机 RL 后训练"全流程 LimX, 2025。

### 分析（含受争议命题框架）

将三条强断言置于"支持 vs 边界"框架下审视：

- **"养成人格"（阶段一）——受争议命题。** 支持：MemoryOS 等记忆操作系统证明外部记忆层可承载长期人格画像 MemoryOS, 2025。边界：Apple 明确声明"在训练基础模型时不使用用户的私人数据或交互" Apple, 2025；Zylos（2026）指出个人效率智能体适配新任务后可能"忘记用户工作风格"，即灾难性遗忘风险。换言之，权重级个性化训练尚非消费级现实，当前最佳实践仍是外部记忆＋推理，而非本地权重微调。
- **"本地训练场"（阶段二）——部分成立、受硬件约束。** 支持：MeBP 证明 <1GB 显存即可端侧微调 MeBP, 2025。边界：Emergentmind（2026）综述指出移动 NPU/DSP"通常仅优化前向推理、缺乏专用反向支持"，边缘 DRAM 仅 4–12GB，而全量微调峰值显存 >20GB。Apple 已出货产品做的是端侧推理＋开发者适配器，并非用户个性化训练 Apple, 2025。
- **"Sim-to-Real 本地学习"（阶段三）——研究热、落地冷。** 支持：GR00T、NeRD、RLinf、LimX 等显示仿真到现实的迁移路径 NVIDIA Jetson, 2025；NVIDIA R²D², 2025。边界：NVIDIA Jetson 博客明确写明训练/微调发生在非边缘（Isaac Sim ＋ LeRobot），Jetson 负责部署与推理 NVIDIA Jetson, 2025；Zylos（2026）亦指出真正"每次交互在线学习"不现实，实际为日/周级定期重训，存在知识滞后。

**事实 vs 观点。** 市场规模属事实：Precedence Research（2025）估算自主 AI 智能家居市场 2025 年 181 亿美元、2035 年达 1712.9 亿美元（CAGR 25.20%）Precedence, 2025。但需注意的是，该报告通篇未提及"持续学习"一词，反映市场叙事与技术现实之间存在落差。"持续学习对三阶段具颠覆性重塑"本身是一种观点性解读，须以边界证据平衡。

**非线性加速。** 有观点称持续学习使三阶段不再线性等待厂商季度更新、转为本地实时进化。记忆层/适配器级适配（MemoryOS、LoRA）确实支持近实时个性化；但权重级持续训练受显存、NPU 反向能力与隐私约束，所谓"实时进化"在当下更多是方向而非现状。至于"去平台化高迁移成本"，属观点性推演——有产业分析认为本地养成记忆权重将抬高换家迁移门槛，但尚缺跨平台迁移成本的量化实证。

### 小结

持续学习确实在重塑家庭 Agent 三阶段，但程度不均、且尚未成为普遍消费级现实：阶段一的人格养成在记忆层成立、权重层受争议；阶段二的本地训练场有原型验证、受显存带宽掣肘；阶段三的 Sim-to-Real 本地学习研究活跃、落地仍以仿真训练＋边缘推理为主。对"颠覆性重塑"应保留审慎——可塑性-稳定性困境、硬件与隐私边界，决定了家庭 Agent 的进化更可能是"记忆/适配器快变 ＋ 核心权重慢变"的分层节奏，而非无代价的实时突变。

---

## 3. 第3章 记忆范式之争（RAG vs 权重即记忆）与家庭数据主权

### 论点：从"RAG 已死"的叙事到混合记忆的真实图景

**【受争议命题】** "RAG 消亡、权重即记忆复兴"并非严谨论断，而是一轮随上下文窗口扩张而周期复现的媒体叙事。自 2023 年 5 月 Anthropic 推出 100K 上下文的 Claude 起，每逢更长窗口发布，"为何还要检索"的论调便卷土重来 LightOn, 2025。RAG 原作者 Douwe Kiela 明确反驳：RAG 的初衷正是"参数化记忆 + 非参数化记忆"的最佳组合，所谓"消亡"误解了其本质 Kiela, 2025。

**【事实】** 真实工程图景并非二选一，而是参数化记忆与外部检索的混合作业。参数化 RAG（PRAG）通过 LoRA 把文档知识直接编码进模型权重，在知识密集型问答上较标准 RAG 提升 2.5–6 个绝对 F1 点 Emergentmind, 2025。其动态演进 DyPRAG 进一步用轻量"参数翻译器"把文档即时映射为 LoRA 适配器，在法律判决基准 PL-CA 上将上下文长度由约 20k token 压缩到 <500 token，推理速度提升 2–3 倍，且效果持平或更优 Tan et al., 2025。

### 论据：混合记忆的三层结构与商业落地

**【观点】** 有产业分析认为，家庭 Agent 应把高频"热记忆"（家庭日程、成员偏好、常用菜谱）内化进参数，把低频"冷知识"（维修手册、档案）留在外部检索。这一判断得到多项证据支持，但也面临反证。

**【支持证据】** 参数化记忆的"热内化"确有工程价值。MemOS 将记忆封装为标准化 MemCube，统一管理明文、激活、参数三类记忆，并支持高频明文记忆向激活缓存、再向参数记忆逐级"凝固" MemTensor 等, 2025。MIRIX 将用户长期偏好与人格存为永久 KV 对的"核心记忆"，每次回答强制加载，同样体现热记忆固化思路 Wang & Chen, 2025。在端侧，苹果 2025 设备端基础模型（约 3B）提供 rank-32 适配器工具包，开发者可在本地训练轻量 LoRA 以扩展技能，且推理全程不联网 Apple, 2025；小米 Miloco 则将自研视觉语言模型部署到家庭边缘设备，所有视觉数据在端侧完成计算、不向外部服务器传输 智东西, 2025。

**【反证】** 但"权重即记忆复兴"若理解为"以参数记忆取代检索"，则存在硬性约束。其一，参数化记忆面临持续学习的核心难题——灾难性遗忘：模型在学习新知识时易覆盖旧知识 Guo et al., 2025。其二，长上下文本身存在"上下文悬崖"：研究显示当上下文超过约 32k token，模型抽取正确细节的准确率跌破 50%，盲目灌入长文本反而损害效果 xdge, 2025。其三，RAG 在海量冷知识与可溯源场景仍不可替代——Kiela 指出企业知识库以 TB 计，即使 10M 上下文也仅覆盖其极小部分 Kiela, 2025。商业产品亦非"放弃 RAG"：逆向分析显示 ChatGPT 采用四层静态注入、Claude 采用 RAG 式按需检索（conversation_search 含语义匹配），两者均押注大上下文，但 Claude 的检索仍依赖向量/混合检索 Zilliz, 2025。

### 分析：家庭数据主权与"可学习操作系统"的边界

**【观点】** 有产业分析认为，持续学习使家庭数据不再经 API 回流巨头训练、改在本地编码，从而重塑家庭数据主权。

**【事实】** 本地化确有隐私收益：小米 Miloco 遵循"家庭隐私不外流"原则，视觉数据端侧计算 智东西, 2025；MIRIX 桌面助理将数据存入本地 SQLite Wang & Chen, 2025。

**【平衡】** 但主权需与能力权衡。TrendForce 指出，边缘 AI 虽分担实时推理，云端对训练、迭代与长上下文推理仍"不可或缺" TrendForce, 2026。自主智能家居市场 2025 年 181 亿美元、2035 年达 1712.9 亿美元（CAGR 25.20%），边缘 AI 是驱动，数据隐私仍是首要挑战 Precedence Research, 2025。故"本地编码 + 云边协同"比纯本地化更现实。

**【受争议命题】** 有产业分析认为，参数化与外部检索融合正"模糊模型与数据库边界、催生可学习操作系统"。MemGPT 以 OS 虚拟内存分页管理 LLM 上下文 Packer et al., 2023；MemOS 把记忆视为系统资源统一调度三类记忆 MemTensor 等, 2025；MIRIX 以多智能体协同六类记忆 Wang & Chen, 2025。**【反证】** 但"可学习 OS"仍是隐喻：MemOS/MIRIX 仍依赖向量库与图库，权重与数据库未真正合一；训练主导权仍在云端，边界消融更多是调度层抽象而非物理融合。

### 小结

"RAG 消亡"是叙事而非事实；真实图景是参数化热记忆（LoRA/DyPRAG）与外部冷检索（RAG）协同的混合记忆。家庭场景中，持续学习推动数据本地编码、强化主权，但能力与隐私的权衡要求云边协同。把模型与数据库"操作系统化"统一调度是值得关注的方向，但其"边界消融"命题仍待实证检验。

---

## 4. 第4章 权力格局与商业模式冲击

### 论点

开源持续学习与端侧部署正在从底层撼动家庭 AI 的价值分配逻辑。有产业分析认为，传统闭源巨头"重金预训练—按次卖 API"的护城河可能被削弱，本地后验知识（家庭场景持续累积的个性化数据）价值上升，并连带冲击 SaaS 订阅模式、推动硬件厂商夺回主权。但这一组判断在 2024–2026 年的市场数据面前存在显著争议，本章对"预训练壁垒贬值""订阅瓦解"以**受争议命题**方式平衡呈现，并厘清硬件厂商"起义"的真实边界。

### 论据①：受争议命题——预训练壁垒是否相对贬值

*支持方观点与事实*：端侧开源模型的能力已足以支撑多数家庭场景。行业评测显示，Llama 3、Mistral、Qwen 等开源模型（含 1B–3B 端侧规格）可在消费级硬件本地运行，并支持用私有数据微调 LearnAIForge, 2026。持续学习研究进一步指出，生成式模型可通过架构/正则/回放三类方法缓解灾难性遗忘，使模型在家庭端持续吸收后验知识而保持质量 Guo 等, 2025。有产业分析据此认为，家庭场景的差异点正从"通用预训练知识"转向"持续学习框架 + 家庭数据闭环"。

*反方事实与观点*：TrendForce 2026 年的行业研究（赞助内容）明确判断，"边缘成长、云端萎缩"的零和场景不会发生——"Cloud + Edge"混合架构才是主流，边缘侧重实时推理，云端仍主导模型训练、迭代、跨域协作与长上下文推理 TrendForce, 2026。这与"预训练壁垒贬值"叙事相左：云端训练/迭代仍是价值高地。订阅侧数据同样构成反证——OpenAI 2026 年 2 月宣布 ChatGPT 周活跃用户达 9 亿、付费订阅超 5000 万、年化收入运行率超 250 亿美元，订阅经济仍在扩张 OpenAI via 财联社, 2026。据此，至少头部闭源 API 厂商尚未显现"壁垒贬值"的财务迹象。

### 论据②：API 经济与 SaaS 订阅冲击

开源持续学习提供了替代路径。其一，买断制 + 本地进化：用户一次采购硬件/模型，后续靠端侧持续学习自我优化，降低对按次 API 的依赖。其二，"Red Hat 模式"——协议层开源、服务层收费。红帽将其企业 AI 战略概括为"any model, any hardware, any cloud"，通过 vLLM、llm-d、Llama Stack 等开源组件占据推理与调度层，再以订阅制提供治理、GPU-as-a-Service 与 Model-as-a-Service Red Hat, 2025；红帽大中华区总裁亦强调企业级 AI 的恰当路径是"开源 + 混合式 + 小模型" 21世纪经济报道, 2025。

这是否构成对 OpenAI/Anthropic 类 API 公司的结构性利空？*观点层面*，有产业分析认为是"局部调整而非颠覆"：混合架构下云端训练与长上下文推理仍依赖闭源前沿模型，且订阅数据仍在增长。但须警惕另一观点——开源商业化的收入真实性与可持续性仍存疑，媒体分析指出除红帽外多数开源大模型企业尚未跑通盈利，单纯 API/服务收费"为时尚早" The Paper, 2025。因此 Red Hat 模式是可行参照，而非已被验证的普遍解。

### 论据③：硬件厂商"起义"

最确定的趋势是硬件厂商从"被搭载方"转向"模型主权方"。*事实层面*：Apple 2025 年以约 30 亿参数端侧模型 + Private Cloud Compute 构建隐私优先的端云套件，端侧免费推理、训练不使用用户私人数据 Apple On-Device FMs, 2025；小米 2025 年 11 月发布 Xiaomi Miloco（Local Copilot），以自研 MiMo-VL-Miloco-7B 端侧视觉语言模型接入近 10 亿台 IoT 设备，视觉数据在端侧完成计算 智东西, 2025；机器人厂商也出现端侧"烧模型"的同类动向。

*权力天平判断*：有产业分析认为，掌握场景与数据的硬件厂正从"弱于模型厂"转向"至少持平"。但须客观界定边界——训练算力仍高度集中于 NVIDIA 与云厂商，TrendForce 亦指出 2026 年五大 CSP 资本开支同比增超 50% TrendForce, 2026。因此"端侧主权"更准确地说是**推理与个性化主权**，而非全栈训练主权。市场数据支撑端侧方向：BCC Research 估全球 Edge AI 市场 2025–2030 CAGR 达 36.9% BCC via Benzinga, 2025；自主 AI 智能家居市场 2026–2035 CAGR 25.2% Precedence, 2025；TechRT 统计 2026 年超 75% 企业数据将在边缘产生 TechRT, 2026。

### 小结

①"预训练壁垒贬值"与"订阅瓦解"属于**受争议命题**——支持方（端侧开源够好 + 持续学习闭环）与反方（TrendForce 混合架构、OpenAI 订阅扩张）证据均强，不应当定论。②API 经济向本地化/Red Hat 服务化迁移是真实替代路径，但对闭源 API 公司是结构性利空还是局部调整，取决于云端训练价值是否可被替代，目前更偏向**局部调整**。③硬件厂商"起义"是较确定的趋势，主权边界集中在推理与个性化层，训练算力集中格局短期难破。

---

## 5. 第5章 新风险与护栏赛道及投资再分配与「安卓时刻」

### 论点

开源持续学习让家庭 Agent 从"出厂即定型"走向"边用边学"，把安全对齐信任边界从模型厂商转移到家庭本地。有产业分析认为这将催生新风险、新护栏赛道、资本从模型层向框架层与端侧芯片层再分配，并可能触发 AI"安卓时刻"。但走向非线性确定——风险实证与市场规模可验证，而"主权在民"终局仍属受争议命题。

### 论据

① 新风险：开源武器化——Yi 等（2024, ACL）证明仅凭参数访问通过 RSFT/RPO 即可高效逆转开放权重模型安全对齐；Huang 等（2023）显示仅调解码超参即将 11 个开源模型失对齐率 0%→95%+；Yang 等（2023）证明仅约 100 条恶意样本即可在 1 GPU 小时内逆转安全对齐；Dark LLMs 威胁综述（2025）归纳"开源安全剥离"。价值观漂移与错误服从——Qi 等（2023）证明即使纯良性数据微调，模型拒绝有害请求能力也下降；有产业分析推演家庭级危害属前瞻风险非已实证。灾难性遗忘残余——长期在线学习可能覆盖通用常识，AI 安全目录·灾难性遗忘指南（2026）归纳该风险；杨一博（2026）强调"物理行动必须可验证可停止可回滚"。数据中毒——攻击者以"访客"身份交互注入恶意样本污染持续学习数据，Meta LlamaFirewall（2025）列为重点防御。算力能耗焦虑——训练比推理耗电多；Agentic AI 使算力需求预期放大至此前 100 倍（NVIDIA CEO GTC2025 转引 TrendForce）；全球数据中心耗电持续攀升、AI 负载占比快速扩大。

② 护栏新赛道：Meta 2025 开源 LlamaFirewall，含 PromptGuard2（越狱检测）、Agent Alignment Checks（思维链审计检测提示注入与目标偏移）、CodeShield（不安全代码静态分析）。有产业分析认为端侧将出现"免疫系统"新品类：实时监控学习方向、检测价值观偏移、一键回滚权重快照——对应 EWC（Kirkpatrick 等, 2017）对重要权重"锁定"思想。

③ 投资再分配：边缘 AI TrendForce（2026）估 2025 年 360 亿美元→2029 年 840 亿美元（CAGR 23.5%）；BCC Research（2025）2024 年 87 亿美元→2030 年 568 亿美元（CAGR 36.9%）；中国端侧 AI 据中研普华（2025）突破 2500 亿元、2030 达 1.2 万亿元（CAGR 30.8%）；自主 AI 智能家居 Precedence（2025）2025 年 181 亿美元→2035 年 1712.9 亿美元（CAGR 25.20%）。价值下沉：定价权从模型层向持续学习框架层（EWC/LwF/Replay/端侧 LoRA/Meta-learning 成核心 IP）与端侧训练芯片层转移。FCN 时刻/模型营养师/去中心化联邦网络（Bittensor/FLock.io）属前瞻判断早期验证。

④ 「安卓时刻」终局——受争议命题：支持方——开源模型（Llama/Gemma/Qwen/MiniCPM）已可手机本地运行（Emergentmind·设备端微调综述（2026））；Google AI Edge Gallery 据聚合平台 Trend Hunt 估算两月内下载约 50 万次（trend-hunt, 2026）；端侧 AI 主流化使"隐私+智能"共存（x-techcon·端侧 AI 需求大爆发, 2025）。反方约束——前沿模型仍越来越大成本飙升、云端仍掌握最强模型与数据；芯片算力高度集中；武器化等风险可能反向推动监管将护栏回收到云端集中管控。故"安卓时刻"更可能是混合架构下部分再分配。

### 分析

风险实证链（RSFT/RPO→解码攻击→Dark LLMs→LlamaFirewall）相互印证，说明"去护栏"门槛极低且护栏可开源化，构成正负双向开放的产业基础。投资数据四方机构交叉验证真实可信但口径年份须区分。"安卓时刻"确定性来自开源+端侧技术扩散，约束来自算力集中度与监管反弹。

### 小结

开源持续学习把安全责任下沉本地，放大武器化/价值观漂移/遗忘残余/能耗四类风险，催生 LlamaFirewall 式实时护栏新赛道；资本向框架层与端侧芯片层再分配，市场数据获多方验证；"AI 主权在民"作为受争议命题，实现程度取决于开源扩散与安全治理动态平衡。

### 数据摘要

| 细分赛道 | 口径机构 | 起始年规模 | 终值年规模 | CAGR | 币种 |
|---|---|---|---|---|---|
| 边缘 AI | TrendForce (2026) | 2025: 360 亿美元 | 2029: 840 亿美元 | 23.5% | 美元 |
| 边缘 AI（激进口径） | BCC (2025) | 2024: 87 亿美元 | 2030: 568 亿美元 | 36.9% | 美元 |
| 中国端侧 AI | 中研普华 (2025) | 2025: 2,500 亿元 | 2030: 1.2 万亿元 | 30.8% | 人民币 |
| 自主 AI 智能家居 | Precedence (2025) | 2025: 181 亿美元 | 2035: 1,712.9 亿美元 | 25.20% | 美元 |

---

## 结论

综合五章研究，开源持续学习的大模型在技术范式、主权与权力格局上的命题可概括为"机制可行、现实受限"。第一，端侧范式革命确有机制支撑——持续学习已为多模态生成模型提供抗遗忘工具箱（Guo 等, 2025），EWC 正则与 LlamaFirewall 本地护栏印证安全可内置于权重层（Kirkpatrick 等, 2017；LlamaFirewall, 2025）——但存在算力、能耗、显存、散热四重边界，规模止于 0.5B–7B。第二，用户笔记的三条强断言均受争议：预训练壁垒并未瓦解（云端仍主导训练，TrendForce, 2026；OpenAI 订阅仍在扩张，财联社, 2026）；RAG 与权重记忆实为混合协同而非更替（Kiela, 2025）；订阅模式亦未消亡。第三，安全责任下沉本地放大了对齐剥离、价值观漂移等风险，同时催生端侧护栏新赛道。第四，"安卓时刻"更接近价值向框架层与芯片层的"部分再分配"，而非全面权力转移（Emergent Mind, 2026）。

上述结论以家庭 AI Agent 作为承载案例与落地观察场景：它检验了开源持续学习的大模型如何从论文走向消费级现实，但其自身并非技术主体。本报告呼应引言的审慎框架——开源持续学习的大模型更可能走向"记忆／适配器快变、核心权重慢变"的分层进化节奏，主权宜理解为数据控制权本地化而非模型行为完全可控。未来研究应聚焦边缘 NPU 的反向传播支持、本地护栏标准化，以及消费级个性化实证缺口。

---

## 参考文献

- AI Security and Safety, 2026, AI Security and Safety 指南 灾难性遗忘指南：https://aisecurityandsafety.org/guides/catastrophic-forgetting-guide
- Apple, 2025, Apple 机器学习研究团队 Apple Foundation Models 2025 Updates：https://machinelearning.apple.com/research/apple-foundation-models-2025-updates
- BCC Research, 2025, BCC Research Edge AI 市场报告：https://www.benzinga.com/node/48002789
- Bittensor, 2025, Bittensor 团队 Bittensor 论文：https://arxiv.org/abs/2505.21684
- ChinaIRN（中国产业研究院）, 2025, 中国产业研究院 中国端侧 AI 市场规模预测：https://big5.chinairn.com/hyzx/20250825/143438205.shtml
- Dark LLMs Survey, 2025, AlphaXiv 综述 Dark LLMs 综述：https://www.alphaxiv.org/overview/2505.10066v1
- Emergent Mind, 2025, Emergent Mind Parametric RAG（参数化 RAG）：https://api.emergentmind.com/topics/parametric-rag
- Emergent Mind, 2026, Emergent Mind On-Device Fine-Tuning（端侧微调）：https://www.emergentmind.com/topics/on-device-fine-tuning
- FLock, 2025, FLock 团队 Bittensor Subnet FLock Off Now Live：http://www.flock.io/blog/bittensor-subnet-flock-off-now-live
- Guo 等, 2025, Guo 等 持续学习综述（LLM／MLLM／VLA）：https://arxiv.org/abs/2506.13045
- Huang 等, 2023, Huang 等 解码超参逆转对齐研究：https://arxiv.org/abs/2310.06987
- Kiela, D., 2025, Kiela（RAG 原作者）RAG 消亡论反驳：https://www.163.com/dy/article/JTTJEMQC0519EA27.html
- Kirkpatrick 等, 2017, Kirkpatrick 等 Overcoming Catastrophic Forgetting（EWC）：https://www.pnas.org/doi/10.1073/pnas.1611835114
- LearnAIForge, 2026, LearnAIForge 最佳开源 AI 模型 2025（Llama／Mistral／Qwen）：https://www.learnaiforge.com/articles/best-open-source-ai-models-2025-llama-mistral-qwen
- Li & Hoiem, 2017, Li & Hoiem Learning Without Forgetting（LwF）：https://doi.org/10.1109/TPAMI.2016.2598333
- LimX Dynamics, 2025, 逐际动力 DreamActor：http://limx.cn/zh/news/BK000025
- LlamaFirewall, 2025, Meta LlamaFirewall 三层护栏：https://arxiv.org/abs/2505.03574
- MemTensor 等, 2025, MemTensor 等 MemOS：统一记忆操作系统：https://news.qq.com/rain/a/20250707A04QB600
- MemoryOS, 2025, MemoryOS 团队 分层人格记忆系统：https://arxiv.org/abs/2506.06326
- NVIDIA, 2025, NVIDIA Jetson AGX Thor 边缘计算模组：https://www.nvidia.com/en-gb/autonomous-machines/embedded-systems/jetson-thor
- NVIDIA Research, 2025, NVIDIA 研究院 R²D²：机器人学习的神经突破：https://developer.nvidia.com/zh-cn/blog/r2d2-three-neural-breakthroughs-transforming-robot-learning-from-nvidia-research/
- ObjectBox, 2025, ObjectBox Edge AI Anywhere, Anytime：https://objectbox.io/dev-how-to/edge-ai-anywhere-anytime/
- Packer 等, 2023, Packer 等 MemGPT：https://arxiv.org/abs/2310.08560
- Precedence Research, 2025, Precedence Research Autonomous AI in Smart Homes Market：https://www.precedenceresearch.com/autonomous-ai-in-smart-homes-market
- Qi 等, 2023, Qi 等 良性微调削弱安全拒绝能力：https://arxiv.org/abs/2310.03693
- Qualcomm, 2025, Qualcomm RB3 Gen 2 + Edge Impulse 边缘 AI 开发套件：https://www.qualcomm.com/developer/blog/2025/03/powering-iot-developers-with-edge-ai-qualcomm-rb3-gen2-kit-now-integrated-with-edge-impulse
- Red Hat, 2025, Red Hat 开源协议＋服务收费模式：https://red.ht/4rbRmzq
- Shi 等, 2026, Shi 等 垂直／水平连续学习分类：https://aminer.cn/pub/662b0b1701d2a3fbfc6610d2
- Song & Tang, 2025, Song & Tang（Apple）MeBP：端侧 <1GB 微调：https://arxiv.org/abs/2510.03425
- Tan 等, 2025, Tan 等 DyPRAG：动态参数化 RAG：https://arxiv.org/abs/2503.23895
- TechRT, 2026, TechRT Edge AI Statistics（边缘 AI 统计）：https://techrt.com/edge-ai-statistics/
- The Paper（澎湃新闻）, 2025, 澎湃新闻 开源大模型企业盈利困境：https://m.thepaper.cn/newsDetail_forward_30423121
- TrendForce, 2026, TrendForce Building Dedicated AI Factories（云边混合主流）：https://www.trendforce.com/news/2026/03/26/sponsored-content-building-dedicated-ai-factories-confronting-the-power-compute-national-power-challenge
- Tsinghua University（清华大学）, 2025, 清华大学 RLinf：强化学习推理基础设施：https://www.ee.tsinghua.edu.cn/info/1076/4984.htm
- Wang & Chen, 2025, Wang & Chen MIRIX：核心记忆系统：https://finance.sina.cn/tech/2025-07-15/detail-inffpwts2115095.d.html
- Wang 等, 2023, Wang 等 O-LoRA：https://aclanthology.org/2023.findings-emnlp.715.pdf
- xdge, 2025, xdge 上下文悬崖（>32k 跌破 50%）：https://blog.xdge.ai/page/5
- x-techcon, 2025, x-techcon 端侧 AI 主流化探讨：https://m.x-techcon.com/article/10836.html
- Yang 等, 2023, Yang 等 约 100 恶意样本逆转对齐：https://arxiv.org/abs/2310.02949
- Yi 等, 2024, Yi 等 RSFT／RPO 逆转对齐：https://aclanthology.org/2024.findings-acl.549/
- Zilliz, 2025, Zilliz Claude 仍保留 RAG 式检索：https://www.53ai.com/news/RAG/2025122487503.html
- 北京商报, 2026, 北京商报 美的 MevoX"自进化"产业叙事：https://so.html5.qq.com/page/real/search_news?docid=70000021_64269b8092c78052
- 财联社, 2026, 财联社 OpenAI 2026-02 周活与 ARR 数据：https://www.cls.cn/detail/2298041
- 杨一博, 2026, 杨一博 灾难性遗忘残余分析：https://www.sohu.com/a/1051237072_122063682
- 智东西, 2025, 智东西 小米 Miloco 端侧 VLM 与近 10 亿 IoT 连接：https://new.qq.com/rain/a/20251114A05ONT00
- 21 世纪经济报道, 2025, 21 世纪经济报道 Red Hat 开源商业模式报道：https://finance.sina.com.cn/tech/roll/2025-04-04/doc-inerzfqq4425225.shtml

---

## 待完善事项

- 第5章"有产业分析推演家庭级危害属前瞻风险非已实证"一句为无链接推断性陈述，已在正文显式标注"属前瞻风险非已实证"作为自证；建议后续补具体出处或明确为团队研判。
- 第1章"On-device LoRA 与元学习"一句标注为待补来源断言，尚未补入权威链接。
- 第1章美的 MevoX 引用为腾讯新闻搜索跳转页（so.html5.qq.com），非直接报道原文，可追溯性偏弱。
- 第5章 Google AI Edge Gallery 下载量取自聚合平台 Trend Hunt 估算，数字溯源偏弱。

---

> 本报告由 AI 深度研究团队生成，重要决策请经专业人员核验。所有引用来源请用户在重要场景下二次核验时效性与真实性。
