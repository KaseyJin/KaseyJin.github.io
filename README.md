# Kasey Jin · Personal Archive

金鑫怡的个人主页 —— 一个单文件的个人档案、研究展示与持续探索记录。

**在线访问：https://kaseyjin.github.io**

不是简历模板，气质更接近「编辑杂志 × 学术档案 × 个人展览」：克制的排版、大面积留白、细线分隔，以及散落在各处的小号英文元信息。

---

## 页面结构

| 章节 | 内容 |
|---|---|
| **I · Opening** | 姓名、专业背景、自述、兴趣标签与个人金句 |
| **II · Research** | 论文档案卡（未发表草稿）、研究问题与方法、内嵌 SVG 研究流程图，可展开完整档案 |
| **III · Selected Works** | Liteasy、Anki Clipper 两个项目，含界面截图，可展开项目详情 |
| **IV · Journey** | Study（人大）／ Practice（四段校园与实践经历）／ Internship |
| **V · Open Field** | 三个仍在进行中的探索方向 |

---

## 技术说明

整个网站**只有一个 `index.html`**，双击即可打开，无需服务器、构建步骤或任何安装。

- 纯原生 HTML / CSS / JavaScript，没有 React、Vue、Tailwind、jQuery 等任何框架
- 没有 npm、构建工具、CDN、外部字体、外部样式表或外部脚本
- 没有后端、数据库与 API，页面运行时不发起任何网络请求
- 全部 6 张图片以 Base64 Data URI 内嵌，仓库内不存放图片文件

### 视觉系统

两套独立配色，通过 CSS 变量切换，过渡约 560ms：

- **日间** — 暖白纸张底色、深棕黑文字，用多层径向渐变模拟纸张受光与纹理
- **夜间** — 深森林绿底、暖白标题、灰绿辅助文字，配一层近乎静止的绿色光晕。不是简单的颜色反转，也不使用纯黑或霓虹色

主题选择存入 `localStorage`，刷新后保持。

### 交互

- 锚点导航与平滑滚动，当前章节自动高亮（`IntersectionObserver`）
- 滚动渐显，同组元素依次错开
- 论文与项目档案可展开，支持关闭按钮 / 点击遮罩 / `Esc` 三种关闭方式，带焦点捕获与焦点归还
- 返回顶部按钮、手机端折叠菜单

### 可访问性

语义化标签、ARIA 属性、完整的键盘可达性与可见焦点样式。全站尊重 `prefers-reduced-motion`：开启后渐显与动画不会触发，内容直接呈现。禁用 JavaScript 时页面内容同样完整可读。

### 响应式

桌面端最大宽度 1280px，Journey 使用不规则杂志式网格；窄屏逐级降为双列与单列，无横向滚动。

---

## 本地预览

克隆后双击 `index.html` 即可，没有任何依赖需要安装。

```bash
git clone https://github.com/KaseyJin/KaseyJin.github.io.git
```

修改 `index.html` 后 `git push`，GitHub Pages 会在一两分钟内自动更新线上页面。

---

## 说明

- Research 章节的论文为**未发表草稿**（Working Paper / Draft in Progress），页面不提供全文与下载
- 尚未确认的时间、职责与成果在页面上标注为「待补充」，未作虚构
- 原始图片素材不纳入版本库（见 `.gitignore`），页面所需图片均已内嵌
