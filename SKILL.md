---
name: silas-handdrawn-real-object-scenes
description: Use when a user requests flat hand-drawn Silas article illustrations, lightweight real-object metaphor scenes, work-situation images, project-review visuals, or hand-drawn long-scroll story images; do not use for the Silas 2.5D branch or photorealistic human compositing.
---

# Silas Hand-Drawn Real-Object Scenes

把中文主题、正文或项目经历转成“扁平手绘 Silas + 摄影质感真实物件 + 清楚物理动作 + 短中文标注 + 大留白”的正文图或长卷故事图。

## 两种模式

- 标准模式：默认 16:9，一张图只表达一个冲突、一个核心动作和一个主物件组。
- 长卷模式：项目复盘、个人路径、产品演化或成长叙事时使用；用一条自然起伏的手绘路线串联 5-8 个实物节点。

如果用户只要分析或建议，先输出 shot list；用户明确要求生成或看效果时，完成内部母版锁定后直接生成。具体事实只能来自用户输入或用户提供的素材。

## 工作流

1. 读取 `references/character-ip.md`，锁定 Silas 的手绘身份特征。
2. 读取 `references/style-dna.md`，锁定手绘角色与摄影实物的混合媒介、比例和留白。
3. 用 `references/story-extraction.md` 把主题压成处境、物理冲突、动作和 2-4 个短标签。
4. 用 `references/object-patterns.md` 选择能与角色真实接触的物件；禁止堆叠主题名词。
5. 标准模式读取 `references/master-selection.md`，从 01-06 选择质量锚点；长卷模式锁定 07。
6. 用 `references/prompt-template.md` 写每张图的独立提示词。角色图只作为 identity reference；母版只作为 composition reference。
7. 每次只生成一张候选图，查看后按 `references/qa-checklist.md` 验收；未通过就修正并重生成。
8. 保存到用户指定目录；没有指定时使用当前项目的版本化资产目录，不覆盖既有文件。

## 母版与隐私边界

- `assets/identity/silas-handdrawn-identity.png` 是唯一内置身份锚点。
- `assets/examples/01-06` 是标准模式质量锚点；`07-creation-route-long-scroll.png` 是长卷骨架。
- 母版用于校准比例、留白、动作清晰度与混合媒介融合，不是可描摹构图。至少改变主物件、空间方向、角色动作、配件、标签位置、视角中的 3 项。
- 不从身份图、母版或外部资料推断用户履历、公司、数据或项目事实。

## 输出门槛

候选图必须在 3 秒内读懂；Silas 必须以手和身体承担核心物理动作；真实物件必须保持摄影质感；角色不得漂成 2.5D 公仔。第一张结果只是候选图，查看和 QA 后才能交付。
