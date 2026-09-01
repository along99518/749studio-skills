# 749studio Skills

> AI 短剧创作方法论 Skill 集。故意克制型的影视化适配工具。

Agent Skills 开放标准格式（SKILL.md + references/），支持 Claude Code / Codex / Gemini CLI / Cursor 等 Agent 工具加载，也可导入扣子（Coze）技能。

## Skills

### viral-opening —— 爆款开头

为单集短剧生成「前 20-30 秒留住观众」的口播文案候选（A/B/C/D 四种主角驱动结构），并可将锁定文案视听化为高密度短镜头剧本。

它不会：

- × 虚构剧本里没有的爆点（每一句必须有原文依据）
- × 让案件/反派抢走主角的叙事主体地位
- × 提前剧透主角的最终计划和结局
- × 写成剧情简介/新闻摘要/口号总结

它只做：完整剧本 → 主角识别 → 爆点扫描 → 四结构文案候选 → 视听化（OS 一字不改）。

### script-vision —— 剧本视听适配

把小说/网文/文学剧本转换为**可拍摄的影视剧本正文**（可直接交给分镜系统）。

一个故意不让 AI 多写的适配器。它不会：

- × 续写剧情（原文结束，画面也结束）
- × 修改对白（台词 100% 逐字锁定）
- × 抢分镜的活（不输出镜头表）
- × 创建人物设定 / 剧情梗概
- × 无意义扩写（「信息增益」原则：每新增一句必须有新信息）

它只做：文学叙述 → 可拍摄场景正文（心理转表演、时间轴守恒、场景事件边界）。

附角色级台词多语言转换（普通话/英日韩 + 四川话/粤语/东北话等方言口语化转写）。

### visual-director —— 视觉导演

为一部剧确定「用什么导演拍摄语言去拍」。两阶段：先出 4 个**拍法完全不同**的方案对比（严禁画风词），再按选定方案输出六段结构视觉定位文案。

它不会：输出画风、角色设定、分镜、资产——只做导演语言决策。

## 为什么是「克制型」？

AI 改编最大的毛病，不是不会写，而是**太会写**：

42 字原文 → 普通 LLM 改成 200 字（同义堆砌 + 台词加料 + 凭空续写）→ 下游时长、配音、预算全部失真。

本仓库的 skill 用硬规则约束模型只做转换、不做创作。三个案例看懂差异：

- [案例1：AI 为什么越改剧本越长](examples/case-1-info-gain.md)
- [案例2：为什么禁止 AI 润色台词](examples/case-2-dialogue-lock.md)
- [案例3：原文结束，画面也必须结束](examples/case-3-no-continuation.md)

## 分发渠道

| 渠道 | 地址 |
|---|---|
| GitHub | https://github.com/along99518/749studio-skills |
| HuggingFace | https://huggingface.co/datasets/along9958/749studio-skills |
| 虾评（众测） | 爆款开头：https://xiaping.coze.com/skill/3ee543bb-a426-40fd-9dc1-9774185a684f<br>视觉导演：https://xiaping.coze.com/skill/3662a5e5-f248-42c5-86d1-784f9530ace6<br>剧本视听适配：https://xiaping.coze.com/skill/81b3cd8e-41f8-4696-aa39-ff720c8460fb |

## 版本说明

- 各 skill 标注 snapshot-v1：从生产系统抽离时的规则快照，不与生产版本实时同步
- 反馈通过 GitHub issue 提交

## License

CC-BY-NC-4.0（署名-非商业性使用），全文见 [LICENSE](LICENSE)。商业授权请联系仓库所有者。
