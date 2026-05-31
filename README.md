# 🎨 GPT Image 2 Prompt Skill

> A Claude Code skill that generates structured, noise-free prompts for GPT Image 2.

[English](#english) | [中文](#zhong-wen)

---

## <a id="english"></a>English

### What is this?

This is a [Claude Code](https://claude.ai) skill that helps you write better prompts for **GPT Image 2** (gpt-image-2), the latest image generation model from OpenAI.

The problem: GPT Image 2 is too obedient — the more details you give it, the more it tries to render everything, causing noisy, dirty images (blurry edges, grainy shadows, clumpy hair, overall haze).

The solution: **Less is more + a "weakening patch" at the end.**

### How it works

1. You describe what image you want in natural language
2. The skill extracts 6 elements: subject, scene, supporting elements, style, lighting, composition
3. It applies the de-noising framework to trim redundant details
4. It replaces problematic keywords (`ultra detailed`, `masterpiece`) with safe alternatives
5. It outputs a structured 3-paragraph prompt ready for gpt-image-2

### Installation

```bash
npx skills install athenagodpm/gpt-image2-prompt-skill
```

### Usage

In Claude Code, invoke the skill when you need to generate an image prompt:

```
gpt-image2-prompt 帮我生成一张赛博朋克少女雨夜街头的图
```

The skill will output a structured prompt like:

```
一位黑衣少女站在雨夜的霓虹街头，
身旁只有无声的全息广告在闪烁。
赛博朋克美学，克制风格，
柔和漫反射霓虹光，冷色调为主，
三分法构图，背景虚化。

整体画面弱化细节，干净高级感，
柔和光影，控制噪点，电影感色彩分级。
```

### Best for

- Posters / covers with text rendering
- E-commerce product shots
- Concept art & illustrations
- Multi-round iterative design

### Be cautious with

- Character consistency across multiple generations
- Complex compositions (many people + objects + precise positioning)
- Transparent background output (not supported)
- Non-Latin text rendering

---

## <a id="zhong-wen"></a>中文

### 这是什么？

这是一个 [Claude Code](https://claude.ai) 的 skill，帮你为 **GPT Image 2**（gpt-image-2）编写高质量的图像生成 prompt。

核心痛点：GPT Image 2 太"听话"了——prompt 信息越多，它越想画到位，导致**脏图**（边缘发糊、暗部噪点、头发结块、整体灰蒙蒙）。

解决方案：**做减法 + 末尾加弱化补丁。**

### 工作流程

1. 你用自然语言描述想要的图片
2. Skill 提取 6 个要素：主体、场景、辅助元素、风格、光影、构图
3. 用精简准则过滤冗余信息，避免信息过载
4. 替换脏词（`ultra detailed` → `弱化细节`）
5. 输出三段式结构化 prompt

### 安装

```bash
npx skills install athenagodpm/gpt-image2-prompt-skill
```

### 使用

在 Claude Code 中触发 skill：

```
gpt-image2-prompt 帮我生成一张赛博朋克少女雨夜街头的图
```

### 最强场景

- **文字/海报/封面** — 文本渲染能力领先
- **电商/产品图** — 世界知识丰富，产品真实感强
- **概念图/插图** — 指令跟随好，风格可控
- **多轮设计迭代** — 支持对话式改图

### 注意事项

- 不支持透明背景输出
- 跨图角色一致性不如 Midjourney 稳定
- 非英文字体渲染不太稳定
- 避免使用"超高细节""ultra detailed""masterpiece"等脏词

---

Built from [athena's de-noising methodology](https://github.com/athenagodpm/gpt-image2-prompt-skill) + personal practice + OpenAI official docs.
