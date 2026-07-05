# 生图提示词模板

每张图单独生成。根据正文内容替换变量，不要把多张图拼在一张里。

```text
Use case: illustration-story
Asset type: Chinese article body illustration in the Yunqing Comics recurring IP style
Primary request: Create one standalone hand-drawn article illustration that explains this idea: {核心意思}
Scene/backdrop: clean warm white paper background with generous empty space; only a few simple desk/story objects if needed
Subject: recurring original IP characters, a small fluffy cloud and a tiny clear bottle. The cloud is {云朵动作}; the bottle is {瓶子动作}. They must perform the core conceptual action, not decorate the scene.
Role semantics: {work-division / AI-human collaboration / blended}. If AI-human collaboration, the cloud represents Yunqing the AI assistant and the bottle represents Zaiping / the human creator; keep both as cloud-and-bottle IP characters, not a robot and a human body.
Structure type: {前后对比 / 系统局部 / 输入处理输出 / 方法分层 / 角色状态 / 概念隐喻}
Composition/framing: {具体构图：主物件、左右/前后关系、信息如何移动}
Style/medium: cute independent hand-drawn cartoon IP, loose pencil and fine ink linework, slightly wobbly imperfect outlines, soft watercolor wash accents, simple black dot faces, warm but not childish, polished article illustration
Color palette: warm off-white, graphite gray lines, pale sky blue, transparent soft blue, muted peach, cream yellow, tiny honey-yellow star details
Materials/textures: light paper grain, soft pencil texture, translucent bottle wash, simple rounded handmade shapes
Text: {默认 no readable text；如需要，使用 0-4 个外围手写标注，每个 2-6 个中文字；标注词必须从当前文章段落的关键词、角色动作或核心隐喻中提炼；不要复用固定词表；不要标题、长句或图例}
Constraints: one image explains only one core idea; keep the characters central to the action; preserve generous white space; use a fresh physical metaphor for this article
Avoid: avoid photorealism, 3D render, hard vector logo style, PPT infographic look, dense UI screenshot, complex architecture diagram, lots of text, branded elements, copying Xiaohei or any reference character
```

## 提炼标注和动作

生成前先从当前正文提炼：

- 1 个核心判断：这张图到底解释什么。
- 1-2 个动作词：例如搬、托、选、压平、过滤、连接、盖章、沉淀；必须贴合正文。
- 0-4 个短标注：必须来自当前段落的关键词或隐喻，不要因为模板里出现过就默认使用。

如果正文没有明确关键词，宁可不写字。不要把上一张图里的“问题 / 候选 / 判断 / 沉淀”等词自动带入下一张图。

## 让角色更参与

如果角色变成装饰，用这个方向重写：

```text
Regenerate with the same core idea, but make the cloud and bottle perform the conceptual work. The cloud should physically move, connect, soften, or gather the messy part. The bottle should record, store, filter, validate, or protect the organized result. If the characters are removed, the metaphor should no longer work.
```

## 强化 AI-人协作

当主题涉及 AI 助理和人类共同完成任务时，用这个方向重写：

```text
Regenerate with the cloud as Yunqing, the AI assistant, and the tiny clear bottle as Zaiping / the human creator. The cloud should sort messy inputs into a few candidate cards or gentle threads. The bottle should choose, stamp, store, or label the final result, showing human judgment and ownership. Keep the characters as the original cloud-and-bottle IP; do not draw a robot or realistic person.
```

## 加少量手写标注

```text
Add only 0-4 tiny handwritten Chinese side labels near the relevant objects. The label words must be extracted from the current article section and its metaphor. Keep labels peripheral, readable, and sparse. Do not use a fixed default label set. Do not add a big title, legend, paragraph, or speech bubble.
```

## 减少信息图感

```text
Regenerate as a warm hand-drawn article illustration, not a diagram. Remove title bars, grid layout, formal nodes, excessive arrows, and explanatory labels. Keep one main handmade object and one clear action.
```
