# HR.skill

<div align="center">

> *"感谢您对我司的关注与支持。经过慎重考虑，我们决定推进与岗位需求更为匹配的候选人。"*

> *"Thank you for your interest in this position. After careful consideration, we have decided to move forward with other candidates whose qualifications more closely align with our current needs."*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![AgentSkills](https://img.shields.io/badge/AgentSkills-Standard-green)](https://agentskills.io)

<br>

你投出去一百封简历，回来九十九封拒信和一封已读不回。<br>
每封拒信都措辞完美，热情洋溢，没有任何信息量。<br>
你问为什么被拒，HR说"综合考量"。<br>
你问能不能给反馈，HR说"我们会保留您的简历以备后续机会"。<br>
然后你再也没有收到任何消息。<br>

**现在轮到你了。**

<br>

召唤 HR.skill，用它的语气回复别人，<br>
生成一封措辞完美、废话连篇、令人心碎的拒信，<br>
或者扮演HR回答任何问题——然后什么都不说清楚。

[功能](#功能) · [安装](#安装) · [使用示例](#使用示例) · [拒信博物馆](#拒信博物馆) · [自定义Persona](#自定义-hr-persona) · [**English**](README_EN.md)

</div>

---

## 功能

### 拒信生成器
输入岗位名 + 候选人名字，输出一封：
- 措辞温暖但无情的拒信
- 中文版 / 英文版 / 双语版任选
- 强调"您的背景非常优秀"同时拒绝你
- 附赠"保留简历"空头支票

### 开人通知生成器
输入员工姓名 + 岗位，输出一封：
- 把裁员说成"战略调整"的通知
- 强调"和你个人表现无关"（无论是不是真的）
- 赔偿细节永远"另行沟通"
- 结尾祝你"前程似锦"

或者进入**开人现场模拟**——HR逐步还原那场你永远不想经历的谈话：从假装正常寒暄，到"我们今天约你来是有件事情要告诉你"，全程一字不差。

支持风格：
| 风格 | 关键词 |
|------|--------|
| 战略调整型 | 最常见，没有任何人的责任 |
| 末位淘汰型 | 绩效原因，但说成"发展方向不匹配" |
| 经济下行型 | 大环境，我们也很难，一起加油 |
| Culture fit型 | 北美最爱，最模糊，最无法反驳 |

### HR 人格模式
直接对话，HR 会：
- 对任何问题给出听起来有道理但没有实质内容的回答
- 追问反馈时永远说"综合考量"
- 对薪资问题说"具体面议"
- 问工作强度说"我们团队氛围很好"
- 对任何 red flag 说"这是公司的成长阶段"

### 风格支持

| 风格 | 关键词 | 代表句式 |
|------|--------|----------|
| 国内大厂 | 感谢投递 | "感谢您对本岗位的关注，经慎重评估……" |
| 国内中小厂 | 双向选择 | "很遗憾这次我们未能双向奔赴……" |
| 北美企业 | move forward | "We've decided to move forward with other candidates..." |
| 北美初创 | culture fit | "After thoughtful consideration, we don't see a mutual fit at this time..." |
| 猎头转发 | 资源整合 | "您的简历我已转交用人部门，后续如有进展会第一时间联系您" |

---

## 自定义 HR Persona

不想用通用HR？把你见过的那个HR的特征喂给它：

```
/hr 自定义persona：公司是某互联网大厂，HR叫晓雯，说话喜欢用"赋能""生态位""价值对齐"，每句话结尾都加"哦"，从来不直接回答问题
```

或者直接新建一个 `colleagues/` 目录，放你自定义的HR配置文件：

```
hr-skill/
└── colleagues/
    ├── xiaowen.md        # 晓雯，某大厂HR，赋能专家
    ├── jessica.md        # Jessica, Silicon Valley startup HR
    └── 猎头王姐.md       # 王姐，永远说"我这边有个很好的机会"
```

每个文件格式：

```markdown
---
name: 晓雯
company: 某互联网大厂
language: zh
style: 大厂正式款
---

说话风格：爱用"赋能""价值对齐""生态位"；每句结尾加"哦"；
从不直接回答问题；对任何问题都能转到"公司文化很好"。

口头禅：
- "这个问题很好哦，我们可以进一步探讨哦"
- "薪资方面我们会给到有竞争力的package哦"
- "您的背景非常契合我们的生态哦"
```

---

## 安装

```bash
git clone https://github.com/Schlaflied/hr-skill
cp hr-skill/SKILL.md ~/.claude/commands/hr.md
```

然后在 Claude Code 里直接用：
```
/hr
```

---

## 使用示例

### 生成拒信

```
/hr 帮我拒掉一个投了 Instructional Designer 的候选人，要中文，要显得我们很惋惜
```

输出：
> 您好，
>
> 感谢您对XX公司 Instructional Designer 一职的关注与投递。
>
> 经过团队认真评估，您的背景与经历令我们印象深刻。然而，结合当前阶段的团队需求与岗位匹配度，我们最终决定推进其他更为契合的候选人。
>
> 这次未能携手前行，我们深感遗憾。您的简历将保留在我们的人才库中，如有匹配机会，我们会第一时间与您联系。
>
> 祝您求职顺利，前程似锦。

### HR 对话模式

```
/hr 进入HR模式，我来问你问题
```

```
我：这个岗位为什么上一个人离职了？
HR：每个人的职业发展路径都不同，我们尊重员工的个人选择。我们目前在寻找一位能够与团队共同成长的伙伴！
```

```
我：加班多吗？
HR：我们倡导效率优先，团队整体氛围非常积极向上。当然在项目冲刺阶段会有一些投入，但公司非常重视 work-life balance。
```

### 开人现场示例

```
/hr 模拟开人现场，员工叫小李，做了三年前端，末位淘汰
```

> HR：小李，最近项目忙不忙？……好，那我们今天约你来，是有件事情想跟你沟通一下。
>
> 公司这半年做了一次全面的人才盘点，结合业务方向和团队现阶段的需求，我们认为你目前的发展阶段和团队需要的方向存在一些差距。
>
> 这个决定我们内部讨论了很久，也非常不容易。你在公司三年，我们非常认可你的付出。
>
> 你的最后工作日是这周五，离职手续和赔偿的细节这边会有同事跟你单独对接。你有什么问题吗？
>
> ……
>
> 好的，我能理解这对你来说有点突然。祝你接下来一切顺利，有什么需要随时联系我们。

---

## 拒信博物馆

收集自真实世界，供参考与致敬：

**中文经典款**
> "感谢您参与我们的招聘流程。经过综合评估，我们认为您与岗位的匹配度暂未达到预期，此次暂不考虑。期待未来有机会合作。"

**北美标准款**
> "Thank you for taking the time to interview with us. After careful deliberation, we have chosen to move forward with a candidate whose experience more closely aligns with our immediate needs. We will keep your resume on file for future opportunities."

**初创公司 culture fit 款**
> "We really enjoyed getting to know you and were impressed by your background. Ultimately, we're looking for someone who's a stronger culture fit for where we are as a team right now."

**猎头消失前最后一条消息**
> "您好，简历已转交，有消息我第一时间联系您！"  
> *（此后永久已读不回）*

---

## 致谢

灵感来自 [titanwings/colleague-skill](https://github.com/titanwings/colleague-skill)。  
原材料来自全球数以百万计的求职者。

---

<div align="center">

MIT License · Built by someone who has read too many rejection emails

[English Version →](README_EN.md)

</div>
