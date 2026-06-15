# Design System for huawo / 化我

> Category: Personal Brand
> Editorial Magazine × Parametric Engineering——杂志装帧感的暖白纸 + 暖金强调色 + 深黑色块反差 + 工程参数化的坐标 / 编号系统。大学生 AI 产品经理的个人品牌视觉系统。

## 1. Visual Theme & Atmosphere

杂志装帧 × 工程参数。暖白纸感主背景 + 暖金强调色 + 深近黑色块反差 + 衬线大字（Bodoni Moda）× 几何无衬线（Syne）× 现代无衬线（Plus Jakarta Sans）。章节用 № 编号 + 双语标签锚定，参数行用 mono 字体 + `KEY / 值` 结构。整体调性克制、精致、有装帧感——不是硬核 Brutalism，是杂志感的工程美学。

- **Visual style:** Editorial Magazine + Parametric Engineering
- **Color stance:** 暖白主背景 + 深黑反差色块 + 暖金强调
- **Design intent:** 让一张封面、一张配图、一页 PPT 都能被识别为「化我的视觉」——靠五个特征锁风格：№ 编号、参数行、双语标签、✦ 符号、暖金强调

## 2. Color

- **Primary:** `#F5F4F0` — 暖白纸感，主背景
- **Secondary:** `#0E0E0E` — 深近黑，反差色块背景（hero 区、深色卡片）
- **Accent:** `#C5A880` — 暖金/沙金，品牌强调色，用于 ✦ 符号、CTA、关键数字、链接 hover
- **Tertiary:** `#161616` — 次级深色，反差色块层次
- **Text:** `#0E0E0E` — 深近黑，主文字
- **Text-on-dark:** `#F5F4F0` — 暖白，反差色块上的文字
- **Mute:** `#7A7A77` — 暖灰，副文字（坐标、状态行、版权）
- **Warm-blush:** `#EAD5C3` — 浅杏色，柔化背景或次级 surface
- **White:** `#FFFFFF` — 纯白，仅用于反差色块上的高对比文字
- **Success:** `#16A34A`、**Warning:** `#D97706`、**Danger:** `#DC2626` — 仅状态用

- 主背景暖白、反差色块深黑、单一暖金做强调——禁止渐变、禁止引入第二种暖色
- 暖金不要超过画面 10%——多了就失去锚点作用
- 暖金 hover/glow 用 `rgba(197,168,128,0.2)` 透明度做光晕

## 3. Typography

- **Scale (固定档位):**
  - 正文 sm / base / lg / xl = **14 / 16 / 20 / 24 px**（line-height 1.65-1.75）
  - 标题 sm / base / lg / xl = **40 / 56 / 80 / 112 px**（line-height 0.92-0.95, letter-spacing -0.02 ~ -0.03em）
  - 数字超大字 moment：**96 / 128 px**（Bodoni Moda 900，仅融资额 / 哲学引言用）
  - 参数行 mono：12-14 px，letter-spacing 0.06-0.12em
- **Families:**
  - display = **Syne** 700-800 —— 大标题、品牌名（HW / 化我✦）、英文大写标签
  - serif = **Bodoni Moda** 400-900 含斜体 —— 装饰性引言、特殊章节、衬线大字 moments
  - primary = **Plus Jakarta Sans** 300-700 —— 主文字、双语标签、正文、CTA
  - mono = **JetBrains Mono** 或 **ui-monospace** —— 坐标、状态行、参数行、№ 编号、版权、SVG 标签
- **Weights:** 300 / 400 / 500 / 600 / 700 / 800
- 字体加载：Google Fonts（preconnect + display=swap）
- 英文大写 + 中文小字嵌套时，中文字号比英文小一档（HW 16pt + 化我 14pt）
- mono 字体只用于参数化信息——不用于正文
- 标题大字用 Syne 800，副标用 Plus Jakarta 500（英文大写 + 中文小字）
- Bodoni Moda 仅用于关键衬线大字 moments（如哲学收尾、引言）——不要泛用

## 4. Spacing & Grid

- **Spacing scale:** 4 / 8 / 12 / 16 / 24 / 32 / 64（4 倍数基准）
- **Container width:** 1200px（PC）/ 100%（移动）
- **Section padding:** 64 / 32（PC / 移动）
- **Swiss Grid（正式版式）:** 12 列 × 128px 内容区，列间距 20px，左右 padding 120px（PC）/ 24px（移动）
- **Slide 标准:** 1920×1080（横版 PPT）/ 1080×1440（竖版小红书）/ 900×383（公众号头图）
- **栅格覆盖层:** 暖金 0.04 透明度的列辅助线，仅调试用，生产隐藏
- **Vertical rhythm:** 章节之间用 № 编号 + 章节名英文大写做分隔，不用 HR 线
- **Alignment:** 默认左对齐——参数化风格不居中（除特殊居中 moments 如哲学收尾）
- 留白优先于分隔线

## 5. Layout & Composition

- **顶部固定签名行:** `HW / 化我✦  ·  № <编号> — <身份标签>`
- **章节标题格式:** `№<编号> / <英文大写> / <中文小字>` + 紧跟一行 mute 灰副标
- **参数行结构:** `<英文 KEY> / <值>`，如 `LOCALIZATION / 坐标 GUANGZHOU, GD`
- **编号列表项:** `### 01 / <标题>` + 缩进正文，数字用 Accent 暖金
- **盟友卡:** 品牌 logo + `№<编号> / <角色>` + `✦` 分隔 + 简短英文描述
- **底部版权块:** `© <年> HW / 化我. ALL RIGHTS RESERVED.` + 一句哲学收尾（Bodoni Moda 斜体）
- Hero 区用反色（深黑底 + 暖白字 + 暖金强调）做视觉冲击入口
- **双底切换规则:**
  - `slide--light`（暖白底 #F5F4F0）= 默认主背景，章节正文页、数据明细页
  - `slide--dark`（深黑底 #0E0E0E）= 强调页，用于 Cover、Team、Contact、Market 全图页
  - 切换规则：每 2-3 页 light 之后插一个 dark 做节奏锚点，避免单调
  - Dark 页的暖金 ✦ 符号 / 关键数字 saturate 提升 10%，呼应反差
- 不要用插画装饰图——视觉冲击靠字号对比、留白、✦ 符号、参数行节奏

## 6. Components

- **章节标题:** mono 字体 `№<编号>` + Syne 字体英文大写 + Plus Jakarta 字体中文小字
- **参数行:** mono 字体 + `KEY / 值` 结构 + Mute 暖灰
- **编号列表项:** `### 01 / <标题>` + 缩进正文，数字用暖金
- **盟友卡:** `rounded-xl`、边框、hover 边框变暖金 + `shadow-[0_0_30px_rgba(197,168,128,0.2)]` 光晕
- **CTA 按钮:** `rounded-full`（圆角胶囊）、边框 + 暖金 hover
- **Toast 通知:** `rounded-xl`、深底 #161616、暖白文字、暖金 ✦ 前缀
- **强调符号:** `✦` 用于品牌签名、章节分隔、关键转折——不当装饰撒
- **链接:** 默认下划线 mute 灰，hover 变暖金
- **圆角:** 默认 `rounded-xl`（12px），按钮用 `rounded-full`——不要直角

## 7. Motion & Interaction

- 默认 transition: `duration-300` 到 `duration-500`，用 `transition-colors` / `transition-all`
- hover 状态用 opacity / color 切换，禁用大幅 transform
- `✦` 符号在 hover 时变暖金（200-300ms opacity / color 过渡）
- 章节进入视口时 300-500ms 的 opacity 0 → 100 + translateY(8-20px → 0)
- Lenis 平滑滚动（smooth scroll）
- 盟友卡 hover: 边框变暖金 + 阴影光晕 + 微 scale(1.02-1.1)
- 禁用：弹跳、缩放 > 1.1、阴影晕染过度、渐变过渡、旋转

## 8. Voice & Brand

- **品牌签名:** HW / 化我✦（永远带 ✦）
- **身份标签:** 浪尖领航官、破界青年、精算师思维、AI 智能体探索者
- **反向定义风格:** 用「不做什么」定义「做什么」——
  - "不走任何无意义的内卷套路"
  - "绝不嘲笑任何付出努力的人"
- **数字 + 身份组合:** `№ 26 — 浪尖领航者`、`26.06.10 / 盟友`
- **哲学收尾:** 一句话总结，不解释（用 Bodoni Moda 斜体）——
  - "人生是配得感的修行"
  - "破界前行"
  - "万物化我"
- **节奏:** 短句 + 长句穿插，不堆排比
- 禁用：鸡汤词（赋能 / 生态 / 闭环 / 链路）、营销词（专属 / 尊享 / 臻享）、AI 味词（本质上 / 深度地 / 系统性）

## 9. Anti-patterns

- 不要把 ✦ / № 当装饰随便撒——只在编号、签名、章节标题、关键转折用
- 不要用渐变、毛玻璃（backdrop-blur 可以，但不要做主视觉）
- 不要用插画、emoji、装饰图（除非是数据图/SVG 参数图）
- 不要混入第二种暖色——单一暖金 #C5A880 是品牌锚点
- 不要用直角——默认圆角 `rounded-xl`（12px），按钮 `rounded-full`
- 不要在暖白主背景上用纯黑（#000）——用 #0E0E0E 深近黑
- 不要在同一个画面里出现两种 mono 字体
- 不要省略 ✦——化我的视觉签名就靠它
- 不要用 Bodoni Moda 当正文——只用于特殊 moments
- 不要大幅 transform 动画——克制是化我视觉的核心
