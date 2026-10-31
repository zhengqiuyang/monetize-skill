# monetize

**Turn your career history into an honest, actionable side-income plan — inside your AI agent.**
**把你的职业经历，变成一份诚实、可执行的变现方案 —— 直接在你的 AI 编程助手里运行。**

An [Agent Skills](https://agentskills.io) compatible skill. Works with Claude Code, ZCode, Cursor, Codex, and any agent that supports the open Agent Skills standard.

一个符合 [Agent Skills](https://agentskills.io) 开放标准的技能，Claude Code / ZCode / Cursor / Codex 等任何支持该标准的智能体均可用。

---

## Why / 为什么做这个

"用 AI 分析我能怎么赚钱"的提示词到处都是，但它们都是一次性玩法：粘贴一段 prompt，得到一堆通用建议和**编造的薪资数字**。

`monetize` 把这件事做成了结构化工作流：

- **6 模块漏斗**：技能审计 → 机会扫描 → 经验产品化 → 最大杠杆点 → 薪资对标 → AI 副业启动包
- **数字可溯源**：薪资/市场价要么联网核实并给来源，要么明确标注"估算，未核实"
- **强制收敛**：最终只给 1 个"本周就开始"的动作 + 一份可验收的 30 天行动清单
- **诚实守则**：不承诺收入、点出竞争与风险、拒绝灰色玩法、背景太薄就直说

支持两种背景输入：丢一份简历/经历描述直接解析，或者让技能分轮访谈你（每次只问 3-4 个问题）。

## Install / 安装

```bash
npx skills add zhengqiuyang/monetize-skill
```

Or manual / 或手动安装：

```bash
git clone https://github.com/zhengqiuyang/monetize-skill.git ~/.agents/skills/monetize
```

安装后在新会话中用 `/monetize` 触发，或自然语言触发（"帮我看看能做什么副业"、"我的技能怎么变现"、"分析下我的薪资天花板" / "what side hustle fits my skills?"）。

## Usage / 用法

```
# 完整流程（引导访谈输入）
/monetize 我做了5年会计，想搞点副业

# 完整流程（简历输入）
/monetize @我的简历.pdf 帮我分析变现潜力，目标每月多赚 5000

# 单模块
/monetize 我是做运营的，帮我分析薪资天花板
```

运行节奏：先产出「技能审计 + 机会扫描」供你确认方向，再跑后四个模块并合成完整报告 `monetization-report.md`。

## What you get / 你会得到

一份这样的报告（[完整示例节选](assets/report-sample.md)）：

```markdown
# 变现潜力分析报告 — 李某 · 2026-11
## 0. 核心资产画像
## 1. 隐藏技能审计        ← 10 项被低估的技能 × 谁付费 × AI 如何放大
## 2. 收入机会扫描        ← 10 条路径 × 启动成本/时间/难度/收入区间（附来源）
## 3. 变现产品化建议      ← 服务 / 咨询 / 数字产品 / 自由职业 offer
## 4. 最大杠杆点          ← 只有一个"本周就开始"的动作
## 5. 薪资天花板对标      ← 更高薪岗位 × 资格差距 × 过渡路径
## 6. AI 副业启动包       ← 5 个每周 <5 小时的 AI 辅助服务
## 7. 30 天行动清单       ← 每项带验收标准
## 附录 A 数据来源 / 附录 B 未核实估算清单
```

技能默认按用户语境适配市场（中国大陆 / 北美 / 欧洲：货币、平台、薪资数据源），详见 `SKILL.md` 中的「语言与市场适配」。

## Design principles / 设计原则

1. **具体压倒通用** — 每个结论必须能追溯到用户的具体经历，拒绝"你可以做咨询"式的废话
2. **数字要么核实、要么标注** — 宁可少给数字，不给编造的数字
3. **诚实压过讨好** — 不承诺收入；明确前 3 个月收入通常远低于稳定期；主动提示劳动合同兼职条款、平台规则、税务、需资质领域等核查点
4. **反分析瘫痪** — 10 条机会不等于要都做；报告收敛到一个杠杆点 + 备选

## Disclaimer / 免责声明

This skill provides educational analysis, not financial, legal, or tax advice. Verify contracts, platform policies, and local regulations before starting any income activity.

本技能仅提供分析思路，不构成理财、法律或税务建议。开展任何收入活动前请自行核查劳动合同、平台规则与当地法规。

## License / 许可

[MIT](LICENSE)
