# 先数字、再连接、后物理：类 WorkBuddy AI 家庭管家的三阶段演进路径研究（2024–2026）

> 【知乎发布提示】建议添加话题：#人工智能  #智能家居  #AI智能体  #家庭机器人  #科技趋势；正文外链可直接点击。
> 发布路径：知乎 → 写文章 → 直接粘贴本 Markdown 即可。


**日期**：2026-07-25

---


## 引言

家庭 AI 智能体正从"会对话的语音助手"走向"能调度、可执行、最终具身的家庭管家"。据 MarketsandMarkets 测算，全球 AI Agent 软件市场 2025 年约 78.4 亿美元、2030 年将达 526.2 亿美元（CAGR 46.3%）（[AI Agents Market](https://www.marketsandmarkets.com/blog/ICT/ai-agents-market)），但落地路径远未收敛：是一步到位卖机器人，还是先软件、后连接、再物理？本研究以用户原创笔记《AI家庭智能体三阶段路径》为框架锚点，逐条叠加 2024–2026 年权威外部来源进行验证、修正与扩展，系统刻画"先数字、再连接、后物理"的三阶段演进主线。

报告覆盖三个阶段与两条纵向分析线：阶段一以纯软件 Agent 建立"家庭决策中枢"与数据飞轮（Alexa+、Gemini for Home、小美 AI 等已商用，[Introducing Alexa+](https://www.aboutamazon.com/news/devices/new-alexa-generative-artificial-intelligence)）；阶段二以家庭 AI 服务器中枢打通 Matter/多协议连接、端侧算力与数字孪生（[NIST 数字孪生框架](https://www.nist.gov/node/1899736)）；阶段三沿 3A→3B→3C 渐进引入具身智能（[Introducing Figure 03](https://www.figure.ai/news/introducing-figure-03)）；并提炼演进底层逻辑与终局形态。

本研究发现三点核心结论预告：其一，三阶段呈"已商用/加速/前瞻"的成熟度梯度；其二，路径由技术错配、信任梯度与数据飞轮三条约束共同决定；其三，连接碎片化、隐私焦虑与莫拉维克悖论是横贯三阶段的共性瓶颈。下文将逐一展开。

---

## 1. 阶段一：软件切入的 AI 数字管家——家庭知识中枢、采购代理、日程协调与数据飞轮

**论点**：在"先数字、再连接、后物理"的演进框架中，第一阶段以纯软件 Agent（App、语音助手、家庭群聊 Bot）以最低成本在家庭内部建立"决策中枢"身份。它不改造任何物理环境，而是通过知识管理、采购代理、教育健康顾问、跨平台日程协调四类数字能力沉淀用户信任、积累私有数据，为后续阶段"让 Agent 实控环境"埋下意愿伏笔。

**论据：能力边界与产业落地**

这一阶段的 Agent 完全运行在软件层，其能力被严格限定在"非物理控制"之内，可归纳为四块。第一，**家庭知识管理**：借助 RAG 私有知识库承载维修记录、保单、药品与疫苗档案；Amazon 于 2025 年 2 月发布的 Alexa+ 已能接收并长期记忆用户上传的 PDF（如业主公约、孩子训练日程），并据此回答具体查询 ([Introducing Alexa+](https://www.aboutamazon.com/news/devices/new-alexa-generative-artificial-intelligence))。第二，**消费采购代理**：类比 WorkBuddy 代订机票，Alexa+ 可自主联网比价、下单，甚至依据摄像头所见与饮食偏好自动补货 ([Alexa+ agentic capabilities](https://www.digitaltrends.com/home/4-reasons-why-you-should-really-pay-attention-to-amazons-alexa-assistant/))。第三，**教育健康顾问**：把枯燥材料转为儿童互动学习内容的同类能力已在 Alexa+ 实测中出现 ([DigitalTrends](https://www.digitaltrends.com/home/4-reasons-why-you-should-really-pay-attention-to-amazons-alexa-assistant/))；第四，**跨平台日程协调**：Google 于 2025 年 8 月推出、10 月开放早期访问的 Gemini for Home 旨在取代 Google Assistant，统一调度 Nest 与 Home 应用中的多方日程 ([Gemini for Home](https://blog.google/products-and-platforms/devices/google-nest/gemini-for-home-launch/))。

国内厂商沿同一逻辑推进"家庭大脑"。美的"小美 AI 智能体"以六大 Agent 提供主动服务，其 IoT 连接设备已超 1.259 亿台 ([美的全屋智能](https://new.qq.com/rain/a/20251103A051ES00))；华为鸿蒙智家 2025 年升级的"小艺管家"标榜"懂家更懂你"，并在精装房智能家居市场取得市占率第一 ([华为鸿蒙智家](https://www.ceweekly.cn/company/2025/1224/486538.html))；小米米家 App 月活突破 1.1 亿、IoT 平台连接设备达 9.05 亿台 ([智家市场观察](https://www.toutiao.com/article/7597744242563252776/))。市场面上，MarketsandMarkets 测算全球 AI Agent 软件市场 2025 年约 78.4 亿美元、2030 年将达 526.2 亿美元，CAGR 46.3%，并把"数据隐私与信任"列为首要抑制因素 ([MarketsandMarkets](https://www.marketsandmarkets.com/blog/ICT/ai-agents-market))。

**分析：战略价值与瓶颈并存**

从战略看，第一阶段是建立"用户信任"与"数据飞轮"的关键窗口。MIT 的一项研究指出，具备长期记忆（LTM）的个人 AI 助手能保留并情境化过往交互、持续适配用户偏好，是"理解你"而非仅"帮你"的技术前提；但同一研究也警示，长期记忆引入了新的伦理脆弱性，部署须审慎 ([MIT LTM 论文](https://arxiv.org/html/2409.11192v1))。一旦家庭成员养成"家庭事务问 Agent"的习惯，让其实控环境的意愿便自然生长——这正是软件切入的深层用意。

反对与制约观点同样清晰。其一，**信任建立极难**：MarketsandMarkets 将信任与透明度列为市场主要障碍；Amazon CEO 更确认 Alexa+ 将嵌入广告，引发"助手变推销"的信任侵蚀担忧 ([Alexa+ 广告化](https://techkv.com/amazon-alexa-plus-ai-ads-launch/))。其二，**隐私顾虑突出**：2025 年江苏消保委指出部分产品藏"数据暗门"，云优先架构放大泄露风险 ([数据暗门](https://www.sohu.com/a/994830648_122014422))；学术视角亦强调智能家居"全景敞视"对公私边界的侵蚀 ([隐私忧虑](https://www.hbskw.com/p/83501.html))。其三，纯软件**无法触达物理层**，"从帮你到懂你"的能力天花板客观存在，须待第二阶段边缘中枢补位。

**小结**

阶段一以零环境改造成本验证了"家庭决策中枢"的可行性，并用真实产业落地（Alexa+、Gemini for Home、小美 AI、小艺管家、米家）与高速增长的市场数据证明其并非空想。其真正的资产不是功能，而是信任与数据飞轮——这恰是向第二阶段"边缘中枢"跃迁的入场券，而隐私与信任瓶颈则构成主要阻力。

---

## 2. 阶段二：家庭 AI 服务器中枢——Matter 互联、边缘本地算力、数字孪生与感知-决策-执行闭环

**论点：从"信息层"下沉到"物理层"。** 在第二阶段，家庭 AI 管家不再停留于软件与对话框，而是以一台"家庭 AI 服务器"为中枢，把分散的设备、传感器与空间本身映射为可计算的家庭数字孪生（Digital Twin），使系统从信息协同升级为物理操作，形成"感知—决策—执行"的本地闭环。这一跃迁的本质，是家庭从"互联网+"走向"信息物理系统（CPS）"的进化——也是"先数字、再连接、后物理"脉络中承上启下的关键一段。

**论据。** 数字孪生为物理层闭环提供了学术底座。美国国家标准与技术研究院（NIST）2025 年 IECON 会议论文提出基于 IEEE 1451 的智能家居数字孪生框架，通过物理孪生体与数字孪生体的双向信息交换，实现温度的实时监测与控制 ([NIST: IEEE 1451-based Digital Twin Framework](https://www.nist.gov/node/1899736))。当家庭被完整建模，Agent 才具备在物理世界执行的前提——这与"先建虚拟、再控物理"的逻辑高度吻合。

家庭 AI 服务器的三层基础设施已现雏形。**算力层**：端侧 7B–13B 多模态模型开始落地，小米 2025 年 11 月开源 Xiaomi Miloco，以自研端侧视觉语言模型 MiMo-VL-Miloco-7B（7B 参数）结合米家摄像头实时画面，在本地完成视频理解与控制推理，宣称视觉数据不出端、不上云 ([36氪：小米 Miloco](https://m.36kr.com/p/3552738263334017))。**连接层**：Matter 标准持续迭代，Matter 1.4 于 2024-11 发布，2025 年通过 1.4.1/1.4.2 小版本与 Matter 1.5（2025-11）补齐安防摄像头、闭合设备等拼图，并增强跨协议桥接（Zigbee/Z-Wave 经桥接接入）([eefocus：Matter 进展](https://www.eefocus.com/e/1970871.html))；CSA 认证产品从 2023 年底约 1500 款增至 2025 年底超 6500 款——其中 2024 年底已突破 3500 款（另有统计将软件组件计入，2025 年 10 月已超 8400 款）([smartcn：Matter 1.5 生态](https://www.smartcn.cn/?p=347446))。Home Assistant 等开源中枢更以协议无关架构兼容 Zigbee、Wi-Fi、蓝牙 Mesh 与红外/射频，用以接管不同时代品牌的存量家电 ([Arm：本地 LLM 推理](https://developer.arm.com/community/arm-community-blogs/b/internet-of-things-blog/posts/transforming-smart-home-privacy-and-latency-with-local-llm-inference-on-arm-devices))；在硬件形态上，小米 2025 年 11 月开售的智能中控屏即内置 Mesh2.0 网关、毫米波雷达与小爱大模型，可作为家庭 AI 服务器的轻量入口 ([新浪：小米智能中控屏](https://k.sina.com.cn/article_1966122321_7530a551020019b50.html))。**记忆层**：本地向量库承载户型图、设备状态与行为模式，成为隐私不上云的关键——Arm 开发者博客展示在树莓派 5 上以 Ollama 运行本地 LLM，实现 100% 端侧、断网可用的家居自动化 ([Arm：本地 LLM 推理](https://developer.arm.com/community/arm-community-blogs/b/internet-of-things-blog/posts/transforming-smart-home-privacy-and-latency-with-local-llm-inference-on-arm-devices))；开源中枢 Home Assistant 2025 年亦将本地 LLM 深度接入语音与自动化 ([Home Assistant：AI 本地智能家居](https://www.home-assistant.io/blog/2025/09/11/ai-in-home-assistant/))。

能力跃迁已在场景端验证。**感知**方面，毫米波雷达可无感识别跌倒：三思电子 2025 年推出将毫米波雷达集成于吸顶灯的跌倒侦测产品，实测漏报率近 0、误报率约 2%，且不采集人脸、保护隐私 ([今日头条：毫米波跌倒灯](https://www.toutiao.com/article/7554929512669102643)；[人民号：毫米波雷达](https://www.peopleapp.com/rmharticle/30050825590))。**决策**方面，美的"小美 AI 智能体"以空气、水、烹饪、光影、安防、能源六大 Agent 构成"感知—决策—执行"闭环，主动联动空调、新风、净化器 ([腾讯新闻：美的全屋智能](https://view.inews.qq.com/a/20251101A02E7A00))；华为鸿蒙智家智能主机 X2 Pro 强调全本地化部署，单台可支撑千台设备、级联至 2699 节点，数据不出户 ([IT之家：华为 X2 Pro](https://www.ithome.com/0/907/265.htm))。**执行**方面，开源社区正以 MCP 协议打通米家与 Home Assistant 生态，并以 RPA/机械手指等"软件定义"方式控制无 API 的老旧家电。

**分析：核心矛盾——连接标准化与碎片化之战。** 一方面，Matter 正消弭新设备的跨生态壁垒，认证数量陡峭增长（[eefocus](https://www.eefocus.com/e/1970871.html)）；另一方面，据行业观察，家庭存量中非智能/不可联网家电仍占相当比例（占存量家电的绝大多数；行业粗略估计约七成以上，但缺乏统一口径统计），且分属不同时代、品牌与协议，并不兼容 Matter。多家机构渗透数据印证这一结构性落差：奥维云网显示 2024 年白色家电智能产品合计渗透率仅 51.1%、洗碗机 60%，油烟机/洗衣机等品类更低（[新浪/中国消费者报：奥维云网数据](https://finance.sina.cn/2025-05-20/detail-inexeyff3805863.d.html)）；艾瑞咨询称中国智能家居设备家庭渗透率仅约 16%、Statista 更早统计为 14.5%（[艾瑞/同花顺](https://m.10jqka.com.cn/20260313/c675270453.shtml)；[Statista/贤集网](https://www.xianjichina.com/special/detail_527085.html)）——均指向绝大多数家庭与家电设备尚未接入智能网络。学界与产业界对此存在路线分歧：标准化派认为 Matter 终将统一主流设备，[Marketintelo 预测 Matter 设备市场 2025 年 148 亿美元、2034 年 526 亿美元（CAGR 15.1%）](https://marketintelo.com/report/matter-smart-home-device-market)；务实派（多为开源社区与跨生态厂商）则认为，在可预见的未来，"软件定义"（虚拟驱动 + 视觉识别反馈控制 + RPA/机械手指）去整合非智能家电，才是更快落地、也更可能成为"事实中控标准"的路径——Home Assistant 的协议无关架构与小米 Miloco 的跨生态 MCP 桥接正是代表 ([BAAI：小米 Miloco](https://hub.baai.ac.cn/view/50369))。边缘 AI 处理器的算力供给也在支撑这场整合：2025 年边缘 AI 处理器市场约 68.4 亿美元、NPU 占比居首（约 44%），为本地多模态推理提供底座 ([Intelevo：边缘 AI 处理器](https://www.intelevoresearch.com/reports/edge-ai-processor-market/))。

**小结。** 阶段二是家庭 AI 管家从"会说话"到"会动手"的关键一跃：以家庭 AI 服务器为中枢，Matter/多协议连接打通设备、7B 级端侧模型提供本地智能、数字孪生承载空间与记忆，形成感知—决策—执行的本地闭环。其最大障碍不在单点技术，而在于"连接标准化"与"海量存量非智能家电碎片化"之间的拉锯。本章对此持一定倾向性判断：标准化派有 Matter 1.4/1.5 覆盖扩张与头部厂商（华为、小米等）统一接入的支撑，认为时间站在统一标准一侧；但鉴于占存量绝大多数的非智能家电（约七成以上）并不兼容 Matter，务实派（开源社区与跨生态厂商）主张以"软件定义"（虚拟驱动 + 视觉识别反馈控制 + RPA/机械手指）整合才是更快落地、更可能成为"事实中控标准"的路径。综合判断偏向后者——但此属阶段性倾向，最终仍取决于 Matter 渗透速度与存量改造速度的赛跑。

### 关键发现
- 发现1：家庭数字孪生已有标准化学术框架（IEEE 1451 双向信息交换），为物理层闭环提供底座 ([NIST](https://www.nist.gov/node/1899736))。
- 发现2：Matter 认证产品从 2023 年底约 1500 款增至 2025 年底超 6500 款（2024 年底已突破 3500 款），标准化提速但存量碎片化仍存 ([eefocus](https://www.eefocus.com/e/1970871.html)；[smartcn](https://www.smartcn.cn/?p=347446))。
- 发现3：端侧 7B 级多模态模型（小米 MiMo-VL-Miloco-7B）与开源本地 LLM 中枢（Home Assistant / Arm 树莓派）已进入可部署阶段，隐私不上云成共识 ([36氪](https://m.36kr.com/p/3552738263334017)；[Arm](https://developer.arm.com/community/arm-community-blogs/b/internet-of-things-blog/posts/transforming-smart-home-privacy-and-latency-with-local-llm-inference-on-arm-devices))。
- 发现4：感知层以毫米波雷达跌倒检测、视觉识别食材/电器状态为代表，决策—执行闭环由美的、华为等头部厂商落地 ([今日头条](https://www.toutiao.com/article/7554929512669102643)；[腾讯新闻](https://view.inews.qq.com/a/20251101A02E7A00)；[IT之家](https://www.ithome.com/0/907/265.htm))。

### 数据摘要
| 指标 | 数据 | 来源 |
|------|------|------|
| Matter 认证产品数 | 2023底~1500 → 2024底>3500 → 2025底>6500 款 | [eefocus](https://www.eefocus.com/e/1970871.html) |
| Matter 设备市场 | 2025 年 148 亿美元 → 2034 年 526 亿美元（CAGR 15.1%） | [Marketintelo](https://marketintelo.com/report/matter-smart-home-device-market) |
| 边缘 AI 处理器市场 | 2025 年 68.4 亿美元，NPU 占比居首（约 44%） | [Intelevo](https://www.intelevoresearch.com/reports/edge-ai-processor-market/) |
| 端侧模型 | 小米 MiMo-VL-Miloco-7B（7B 多模态）本地部署 | [36氪](https://m.36kr.com/p/3552738263334017) |
| 本地中枢 | Home Assistant + Ollama 本地 LLM，断网可用 | [Home Assistant](https://www.home-assistant.io/blog/2025/09/11/ai-in-home-assistant/) |
| 华为主机 | X2 Pro 全本地化，单台千台设备、级联 2699 节点 | [IT之家](https://www.ithome.com/0/907/265.htm) |

---

## 3. 阶段三：具身智能进家庭——分离式架构、VLA 与灵巧手、3A-3B-3C 渐进路线及 affordance 鸿沟

### 论点

当"大脑"——即以自然语言调度数字工具与边缘设备的 Agent——在家庭中逐步成熟后，管家若要真正完成取饮料、收衣物、搀扶老人等非标准化物理任务，就必须拥有"躯体"。这些任务发生在开放、杂乱、长尾的物理空间，无法仅靠 API 与软件编排解决，须依赖具身智能。然而具身化并非一蹴而就：本框架主张沿"功能级具身（3A）→分布式躯体（3B）→通用具身管家（3C）"的分离式架构渐进落地，而贯穿全程的最大技术鸿沟，是从"数字工具调用"到"物理世界 affordance 理解"的认知跃迁。

### 论据

3A 功能级具身，指为既有的扫地、割草、泳池等家用机器人注入 Agent 能力，使其接受家庭服务器的动态调度，而非执行固定脚本。3B 分布式躯体，则是以服务器作为中央"大脑"调度多台异构机器协作，此时系统价值从"自己动手"转向"精准调度＋异常处理"。3C 通用具身管家，依赖 VLA（视觉-语言-动作）模型与灵巧手，构成通用人形或轮式平台；在分离式架构下，服务器承担类"大脑皮层"的高层规划，机器人端侧承担类"小脑"的低延迟动作控制，二者经低延迟家庭局域网协同，形成"分离式具身智能"。

这一路径已有产业雏形。Figure 于 2025 年 10 月发布通用人形机器人 Figure 03，采用自研 Helix VLA 模型与 3 克级指尖触觉传感，并规划 BotQ 产线达年产 1.2 万台 ([Introducing Figure 03](https://www.figure.ai/news/introducing-figure-03))。其 Helix 系统以 70 亿参数 VLM 为高层主干、8000 万参数动作模型为底层，实现上半身 35 自由度、200Hz 连续控制，并示范了两台机器人零样本协作收纳杂物 ([Helix: A Vision-Language-Action Model for Generalist Humanoid Control](https://www.figure.ai/news/helix))；后续 Helix-02 更让两台人形机器人在无中央调度器的情况下两分钟内协作整理卧室 ([Helix-02 Bedroom Tidy](https://figure.ai/news/helix-02-bedroom-tidy))。学术侧，Physical Intelligence 的 π0 以流匹配将预训练 VLM 拓展为跨本体通用操作策略，达成 50Hz 灵巧控制与叠衣等任务，并直言"叠一件衬衫比赢一局棋更难"，点出莫拉维克悖论 ([π0: A Vision-Language-Action Flow Model for General Robot Control](https://www.pi.website/blog/pi0))。VLA 已被综述确认为具身智能主流架构 ([VLA 架构下的智能体演化](http://www.kjdb.org/CN/10.3981/j.issn.1000-7857.2025.10.00077))。

从"数字工具调用"到"物理世界 affordance 理解"，是第三阶段最难的一跃。门把手可被"拧"、湿杯可被"握"但须控力、地毯边缘可能"绊脚"——这些都要求机器人具备物理常识推理与力控能力，而非仅识别物体类别。学界将之归因于莫拉维克悖论（感知厨房脏乱远难于下棋）与 Sim-to-Real 迁移鸿沟 ([深度｜什么是物理 AI？](https://so.html5.qq.com/page/real/search_news?docid=70000021_3956994044126452))。

### 分析

正方"具身终局论"认为，VLA 已在实验室展现跨本体泛化与多机协作能力，分离式架构（云端/服务器大脑＋端侧小脑）恰契合家庭局域网的现实算力与延迟约束，是家庭管家最可信的技术终局。

反方"时机未到／过度炒作论"则指向冷峻数据：斯坦福《2026 AI 指数报告》显示，机器人在仿真环境家务成功率达 89.4%，但在真实家庭 1000 项任务中仅 12.4% ([美国斯坦福大学发布《2026年AI指数报告》](https://www.news.cn/liangzi/20260417/1d935fe6f2f04c9cb07afe3a38e76db1/c.html))；第三方测算其失败率高达约 88% ([Humanoid Robot Hype Meets an 88% Household Task Fail Rate](https://www.eweek.com/news/humanoid-robots-fail-88-percent-household-tasks/))。与此同时，2025 年全球人形出货约 1.8 万台、同比激增 508%，但智元（约 5200 台）、宇树（超 5500 台纯人形）的出货量主要流向文娱商演、科研教育与数据采集，而非家庭 ([IDC report: China leads the global humanoid robot rise in 2025](https://news.cgtn.com/news/2026-01-24/IDC-report-China-leads-the-global-humanoid-robot-rise-in-2025-1KccOGZyVGM/p.html)；[2026，人形机器人只赢了面子](https://web-origin.lbkrs.com/zh-CN/news/283611721))。成本高企（高端机型售价达十万元级，而 78% 家庭心理价位在千元内）、可靠性不足（有测试指关节平均无故障仅约 8 小时），使瑞银断言其"尚未真正商业化"，台积电魏哲家直言部分演示"无用、只是作秀"，麦肯锡称之为"试验炼狱" ([2026，人形机器人只赢了面子](https://www.tmtpost.com/7961688.html)；[人形机器人：82%用户要家务替代，家庭成功率仅12%，如何破局？](https://www.toutiao.com/article/7637141392241754639/))。行业共识是"工业先于家庭"，C 端爆发待 ROI 突破。

### 小结

具身智能是家庭管家的必然第三阶段，但必须沿 3A→3B→3C 的渐进路线、以分离式架构稳妥下沉。当前产业证据最强处在于工业与商业场景，真实家庭 12.4% 的成功率是须正视的基准线；VLA＋灵巧手＋低延迟局域网构成最具可信度的技术路径，而 affordance 理解与 Sim-to-Real 鸿沟，则是横亘在"表演能力"与"实用能力"之间、短期内难以逾越的核心障碍。

---

## 4. 演进路径的底层逻辑——技术成熟度错配、信任梯度、数据飞轮与阶段跃迁瓶颈

### 论点

"先数字、再连接、后物理"的三阶段演进并非主观偏好，而是由三条结构性约束共同决定的"唯一正确"顺序：**技术成熟度的错配、不可逆的信任梯度、必须逐层累积的数据飞轮**。该路径让每一阶段的商业落地都与对应技术的成熟度同频，避免在不具备条件时过早烧钱。

### 论据

**一、技术成熟度错配决定"分步走"。** 三阶段所依赖的核心技术成熟度差异显著：第一阶段依赖的大语言模型与 AI 智能体已进入规模化应用期——Gartner 2025 年 AI 技术成熟度曲线显示，生成式 AI 已滑入"幻灭的低谷"，而 AI 智能体处于"期望膨胀顶峰"、距生产成熟期约 2–5 年 ([Gartner Hype Cycle for AI 2025](https://gartner.com/en/insights/gartner-hype-cycle))；第二阶段依赖的 IoT 芯片与协议正处于成熟中——边缘 AI 处理器市场 2025 年约 68.4 亿美元、2034 年预计 249.2 亿美元 ([Global Edge AI Processor Market](https://www.intelevoresearch.com/reports/edge-ai-processor-market/))，连接标准 Matter 认证产品从 2023 年底约 1500 款增至 2025 年底 6500 余款、2026 年一季度单季新增超 600 款 ([Matter 协议最新进展](https://m.eefocus.com/e/1970871.html))；第三阶段依赖的通用机器人仍处早期——斯坦福《2026 AI 指数报告》显示，机械臂在 RLBench 仿真中成功率 89.4%，但在真实家庭 1000 项家务中仅 12.4% ([科技日报：斯坦福2026 AI指数报告](https://www.news.cn/liangzi/20260417/1d935fe6f2f04c9cb07afe3a38e76db1/c.html))。技术成熟度的"阶梯状"分布使同步推进三阶段在商业上不可行。

**二、信任梯度要求"不可逆的心理建设"。** 用户授权的敏感程度逐级递增：先交"日程/偏好数据"（低风险）→再交"家门控制权"（摄像头、API，高风险）→最后接受机器人在物理空间活动（最高风险）。隐私焦虑是真实且普遍的阻力：Copeland 2024 智能家居隐私调查显示，担忧数据隐私的房主比例从 2022 年的 23% 升至 2024 年的 27%，52% 的用户根本不知智能设备如何收集数据 ([Copeland Smart Home Data Privacy Survey](https://www.achrnews.com/articles/164019-copeland-survey-looks-at-views-on-smart-home-products))；三星欧洲研究称近 89% 的受访者对隐私表示担忧 ([Samsung Privacy Blind Spot Study](https://news.samsung.com/uk/privacy-blind-spot-could-stall-ais-future-in-uk-homes-says-new-study))；江苏省消保委调查更显示 42.60% 的智能音箱用户怀疑被监听或录音 ([江苏智能家居家电消费调查](https://jsnews.jschina.com.cn/jsyw/202601/t20260122_s6971c2b2e4b064219d217b0d.shtml))。信任只能自下而上累积，无法跳跃。

**三、数据飞轮必须"逐层闭环"。** 阶段一积累偏好数据、阶段二积累环境数据（设备状态、空间布局）、阶段三积累物理交互数据（操作成功率、力控反馈）。缺前两阶段数据，具身机器人进家庭如同"瞎子+失忆者"——这恰被莫拉维克悖论与 Sim-to-Real 鸿沟印证：高层规划对机器容易、低层感知运动极难 ([Moravec's Paradox and the Robot Olympics](http://www.physicalintelligence.company/blog/olympics))；贝恩 2025 技术报告亦指出灵巧操作与精细力控仍处较早阶段 ([Why Robots Struggle With Common Sense](https://www.robotaigeek.com/ai-robotics/how-ai-robots-work/why-robots-struggle-common-sense-deployment-gap))。MIT CSAIL 的 RialTo 用"数字孪生+真实到仿真再到真实"训练，较模仿学习提升 67%，但仍需约 3 天训练且难模拟柔性物体 ([Precision Home Robots: Real-to-Sim-to-Real](https://news.mit.edu/2024/precision-home-robotics-real-sim-real-0731))，说明物理数据稀缺是硬约束。

**四、三阶段跃迁的关键瓶颈与破局。**

| 跃迁 | 关键瓶颈 | 外部实证 | 破局路径 |
|------|----------|----------|----------|
| 一→二 | 连接协议碎片化（大量家电无 API）；隐私恐惧致不敢装摄像头 | Matter 认证 2025 破 6500 款但仍非全覆盖 ([Matter 协议最新进展](https://m.eefocus.com/e/1970871.html)) | Matter/Thread 1.4 统一凭证共享 ([The Matter Standard in 2026](https://matter-smarthome.de/en/development/the-matter-standard-in-2026-a-status-review/))；视觉反馈控制（读屏幕/指示灯状态实现无 API 控制）；端侧本地计算消除隐私焦虑 ([Matter+边缘AI](https://www.esmchina.com/news/13337.html)) |
| 二→三 | 莫拉维克悖论（高层易、低层难）；家庭环境非标 | 真实家务成功率仅 12.4% ([科技日报](https://www.news.cn/liangzi/20260417/1d935fe6f2f04c9cb07afe3a38e76db1/c.html)) | 家庭 AI 服务器先建高精度语义三维地图（数字孪生）；机器人先在仿真训练（Sim-to-Real）；优先轮式+单臂半人形切入 ([石景山人形机器人数据训练中心](https://new.qq.com/rain/a/20260511A0432X00?refer=cp_1009)) |

### 分析

三条约束相互强化：技术成熟度决定"能做什么"，信任梯度决定"用户敢交什么"，数据飞轮决定"机器能学什么"，三者都指向同一结论——跳阶既不经济也不可行。需呈现多元观点：**"直接卖机器人派"**（如 Tesla、Figure、宇树）认为具身是终局、可跨越式投入，但其商业化仍受 12.4% 成功率与十万元级成本的硬约束 ([2026，人形机器人只赢了面子](https://www.huxiu.com/article/4852535.html?f=rss))；**"云优先派"**主张集中算力更快，但隐私调研表明用户对云端收集高度抗拒。主流证据更支持"软件先行、逐步下沉"的节奏。

### 小结

三阶段路径是当前技术成熟度、用户心理与数据条件共同约束下的唯一经济可行顺序。一→二的核心矛盾是协议碎片化与隐私恐惧，可由 Matter/Thread、视觉反馈控制与端侧计算缓解；二→三的核心矛盾是莫拉维克悖论与非标环境，可由数字孪生、Sim-to-Real 与轮式+单臂形态渐进突破。路径本身不可逆，但每个瓶颈都有可验证的破局杠杆。

---

## 5. 终局形态：分离式具身智能与即插即用的家庭机器人商业落地规律

### 论点：终局是"分离式"而非"一体式"

家庭 AI 管家的终局并非一台"全能机器人"，而是**大脑（家庭服务器）与手脚（具身机器人）分离**的分布式系统。在"先数字、再连接、后物理"框架下，最稳健的形态是：推理与记忆驻留本地服务器，机器人本体退化为可替换、可即插即用的移动终端。这契合"先无形管家、后配躯体"的规律。

### 论据一：分布式架构已现雏形——大脑、神经、手脚三层分离

分布式家庭智能体的第一层是**家庭 AI 服务器（大脑）**，负责长程记忆与多模态推理。2026 年已出现本地"家庭 AI 中枢"：卧安 AI Hub、萤石 EZVIZ AI CoreX（64T）、摩尔线程 AICUBE（50TOPS + 私有云）均把智能体下沉本地、数据不出户 ([卧安机器人 AI Hub 支持 OpenClaw](https://www.onero.cn/news/19))([萤石发布 EZVIZ AI CoreX](https://so.html5.qq.com/page/real/search_news?docid=70000021_28469eb36e853152))([摩尔线程 AICUBE 家庭中枢](https://www.toutiao.com/article/7641847215481078291))。开源 FOFOCA 更拆为四层：独立边缘服务器运行向量库、关系库与视频存储，**记忆与推理不依赖板载硬件**，本体仅由 ESP32（控制）与树莓派 5（板载脑）构成 ([FOFOCA 四层开源架构](https://developer.espressif.com/blog/2026/05/fofoca-esp32-ai-robot/))。

（注："十年记忆、万亿参数"为终局愿景刻画，当前产品以数十 TOPS 本地算力起步，规模与年限仍属前瞻设想，本文据实引用已落地的算力与存储规格。）

第二层**环境接口（神经与反射）**：全屋传感器与可控 IoT 构成感知与响应层。Matter 协议 2025 年底认证 6500+ 款设备、1.4 版补齐安防摄像头 ([Matter 1.4 进展](https://www.eefocus.com/e/1970871.html))；Google 把 Gemini 部署到逾 8 亿台既有设备，以"智能"而非新硬件为核心 ([Google 部署 Gemini 至 8 亿设备](http://www.techbuzz.ai/articles/google-deploys-gemini-ai-across-800m-smart-home-devices))。第三层是**移动代理（手脚）**：1 至多台具身机器人负责物理操作（Figure 03、宇树、特斯拉 Optimus 等）。

### 论据二：即插即用——智能不因本体损坏而消失

分离式架构的关键收益是**智能的持久化与可迁移**：FOFOCA 证明，机器人关机或失联时向量记忆、日志与视频仍完整保留在边缘服务器 ([FOFOCA 四层开源架构](https://developer.espressif.com/blog/2026/05/fofoca-esp32-ai-robot/))。傅利叶"具身之家"给出"数字孪生地图"雏形：其语义场景图由"物理地图"（坐标、避障）与"语义地图"（功能、物品）双层构成，支持动态更新与经验积累 ([傅利叶具身之家语义地图](https://view.inews.qq.com/a/20260718A03BCA00))。Kairos-Homeworld 开源 30 万套中国住宅户型与 5000 个可交互 3D 场景，把家庭空间数字孪生作为训练底座 ([Kairos-Homeworld 数字孪生](https://new.qq.com/rain/a/20260605A05O4E00?refer=cp_1009))。由此可见，**新机器人接入家庭时，下载"家庭记忆"+"数字孪生地图"即可即插即用具身化**——本体损而智能不灭。

### 论据三：商业落地规律——无形管家先行，躯体随后

参与者清晰分化为两派。**"软件先行派"**以 Amazon 与 Google 为代表：Alexa+ 于 2025 年 2 月发布、具 agentic 编排能力 ([Introducing Alexa+](https://www.aboutamazon.com/news/devices/new-alexa-generative-artificial-intelligence))；Google 在 I/O 2026 暂停新硬件、全力押注 Gemini for Home，明确"智能优先、设备其次" ([Google I/O 2026 软件优先](https://www.techinsights.com/ja/node/61846))——以最低切换成本把用户锁进"无形管家"的服务与数据闭环。**"具身押注派"**（Tesla、Figure、宇树）：特斯拉改造弗里蒙特工厂为 Optimus 产线、目标成本 2–3 万美元 ([特斯拉 Optimus 产能路线图](https://tesorb.com/optimus-progress-tracker))；Figure 在宝马约 25 美元/小时、CEO 提每月 600 美元租赁进家庭 ([Figure 商业化数据](https://analysis-atlas.com/research/humanoid-robotics-commercialization-market))([Figure CEO 月租 600 美元](https://new.qq.com/rain/a/20260506A06D8D00?refer=cp_1009))；宇树单价由 2023 年约 8.5 万降至 2025 年约 2.5 万美元 ([宇树价格曲线](https://analysis-atlas.com/research/humanoid-robotics-commercialization-market))。

**成本与节奏的数据**揭示分歧的现实基础：2026 年工业级人形均价约 3 万美元，家庭场景更晚、价格不同 ([人形机器人价格 2026](https://www.techtimes.com/articles/318157/20260610/humanoid-robot-prices-near-30000beijing-factorys-500000-year-plan-may-halve-cost-buyers-lag.htm))。Omdia 指出落地路径"先经工业、家庭在后" ([TechTimes 引 Omdia](https://www.techtimes.com/articles/318157/20260610/humanoid-robot-prices-near-30000beijing-factorys-500000-year-plan-may-halve-cost-buyers-lag.htm))；智元 CTO 彭志辉同样判断"先工业后家庭"、家庭机器人率先以 RaaS 订阅落地、约 5 年进家庭 ([智元彭志辉谈落地路径](https://jnz.cs.com.cn/app/html/jnz/119980.html))。斯坦福 2026 AI 指数显示真实家庭家务成功率仅 12.4%，印证 Sim-to-Real 鸿沟是直接卖家用机器人的瓶颈 ([斯坦福 2026 AI 指数](https://www.tmtpost.com/7961688.html))。

### 分析：两派之争的本质与分离式架构的调和

表面看，软件派与具身派是路线对立；深层看，**分离式架构让两者殊途同归**。软件先行派掌控的"大脑"一旦建立便具强黏性与高迁移成本；具身派押注的"躯体"则在规模制造下快速商品化、成本骤降。当本体成为可替换终端、记忆与数字孪生驻留服务器，"先无形后有形"便技术可行、商业最优：用户先依赖"管家服务"，再以获得"有形躯体"为增量升级，避免早期直接采购昂贵且不成熟的机器人。

**反方观点**认为具身终局无法绕过硬件：Figure、特斯拉视本体即护城河，RaaS/租赁能否跨过可靠性与合规门槛仍待验证 ([Figure 月租方案待验证](https://new.qq.com/rain/a/20260506A06D8D00?refer=cp_1009))；海尔周云杰判断家政机器人 2–3 年规模化"前夜"，强调"群体智能"协同与"卖服务"转型 ([海尔周云杰专访](https://so.html5.qq.com/page/real/search_news?docid=70000021_98769aeaa0508552))。分离式架构不消除硬件挑战，只是把"智能"与"躯体"的风险解耦，可靠性与法规仍是进家庭前的硬约束。

### 小结

家庭 AI 管家的终局是**分离式具身智能**：本地服务器为持久大脑，全屋传感与 IoT 为神经反射，具身机器人为可插拔手脚；本体损坏智能不灭，新机器人凭"家庭记忆 + 数字孪生地图"即插即用。商业落地遵循"无形管家先行、有形躯体随后"，比直接卖昂贵笨拙机器人更合算力下沉与成本曲线。两派路线非零和：分离式架构下，软件沉淀的大脑与规模化的躯体终将融合，家庭拐点取决于可靠性、成本与杀手级家务场景的成熟。

---

## 结论

回到引言之问：家庭 AI 管家应如何演进？本报告基于 2024–2026 年产业与学术证据给出明确判断——"先数字、再连接、后物理"是当前技术、心理与数据约束下的唯一经济可行顺序。三阶段成熟度呈清晰梯度：阶段一软件数字管家已规模商用，Alexa+、Gemini for Home 及美的"小美 AI"、华为"小艺管家"等已落地（[美的全屋智能](https://new.qq.com/rain/a/20251103A051ES00)）；阶段二边缘中枢加速成型，Matter 认证产品从 2023 年底约 1500 款增至 2025 年底超 6500 款（[eefocus](https://www.eefocus.com/e/1970871.html)），端侧 7B 多模态模型进入可部署阶段；阶段三具身智能仍处前瞻，真实家庭家务成功率仅 12.4%（[斯坦福 2026 AI 指数](https://www.news.cn/liangzi/20260417/1d935fe6f2f04c9cb07afe3a38e76db1/c.html)），主流共识为"工业先于家庭"。

路径底层逻辑可归纳为三条结构性约束：其一，技术成熟度错配——Gartner 显示 AI 智能体距生产成熟约 2–5 年、通用机器人仍处早期（[Gartner](https://gartner.com/en/insights/gartner-hype-cycle)）；其二，不可逆信任梯度——隐私担忧普遍，52% 用户不知设备如何收集数据（[Copeland 调查](https://www.achrnews.com/articles/164019-copeland-survey-looks-at-views-on-smart-home-products)）；其三，数据飞轮须逐层闭环。共性瓶颈则贯穿始终：连接协议碎片化、隐私焦虑与莫拉维克悖论（感知运动远难于高层规划，[Physical Intelligence](http://www.physicalintelligence.company/blog/olympics)）。

综上，家庭管家的终局是"分离式具身智能"——本地服务器为持久大脑、具身机器人为可插拔手脚，遵循"无形管家先行、有形躯体随后"的商业规律（[FOFOCA 四层开源架构](https://developer.espressif.com/blog/2026/05/fofoca-esp32-ai-robot/)）。路径不可逆，但每个瓶颈均有可验证的破局杠杆；未来研究应聚焦数字孪生训练底座、Sim-to-Real 迁移与 RaaS 订阅模型的家庭化验证。

---

## 参考文献

### 一、阶段一：软件切入的 AI 数字管家

- Amazon. (2025). Introducing Alexa+, the next generation of Alexa. Amazon. [链接](https://www.aboutamazon.com/news/devices/new-alexa-generative-artificial-intelligence)
- Google. (2025). Gemini for Home: The helpful home gets an AI upgrade. Google. [链接](https://blog.google/products-and-platforms/devices/google-nest/gemini-for-home-launch/)
- DigitalTrends. (2025). 4 reasons why you should really pay attention to Amazon's Alexa+. DigitalTrends. [链接](https://www.digitaltrends.com/home/4-reasons-why-you-should-really-pay-attention-to-amazons-alexa-assistant/)
- 腾讯新闻. (2025). 美的给小米上强度：发力全屋智能. 腾讯新闻. [链接](https://new.qq.com/rain/a/20251103A051ES00)
- 中国经济周刊. (2025). 华为鸿蒙智家新品发布："品价比"拉满. 中国经济周刊. [链接](https://www.ceweekly.cn/company/2025/1224/486538.html)
- 今日头条/网易. (2025). 2025年中国智家市场观察：全维智能与生态重构. 今日头条. [链接](https://www.toutiao.com/article/7597744242563252776/)
- MarketsandMarkets. (2025). AI Agents Market Size, Share, Forecast & Growth Drivers. MarketsandMarkets. [链接](https://www.marketsandmarkets.com/blog/ICT/ai-agents-market)
- Lee, E. (2024). Towards Ethical Personal AI Applications: AI Assistants with Long-Term Memory. MIT (arXiv:2409.11192). [链接](https://arxiv.org/html/2409.11192v1)
- TechKV. (2025). Alexa+ Launches With AI Superpowers and Built-In Ads. TechKV. [链接](https://techkv.com/amazon-alexa-plus-ai-ads-launch/)
- 搜狐. (2025). 智能家居藏"数据暗门"，用户隐私谁来守护. 搜狐. [链接](https://www.sohu.com/a/994830648_122014422)
- 河北北方学院学报(社科). (2025). 窥见隐私——智能家居用户隐私忧虑的多维影响因素分析. 河北北方学院学报. [链接](https://www.hbskw.com/p/83501.html)
- 网易. (2025). 2025年中国智家市场观察：全维智能与生态重构（网易原稿）. 网易. [链接](https://www.163.com/dy/article/KDK0PNO20514D3UH.html)
- agentmarketcap.ai. (2026). AI Agent Market Size Reality Check 2026. agentmarketcap.ai. [链接](https://agentmarketcap.ai/blog/2026/04/08/ai-agent-market-size-reality-check-2026)
- 新华报业网. (2025). 华为鸿蒙智家升级小艺管家. 新华报业网. [链接](https://www.xhby.net/content/s69492442e4b0e65d832f0ce4.html)

### 二、阶段二：家庭 AI 服务器中枢

- NIST (Song, Y. 等). (2025). IEEE 1451-based Digital Twin Framework for Real-Time Monitoring and Control of Smart Homes. NIST / IEEE IECON. [链接](https://www.nist.gov/node/1899736)
- Home Assistant. (2025). Building the AI-powered Local Smart Home. Home Assistant. [链接](https://www.home-assistant.io/blog/2025/09/11/ai-in-home-assistant/)
- Arm. (2025). Transforming Smart Home Privacy and Latency with Local LLM Inference on Arm Devices. Arm. [链接](https://developer.arm.com/community/arm-community-blogs/b/internet-of-things-blog/posts/transforming-smart-home-privacy-and-latency-with-local-llm-inference-on-arm-devices)
- 电子发烧友. (2025). 智能家居互联统一标准最新进展：Matter 1.4 与生态新动向. 电子发烧友. [链接](https://www.eefocus.com/e/1970871.html)
- 智装天下. (2025). 连接标准联盟宿为民博士：Matter 标准迭代升级 生态图谱焕新. 智装天下. [链接](https://www.smartcn.cn/?p=347446)
- Marketintelo. (2025). Matter Smart Home Device Market Research Report 2034. Marketintelo. [链接](https://marketintelo.com/report/matter-smart-home-device-market)
- Intelevo Research. (2025). Global Edge AI Processor Market. Intelevo Research. [链接](https://www.intelevoresearch.com/reports/edge-ai-processor-market/)
- 36氪. (2025). 小米放出首个 AI 大招 Xiaomi Miloco. 36氪. [链接](https://m.36kr.com/p/3552738263334017)
- 北京智源研究院. (2025). 小米给智能家居做了个"大模型大脑"(Miloco). 北京智源研究院. [链接](https://hub.baai.ac.cn/view/50369)
- IT之家. (2025). 华为鸿蒙智家智装组合与智能主机 X2 Pro. IT之家. [链接](https://www.ithome.com/0/907/265.htm)
- 新华网. (2025). 华为鸿蒙智家亮相 AWE2025. 新华网. [链接](https://www.news.cn/tech/20250321/ae3721b1b7a645efac52de26e3929f7d/c.html)
- 中国网. (2025). 美的发布全屋智能新战略. 中国网. [链接](https://business.china.com.cn/2025-08/04/content_43192614.html)
- 腾讯新闻. (2025). 美的全屋智能惊艳亮相 小美 AI 智能体. 腾讯新闻. [链接](https://view.inews.qq.com/a/20251101A02E7A00)
- 新浪. (2025). 小米智能中控屏开售. 新浪. [链接](https://k.sina.com.cn/article_1966122321_7530a551020019b50.html)
- 今日头条. (2025). 三思跌倒侦测护眼吸顶灯（毫米波雷达）. 今日头条. [链接](https://www.toutiao.com/article/7554929512669102643)
- 人民号/厦门日报. (2025). 毫米波雷达居家养老"神器". 人民日报客户端. [链接](https://www.peopleapp.com/rmharticle/30050825590)
- 凤凰网. (2025). 毫米波雷达如何解决独居老人跌倒难题. 凤凰网. [链接](https://i.ifeng.com/c/8oXuiKus6mt)
- Logiciel. (2025). Digital Twins for Smart Homes (2025). Logiciel. [链接](https://logiciel.io/blog/digital-twins-predictive-design-smart-homes-2025)
- 中国消费者报/新浪. (2025). 聚焦智慧家居系列报道（奥维云网智能家电渗透率数据）. 新浪. [链接](https://finance.sina.cn/2025-05-20/detail-inexeyff3805863.d.html)
- 艾瑞咨询/同花顺. (2026). 艾瑞观察——中国智能家居行业正从设备互联迈向空间智能新时代. 同花顺. [链接](https://m.10jqka.com.cn/20260313/c675270453.shtml)
- Statista/贤集网. (2025). AI 发展趋势下智能家居突破与传统行业影响. 贤集网. [链接](https://www.xianjichina.com/special/detail_527085.html)
- 国际电子商情. (2025). Matter+边缘AI：泰凌重塑无界智联家居新生态. 国际电子商情. [链接](https://www.esmchina.com/news/13337.html)
- matter-smarthome.de. (2026). The Matter Standard in 2026 – A Status Review. matter-smarthome.de. [链接](https://matter-smarthome.de/en/development/the-matter-standard-in-2026-a-status-review/)

### 三、阶段三：具身智能进家庭

- Figure AI. (2025). Introducing Figure 03. Figure AI. [链接](https://www.figure.ai/news/introducing-figure-03)
- Figure AI. (2025). Helix: A Vision-Language-Action Model for Generalist Humanoid Control. Figure AI. [链接](https://www.figure.ai/news/helix)
- Figure AI. (2025). Helix-02 Bedroom Tidy. Figure AI. [链接](https://figure.ai/news/helix-02-bedroom-tidy)
- Black, K. 等 (Physical Intelligence). (2024). π0: A Vision-Language-Action Flow Model for General Robot Control. Physical Intelligence (arXiv:2410.24164). [链接](https://www.pi.website/blog/pi0)
- 新华网/斯坦福 HAI. (2026). 美国斯坦福大学发布《2026年AI指数报告》. 新华网. [链接](https://www.news.cn/liangzi/20260417/1d935fe6f2f04c9cb07afe3a38e76db1/c.html)
- eWeek. (2026). Humanoid Robot Hype Meets an 88% Household Task Fail Rate. eWeek. [链接](https://www.eweek.com/news/humanoid-robots-fail-88-percent-household-tasks/)
- IDC/CGTN. (2026). IDC Report: China Leads the Global Humanoid Robot Rise in 2025. CGTN. [链接](https://news.cgtn.com/news/2026-01-24/IDC-report-China-leads-the-global-humanoid-robot-rise-in-2025-1KccOGZyVGM/p.html)
- 蓝鲸财经(转钛媒体). (2026). 2026，人形机器人只赢了面子. 蓝鲸财经. [链接](https://web-origin.lbkrs.com/zh-CN/news/283611721)
- 《科技导报》. (2025). VLA 架构下的智能体演化：从机理建构到应用拓展. 科技导报. [链接](http://www.kjdb.org/CN/10.3981/j.issn.1000-7857.2025.10.00077)
- 腾讯新闻/腾讯科技. (2025). 深度｜什么是物理 AI？ 腾讯新闻. [链接](https://so.html5.qq.com/page/real/search_news?docid=70000021_3956994044126452)
- 钛媒体. (2026). 2026，人形机器人只赢了面子. 钛媒体. [链接](https://www.tmtpost.com/7961688.html)
- 今日头条. (2026). 人形机器人：82%用户要家务替代，家庭成功率仅12%，如何破局？ 今日头条. [链接](https://www.toutiao.com/article/7637141392241754639/)

### 四、演进底层逻辑、隐私与终局形态

- Gartner. (2025). Gartner Hype Cycle for AI 2025. Gartner. [链接](https://gartner.com/en/insights/gartner-hype-cycle)
- Copeland / ACH&R News. (2024). Copeland Smart Home Data Privacy Survey. ACH&R News. [链接](https://www.achrnews.com/articles/164019-copeland-survey-looks-at-views-on-smart-home-products)
- Samsung News. (2025). Privacy Blind Spot Could Stall AI's Future in UK Homes. Samsung News. [链接](https://news.samsung.com/uk/privacy-blind-spot-could-stall-ais-future-in-uk-homes-says-new-study)
- 交汇点新闻/江苏省消保委. (2026). 八成以上受访者满意，你的智能家居家电好用吗？ 交汇点新闻. [链接](https://jsnews.jschina.com.cn/jsyw/202601/t20260122_s6971c2b2e4b064219d217b0d.shtml)
- Physical Intelligence. (2025). Moravec's Paradox and the Robot Olympics. Physical Intelligence. [链接](http://www.physicalintelligence.company/blog/olympics)
- RobotAI Geek / Bain & Company. (2025). Why Robots Struggle With Common Sense — and Why That Matters. RobotAI Geek. [链接](https://www.robotaigeek.com/ai-robotics/how-ai-robots-work/why-robots-struggle-common-sense-deployment-gap)
- MIT News / CSAIL. (2024). Precision Home Robots Learn With Real-to-Sim-to-Real. MIT News. [链接](https://news.mit.edu/2024/precision-home-robotics-real-sim-real-0731)
- 腾讯新闻. (2026). 数智赋能发展 机器人在这里"上学". 腾讯新闻. [链接](https://new.qq.com/rain/a/20260511A0432X00?refer=cp_1009)
- 虎嗅. (2026). 2026，人形机器人只赢了面子. 虎嗅. [链接](https://www.huxiu.com/article/4852535.html?f=rss)
- 卧安机器人/onero. (2026). 卧安机器人 AI Hub 支持 OpenClaw. 卧安机器人. [链接](https://www.onero.cn/news/19)
- 萤石/腾讯. (2026). 萤石发布 EZVIZ AI CoreX. 腾讯. [链接](https://so.html5.qq.com/page/real/search_news?docid=70000021_28469eb36e853152)
- 摩尔线程/头条. (2026). 摩尔线程 AICUBE 家庭中枢. 今日头条. [链接](https://www.toutiao.com/article/7641847215481078291)
- Espressif. (2026). FOFOCA 四层开源架构. Espressif. [链接](https://developer.espressif.com/blog/2026/05/fofoca-esp32-ai-robot/)
- 腾讯. (2026). 小湃 ClawStation 分布式 AI. 腾讯. [链接](https://new.qq.com/rain/a/20260630A025ZD00?refer=cp_1009)
- TechBuzz. (2025). Google Deploys Gemini AI Across 800M Smart Home Devices. TechBuzz. [链接](http://www.techbuzz.ai/articles/google-deploys-gemini-ai-across-800m-smart-home-devices)
- TechInsights. (2026). Google I/O 2026 软件优先. TechInsights. [链接](https://www.techinsights.com/ja/node/61846)
- tesorb. (2026). 特斯拉 Optimus 产能路线图. tesorb. [链接](https://tesorb.com/optimus-progress-tracker)
- 钛媒体. (2026). 特斯拉 Optimus 量产供应链. 钛媒体. [链接](https://www.tmtpost.com/agent/ai-article/18508)
- Analysis Atlas. (2026). Humanoid Robotics Commercialization Market (Figure 商业化数据 / 宇树价格曲线). Analysis Atlas. [链接](https://analysis-atlas.com/research/humanoid-robotics-commercialization-market)
- TechTimes. (2026). Humanoid Robot Prices Near $30,000 (引 Omdia). TechTimes. [链接](https://www.techtimes.com/articles/318157/20260610/humanoid-robot-prices-near-30000beijing-factorys-500000-year-plan-may-halve-cost-buyers-lag.htm)
- 腾讯. (2026). Figure CEO 月租 600 美元. 腾讯. [链接](https://new.qq.com/rain/a/20260506A06D8D00?refer=cp_1009)
- 中证网. (2026). 智元彭志辉谈落地路径. 中证网. [链接](https://jnz.cs.com.cn/app/html/jnz/119980.html)
- 腾讯/网易. (2026). 傅利叶具身之家语义地图. 腾讯. [链接](https://view.inews.qq.com/a/20260718A03BCA00)
- 腾讯. (2026). Kairos-Homeworld 数字孪生. 腾讯. [链接](https://new.qq.com/rain/a/20260605A05O4E00?refer=cp_1009)
- 腾讯. (2026). 海尔周云杰专访. 腾讯. [链接](https://so.html5.qq.com/page/real/search_news?docid=70000021_98769aeaa0508552)

---

> 本报告由 AI 深度研究团队生成，重要决策请经专业人员核验。所有引用来源请用户在重要场景下二次核验时效性与真实性。
