# how-to-live-better-skill

Agent skill generated from **《HowToLiveBetter / 高性价比人生指南》** by **eternity4719**, with [book-to-skill](https://github.com/virgiliojr94/book-to-skill).

一本 414 页、34 节、667 条建议的中文开源生活指南，压缩成 agent 可直接调用的知识库。每条建议在原书中都写明「花掉什么、换回什么、证据有多硬」，本 skill 保留了这套判断框架：遇到一件事该不该做，先问成本、收益、证据等级，再问性价比。

覆盖健康与急救、省钱防骗、中国大陆法律红线与劳动社保、婚育育儿、出国留学、创业合规、慢性病与养老。

## 安装

```bash
npx skills add https://github.com/id399-dzx/how-to-live-better-skill
```

仓库根目录即 skill 根目录（`SKILL.md` 在根），无需 `--skill` 子路径。

或手动：clone 到你的 agent skills 目录（如 `~/.claude/skills/`、`~/.copilot/skills/`、`~/.workbuddy/skills/`）下，目录名保持 `how-to-live-better`。

## 用法

- 不加参数 — 加载核心判断框架
- 问一个具体事 — 「替朋友担保签不签」「每天通勤两小时值不值」「家里老人摔倒过要不要装扶手」；会定位到具体条目并注明出自第几节第几条
- 问某节 — 说 `ch13` 或「紧急情况」
- 浏览 — 问「有哪些章节」

查不到就说查不到，不编数字。

## 文件

| 文件 | 内容 |
|---|---|
| `SKILL.md` | 10 条核心判断框架 + 36 章索引 + 主题索引 |
| `chapters/` | 36 个章节摘要（ch00 方法论、ch01–ch34 逐节、ch35 附录 9 篇长文） |
| `cheatsheet.md` | 一页纸：判断规则表、时间窗、热线、硬阈值、识别信号 |
| `patterns.md` | 15 个可复用决策模式 |
| `glossary.md` | 统计 / 法律 / 医保 / 金融 / 心理术语表 |

章节文件按需加载，不占用常驻上下文。

## 内容与许可

**这些文件是综合摘要，不是原书正文。** 章节内容由 agent 提炼、压缩、重构而成，保留了原书的数字、条款号与判断口径，但没有复制原文段落。

- 原作品：**《HowToLiveBetter / 高性价比人生指南》**，作者 **eternity4719**
- 原作品链接：https://github.com/eternity4719/HowToLiveBetter
- 原作品许可：**CC BY 4.0**（Creative Commons Attribution 4.0 International）
- 修改：是 —— 摘要化、按 agent skill 结构重组、补充索引与速查表
- 本仓库许可：CC BY 4.0（见 [LICENSE.md](LICENSE.md)）
- 快照版本：2026-10-06，原书正文提交 `20718ee`

原书每天都在改，**涉及时效性强的金额、天数、条款时请以在线版为准**：https://eternity4719.github.io/HowToLiveBetter/

## 边界

- 中国大陆语境。法律、医保、社保内容按中国大陆现行规定写，不能当境外依据。
- 这不是医嘱，也不是法律意见。原书在每条里留的边界提示（「去看医生」「按你的医生的意见办」「以当地规定为准」）在本 skill 中保留。
- 成本栏数字是作者按市面价格的粗略估计，只用于互相比较，不宜引用。
