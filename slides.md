---
theme: dracula
title: Signal is Physics
info: |
  Talk Slides Template
highlighter: shiki
drawings:
  persist: false
transition: slide-left
mdc: true
download: true
fonts:
  sans: Noto Serif SC
  mono: Noto Serif SC
---

<!-- 页面类型：封面页。用于介绍整场报告的主题、署名、机构和时间，是观众进入演讲的第一印象。 -->

<span class="title-slide-marker"></span>
<!-- 页面标记：触发 style.css 中的封面页专用样式。 -->

# Signal is Physics
<!-- 主标题：报告或项目的核心名称。 -->

## Structured Reasoning for Multimodal World Understanding
<!-- 副标题：用一句话补充报告的研究范围或方法主线。 -->

**Yiwei Wang** - University of California, Merced
<!-- 作者/单位：说明汇报人、团队或机构信息。 -->

May 2026
<!-- 时间：说明报告日期或版本。 -->

![UC Merced](/Image/uc_yellow.svg)
<!-- 标识图片：放置学校、实验室、公司或项目 logo。 -->

---

<!-- 页面类型：普通图文页。用于讲清一个核心观点、背景问题或概念，并用图片辅助理解。 -->

# Three Questions, One Principle
<!-- 页面标题：概括本页要讲的中心问题或结论。 -->

**Multi-microphone localization** asks whether we can infer where a sound comes from.

**Camera-motion understanding** asks whether AI can tell pushing forward from rotating.

**Sonar-array reconstruction** asks whether multi-transducer signals can recover a target position.
<!-- 正文要点：用短段落或项目式文字展开主要内容。 -->

These three questions are, fundamentally, the same question.
<!-- 强调句/过渡句：收束本页观点，连接到下一页。 -->

![Figure](/Image/fig_1.png)
<!-- 主图：展示概念关系、例子、流程或视觉证据。 -->

---

<!-- 页面类型：目录页。用于进入一个新的 Part，并在目录中高亮当前章节。 -->

<span class="toc-slide-marker"></span>
<!-- 页面标记：触发 style.css 中的目录页专用样式。 -->

# Contents
<!-- 目录标题：说明当前页展示报告结构。 -->

<div class="toc-list">
  <div class="toc-item is-current">
    <span class="toc-index">Part 1</span>
    <span class="toc-title">Perception != Understanding</span>
  </div>
  <div class="toc-item">
    <span class="toc-index">Part 6</span>
    <span class="toc-title">Looking Up: From Reasoning to Action</span>
  </div>
</div>
<!-- 目录条目：当前章节行保留深色，其他章节行由样式变为浅灰。 -->

---

<!-- 页面类型：纯文字论述页。用于解释定义、挑战、假设、结论，不依赖图片或表格。 -->

# Capability Boundary of Current Multimodal AI
<!-- 页面标题：说明本页讨论的问题。 -->

### What Models Have Achieved
<!-- 小标题：组织正文层级，让听众快速抓住逻辑段落。 -->

Current models are strong at **image recognition and generation**, improving quickly in **video QA and cross-modal retrieval**, and advancing rapidly in **speech understanding and audio generation**.
<!-- 正文段落：陈述背景、现状、定义或论证。 -->

### But There Are Systematic Failures in Physical Constraint Reasoning
<!-- 小标题：引出转折、限制或核心问题。 -->

Yet they still fail on **sound-source motion**, show **audio-video temporal misalignment**, and can drift further from physical truth as reasoning chains become longer.
<!-- 正文段落：给出问题、风险或研究动机。 -->

Scale and data alone cannot fix a missing understanding of physics.
<!-- 结论句：用一句话收束本页信息。 -->

---

<!-- 页面类型：论文/证据展示页。用于展示一个研究发现、实验结果或代表性工作，并附引用来源。 -->

# Evidence 1 - Spatial Blind Spot
<!-- 页面标题：说明证据编号、研究名称或发现主题。 -->

### Key Finding
<!-- 小标题：标出本页最重要的发现。 -->

Audio LLMs Cannot Perceive Sound Source Direction. When a sound source moves **left to right**, the model can barely determine the direction, and accuracy approaches **random chance**.
<!-- 正文结论：简洁描述实验现象、结果或贡献。 -->

**Conclusion**: The model is listening, but not reasoning about space.
<!-- 强调结论：用一句话解释这个证据对主线的意义。 -->

![Figure](/Image/fig_4.png)
<!-- 结果图片：放置实验图、方法图、曲线图或 benchmark 表现。 -->

<footer>Spatial Blind Spot: Auditory Motion Perception Deficits in Audio LLMs. Zhe Sun, Yujun Cai, Jiayu Yao, Yiwei Wang. 2025</footer>
<!-- 页脚引用：放论文标题、作者、年份或备注信息。 -->

---

<!-- 页面类型：表格型总结页。用于做方法归纳、工作对比、框架映射或章节总结。 -->

# Three Forms of Structured Reasoning
<!-- 页面标题：说明表格总结的对象。 -->

The reasoning process is **transparent and interpretable** with respect to physical constraints.
<!-- 引导正文：说明为什么需要这张表。 -->

| Form | Mechanism | Representative Work |
|------|-----------|-------------------|
| Reasoning Chain | Each step maps to a physical operation | ViewFusion, Thinking with Sound |
| Path Selection | RL learns physically consistent reasoning order | CamReasoner, AudioRouter |
| Structure Injection | Hard-coded physical constraints injected into reasoning | PAS (Phase Aggregated Smoothing) |
<!-- 表格：第一列通常是类别或对象，后续列解释机制、作用、代表工作或映射关系。 -->

---

<!-- 页面类型：带引用的表格方法页。用于解释一个具体方法的内部步骤、物理含义或模块映射，并在页脚保留论文来源。 -->

# ViewFusion - Physical Significance
<!-- 页面标题：说明该方法页讲的是哪项工作或哪个机制。 -->

Each **reasoning step** corresponds to a physical operation, and conclusions from different viewpoints must remain **geometrically consistent**.
<!-- 正文说明：先用一到两句话解释表格的阅读方式和本页结论。 -->

| Reasoning Step | Physical Operation |
|------------|------------------------------|
| Coordinate alignment | Extrinsic matrix transform |
| Triangulation | Multi-view geometry |
| Relation inference | 3D spatial computation |
<!-- 方法表格：列出步骤、模块、物理操作、输入输出或验证方式。 -->

<footer>ViewFusion: Structured Spatial Thinking Chains for Multi-View Reasoning. Xingjian Tao, Yiwei Wang, Yujun Cai, Yifan Song, Jing Tang. 2026</footer>
<!-- 页脚引用：放该方法对应的论文或项目来源。 -->

---

<!-- 页面类型：目录页。用于进入一个新的 Part，并在目录中高亮当前章节。 -->

<span class="toc-slide-marker"></span>
<!-- 页面标记：触发 style.css 中的目录页专用样式。 -->

# Contents
<!-- 目录标题：说明当前页展示报告结构。 -->

<div class="toc-list">
  <div class="toc-item">
    <span class="toc-index">Part 1</span>
    <span class="toc-title">Perception != Understanding</span>
  </div>
  <div class="toc-item is-current">
    <span class="toc-index">Part 6</span>
    <span class="toc-title">Looking Up: From Reasoning to Action</span>
  </div>
</div>
<!-- 目录条目：当前章节行保留深色，其他章节行由样式变为浅灰。 -->

---

<!-- 页面类型：结束页。用于感谢听众、邀请提问，并提供联系方式。 -->

# Thank You!
<!-- 页面标题：结束语。 -->

<span class="closing-slide-marker"></span>
<!-- 页面标记：触发 style.css 中的结束页专用样式。 -->

Questions and discussion welcome.
<!-- 结束说明：邀请讨论或说明下一步。 -->

[wangyw.evan@gmail.com](mailto:wangyw.evan@gmail.com)
<!-- 联系方式：邮箱、主页、二维码或社交账号。 -->

![UC Merced](/Image/uc_yellow.svg)
<!-- 标识图片：再次放置 logo 或品牌标识。 -->

<style>
:global(#slidev-goto-dialog.-top-20) { overflow: hidden; max-height: 80px; }
</style>