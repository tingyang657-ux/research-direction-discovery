# Research Direction Discovery · 研究方向发现

一个帮助研究者从已有突破中发现下一阶段研究方向的 skill，重点是第一性原理、跨领域机制借鉴和关键问题定义。

适用于“某篇论文已经证明一种新能力可行，接下来还能研究什么”的构思阶段。它帮助区分研究大方向、问题、解决机制与实现细节，并明确哪些判断来自事实、结构推论或待验证假说。

## 方法

从前人实际展示的能力出发，区分必须满足的约束与可以重新设计的设定。跨领域借鉴采用以下链条：

> 原领域的真实问题 → 被挑战的假设 → 改变的机制 → 目标领域的对应关系 → 仍需验证的部分。

每个候选方向应给出问题及其重要性、解决思路、具体来源和通俗实例。构思阶段允许大胆假说，不默认预演审稿答辩，也不把类比直接当作目标领域的证据。

## 包含内容

| 文件 | 用途 |
| --- | --- |
| [SKILL.md](SKILL.md) | 技能入口与核心构思方法 |
| [principle-lenses.md](references/principle-lenses.md) | 七个可按需选择的理论分析视角 |
| [cross-field-cases.md](references/cross-field-cases.md) | 六张含一手文献链接的跨领域案例卡 |
| [routing-lessons.md](references/routing-lessons.md) | EDA 布线讨论中的候选状态与纠偏经验 |
| [openai.yaml](agents/openai.yaml) | Codex 界面元数据与默认调用提示 |

这是说明型 skill，没有需要运行的程序，也不包含模型 API 密钥或服务配置。布线案例用于说明方法，不代表相关候选已经通过实验或新颖性验证。

## 安装与使用

本仓库根目录就是 skill 目录。下载或克隆后，将整个目录命名为 `research-direction-discovery`，保留 `SKILL.md`、`agents/` 和 `references/` 的相对路径，并放入宿主支持的 skills 目录。

对于使用个人 `~/.codex/skills` 目录的 Codex 环境，目录结构为：

```text
~/.codex/skills/research-direction-discovery/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── principle-lenses.md
    ├── cross-field-cases.md
    └── routing-lessons.md
```

个人目录示例与显式调用方式可参见 [OpenAI 官方 skills 实践说明](https://developers.openai.com/blog/eval-skills)。不同宿主或版本的安装位置，请以对应的 [官方技能文档](https://learn.chatgpt.com/docs/build-skills) 为准。

调用示例：

```text
使用 $research-direction-discovery，从已有的算法进化突破出发，
提出几个同级研究方向。每个方向解释发现了什么关键问题、
准备如何解决，以及具体借鉴了其他领域的哪段经验。
先停留在方向和问题定义层面，不立即进入源码实现。
```

本 skill 支持研究构思，不能替代文献核验、实验或数学证明。
