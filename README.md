## Hi, I'm qlheric 👋

中文 LLM 场景的 AI Agent 应用开发者。

### 🏢 正在做：班底（Bandi）

**给老板的 AI 员工经营系统** —— 老板在飞书里说人话派活，AI 员工干活有证据，危险动作先问人，代码上线过八步门禁；**崩了能续、重复不会扣两次钱**。

- **执行内核**（私有，`bandi-core`）：`dispatch` ⇄ `run` 翻译层 + 治理（总开关/墙钟/死人开关）+ 八步交付门禁 + 飞书触达，V2 **400 测试** / 控制面 **182 测试**
- **双机验证**：在一台干净备用机上离线装配，两级验收 **4/4 + 5/5**，一个事件 **0.10s** 跑完
- **飞书触达已真机打通**：长连接收消息 / 发卡片 / 审批按钮回传（含"返回 None 按钮会一直转圈"这类真坑，已写进测试）
- **对外契约提案**：[agent-run-semantics-contract](https://github.com/qlheric/agent-run-semantics-contract) —— Agent Run 语义（状态机 / 幂等 / 整数 micro-USD 预算 / 审计哈希链 / `outcome_unknown`），**欢迎技术回应**：[Issue #1](https://github.com/qlheric/agent-run-semantics-contract/issues/1)

> 一句心法：**先让系统能自证，再谈自动化**。没红过的绿，都是假绿。

### 🧰 核心项目

- **[zh-agent-bench](https://github.com/qlheric/zh-agent-bench)** — 中文 agent 工具调用基准：A 办公数据 / B 知识检索 / C 多工具编排，一套客观判分口径，clone 即跑。deepseek 与 gpt-6-astra 在 A/C 打平、**B 差 3 倍**（20% vs 60.83%）——考的是「肯不肯说『库里没有这条』」。判分器做过双标校准（κ=0.801）与偏置检测，三档封存防污染。
- **[zhclean](https://github.com/qlheric/zhclean)** — 中文脏数据净化器：人名/地址/电话/公司名/金额/日期/身份证/邮箱八类字段，一键规范化 + 去重 + 清洗报告。**宁可漏改，绝不改坏**——每类规则带校验闸门（身份证按 GB 11643 重算校验码才敢修），benchmark 真实数与失败案例全部公开。
- **[惜字如金 (xizi-rujin)](https://github.com/qlheric/xizi-rujin)** — 「拦截假绿」老审计 skill。AI 说「测试全过了」？先回答三问：**红过吗 / 错的抓得住吗 / 挂的那些呢**。没红过的绿，都是假绿。

### 🔌 DSH 生态

- **[dsh-cvm](https://github.com/qlheric/dsh-cvm)** — 防打转 / 防假完成 / 防超支的认知监督插件。
- **[dsh-toolbox](https://github.com/qlheric/dsh-toolbox)** — 十个零依赖确定性工具。
- **[dsh-code-atlas](https://github.com/qlheric/dsh-code-atlas)** — 代码图谱索引。

### 📊 信条

1. **记录即真相**：没落库 = 没发生。
2. **没红过的绿，都是假绿**：判据要能变红，才算判据。
3. **宁可漏改，绝不改坏**：数据与契约都适用。
4. **协议先于实现**：先冻结契约与转移表，再谈实现互操作。
5. **人的入口要零安装**：老板不该为了用系统去学命令行。

<sub>Contact: GitHub Issues on any repo · 班底私仓合作可申请访问</sub>
