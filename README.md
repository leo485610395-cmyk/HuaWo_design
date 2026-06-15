# huawo / 化我 Design System

> Editorial Magazine × Parametric Engineering
> 大学生 AI 产品经理的个人品牌视觉系统,以 `DESIGN.md` 形式存在,可被 AI Agent 直接消费。

---

## 这是什么

这是一份**可机器读的设计系统文件**。

不是一份风格指南 PDF,不是一张色卡截图——是一份结构化的 Markdown,把色彩、字体、栅格、组件、动效、品牌语气、反模式全部写清楚,AI Agent(Claude Code / 牛马 / Codex / Gemini 等)读完就能基于它产出符合本品牌视觉的衍生品:小红书封面、公众号头图、PPT、App 原型、Landing Page。

这份文件的设计哲学来自 [Open Design](https://github.com/nexu-io/open-design)——把设计系统从抽象审美沉淀成可复利的数字资产。

---

## 它长什么样

九段式结构:

| 段 | 内容 |
|----|------|
| 1. Visual Theme & Atmosphere | 视觉主题、氛围、设计意图 |
| 2. Color | 主色、强调色、语义色、用法约束 |
| 3. Typography | 字体族、字号档位、字重、加载方式 |
| 4. Spacing & Grid | 间距基准、栅格、版心宽度、对齐 |
| 5. Layout & Composition | 顶部签名行、章节标题、参数行、双底切换 |
| 6. Components | 章节标题、参数行、盟友卡、CTA、Toast |
| 7. Motion & Interaction | 过渡时长、hover 行为、禁用项 |
| 8. Voice & Brand | 品牌签名、身份标签、哲学收尾、禁用词 |
| 9. Anti-patterns | 不做什么——用反向定义边界 |

每一段都写约束,不写玄学。比如「暖金不要超过画面 10%」「不要在暖白主背景上用纯黑,用 #0E0E0E」——这种规则 AI 能直接执行。

---

## 怎么用

### 用法 1:直接喂给 AI Agent,让它给你产出衍生品

```bash
# 在 Claude Code / 牛马 里贴这段 prompt
请读取 huawo-design-system/DESIGN.md,严格按它的色彩、字体、栅格、品牌语气,
给我生成一张小红书封面(1080×1440),HTML/CSS 单文件。

主题:<你的主题>
身份编号:№<编号> / <英文标签> / <中文标签>
钩子(主标题):<主标题>
副钩子:<副标题>
```

### 用法 2:注册到 Open Design,变成你的可调用设计系统

```bash
# 1. clone Open Design
git clone https://github.com/nexu-io/open-design.git

# 2. 把本仓库的 DESIGN.md 放进去
cp huawo-design-system/DESIGN.md open-design/design-systems/huawo/DESIGN.md

# 3. 启动 daemon
cd open-design && pnpm install && pnpm tools-dev

# 4. 打开 Web UI,在 Design System 下拉里就能看到 huawo
```

### 用法 3:作为你自己的设计系统模板

fork 这份文件,把色彩、字体、品牌签名、身份标签换成你自己的——这是最快的设计系统搭建路径。**保留九段式结构,不要砍。** 结构本身就是它的可复利价值。

---

## 三个核心约束(用了就要守住)

1. **暖金 #C5A880 不超过画面 10%**——它是锚点,不是装饰
2. **✦ 符号只用在签名、章节分隔、关键转折**——不当装饰撒
3. **不要渐变、不要直角、不要纯黑**——克制是这套视觉的核心

守住这三条,产出就锁定在品牌调性里;破了任意一条,视觉就散架。

---

## License

MIT——你可以 fork、改写、商用、自托管。

但保留这份文件的精神:它是结构化资产,不是抽象审美指南。fork 之后请把你的色彩、字体、签名写清楚,别让它退化回「感觉对了就行」。

---

## 相关阅读

- **Open Design** — https://github.com/nexu-io/open-design
- **DESIGN.md 完整手册** — 见同仓库 `manual.md`(把网站变成 design.md 的实操手册)
- **作者**:huawo / 化我 · 浪尖领航官
