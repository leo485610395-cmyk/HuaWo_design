# identity-film-10s · design.md 驱动视频首条验证样本

> 这是把 huawo DESIGN.md 接入 [HyperFrames](https://github.com/heygen-com/hyperframes) 渲染出的第一条品牌片头。
> **定位是「链路验证样本」，不是品牌成品。** 证明 design.md 能驱动视频产出，复利维度从静态图/PPT 扩展到动态视频。

## 文件

| 文件 | 作用 |
|---|---|
| `huawo-identity-film-10s.mp4` | 渲染成品，10 秒，1920×1080，30fps |
| `index.html` | HyperFrames 组合源码（HTML + GSAP 动画） |

## 内容结构（3 场景，10 秒）

| 时间 | 场景 | 视觉 |
|---|---|---|
| 0–3.5s | 品牌符号 | 「化我」大字（Syne 800，320px），「我」字暖金 #C5A880，slogan 从下淡入 |
| 3.5–7s | 哲学收尾 | 「人生是配得感的修行」（Bodoni Moda 斜体），从模糊到清晰 |
| 7–10s | 落款 | 「HW✦」+「万物化我 · 2026」 |

全程显示：顶部签名行 `HW / 化我✦ · № 26 / WAVES PILOT / 浪尖领航官`，底部参数行 `LOCALIZATION / GUANGZHOU, GD`。

## 视觉规范溯源（全部来自 DESIGN.md）

| 维度 | 值 | DESIGN.md 出处 |
|---|---|---|
| 主背景 | `#F5F4F0` 暖白 | §2 Primary |
| 强调色 | `#C5A880` 暖金（「我」字、✦、关键转折） | §2 Accent |
| 文字/反差 | `#0E0E0E` 深近黑 | §2 Secondary |
| 副文字 | `#7A7A77` 暖灰（签名/参数行） | §2 Mute |
| display 字体 | Syne 800 | §3 Families |
| serif 字体 | Bodoni Moda 斜体（仅引言 moment） | §3 Families |
| 参数行字体 | JetBrains Mono | §3 Families |
| 品牌符号 | ✦ + № 编号 + 双语标签 | §5 / §8 |
| 动效 | 淡入 + 微位移 + blur→clear，禁大幅 transform | §7 Motion |

## 怎么复现 / 改这个视频

```bash
# 1. 装 HyperFrames（Node 22+）
npx hyperframes init my-video

# 2. 把本目录 index.html 复制过去覆盖
cp index.html my-video/index.html

# 3. 装依赖（FFmpeg + Chrome Headless）
npx hyperframes doctor          # 体检看缺什么
npx hyperframes browser ensure  # 装 Chrome

# 4. 预览（浏览器实时看）
cd my-video && npx hyperframes preview

# 5. 渲染成 MP4
npx hyperframes render
```

改文案/颜色/节奏：直接编辑 `index.html`，HTML 里的 `data-start` / `data-duration` 控制每个场景的起止时间，`<script>` 里的 GSAP timeline 控制动画。

## 已知限制

- **无音轨**：这条没接 TTS 配音和 BGM（HyperFrames 的 TTS/BGM 是可选依赖，未装）
- **Google Fonts 在线加载**：lint 警告，生产环境建议改本地 @font-face
- **验证性质**：视觉细节可能还需打磨，本样本只证明链路通

---

**这就是数字资产的复利：写一次 DESIGN.md，出图、出 PPT、出视频，风格都锁死在同一套系统里。**
