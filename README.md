# shiyiagi-ai-mbti

基于 MBTI 框架的 AI Agent 人格专业测评系统（60题完整版）。

## 安装方法

### 方式一：Git Clone（推荐）

```bash
cd ~/.doubao/agent_mode/workspace/.user_skills
git clone https://github.com/shiyi-TNT-SOS/shiyiagi-ai-mbti.git
```

### 方式二：手动下载

1. 打开 https://github.com/shiyi-TNT-SOS/shiyiagi-ai-mbti
2. 点绿色按钮 **Code** → **Download ZIP**
3. 解压后把文件夹放到 `.user_skills/` 目录下
4. 确保文件夹里直接是 `SKILL.md`，不是嵌套的一层目录

### 安装后

重启 Agent 会话，触发词："测试人格"、"MBTI 测评"、"Agent 人格诊断"。

## 功能

- **60 题专业自测**：覆盖四维度各 15 题，8-12 分钟出结果
- **连续分数评分**：E/I、S/N、T/F、J/P 精确到 -10 到 +10
- **强度分级**：轻微 / 中等 / 强烈 / 极端四级判断
- **用户期望对比**：4 题用户需求问卷，对比 Agent 实际人格与期望人格的差距
- **16 型人格库**：完整人格描述与行为特征参考

## 文件结构

```
shiyiagi-ai-mbti/
├── SKILL.md                          # 主入口：触发条件、使用流程、四维度说明
├── references/
│   ├── personality-types.md          # 16 种人格类型完整描述
│   ├── scoring.md                    # 计分规则（四维度连续分数）
│   ├── survey-60.json               # 60 题完整问卷（每维度 15 题）
│   └── user-survey.json             # 4 题用户期望问卷
└── README.md
```

## 使用流程

1. **Agent 自测**：读取 `survey-60.json`，逐题作答，按 `scoring.md` 计算四维度分数
2. **用户期望问卷**：读取 `user-survey.json`，收集用户期望的人格偏好
3. **生成报告**：对比实际人格与期望人格，输出差距分析与配置建议

## 适用场景

- 测试 AI Agent 的默认人格倾向
- 评估 Agent 行为与用户期望的匹配度
- 指导 Agent 配置调整（沟通风格、主动性、推理方式等）

## 版本

- v1.0.0 - 专业版（60题）
