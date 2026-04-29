# HumanWrite

这个仓库放的是一个写作改写技能。

我主要拿它做两件事：

1. 整理零散笔记
2. 把博客草稿里的 AI 味压下去

中文和英文都能用。

它不追求把文字改得多漂亮，重点是三件事：

1. 原文重点别丢
2. 句子读起来像正常人会写的
3. 需要的话把引用和链接补清楚

## 适合什么

这套技能适合这些场景：

1. 笔记很散，想整理成一篇能读的文章
2. 博客草稿太像模型写的，想把语气压平
3. 原文判断想保留，只想把表达和顺序理顺
4. 要做改写前后对比
5. 要把查到的文章观点接进正文，再把链接补到对应句子后面

## 不适合什么

这些情况我一般不用它：

1. 正式公文
2. 学术论文
3. 法律条文整理
4. 只查资料，不改文字

## 目录结构

目录不复杂，主要是把规则拆开，后面好改。

```text
humanwrite/
├── SKILL.md
├── README.md
├── GITHUB-LAUNCH.md
├── agents/
│   └── openai.yaml
└── references/
    ├── ai-patterns.md
    ├── analysis-lenses.md
    ├── examples.md
    ├── forbidden-phrases.md
    └── scoring.md
```

各文件的作用是这样：

`SKILL.md`

- 主文件
- 写触发条件、边界、工作顺序、自检

`README.md`

- 给人看的说明页
- 讲这个技能大概做什么，目录怎么分

`GITHUB-LAUNCH.md`

- 发 GitHub 时直接用的材料
- 里面放了仓库名、描述、topics、发帖文案

`agents/openai.yaml`

- 放展示名、短描述、默认提示词

`references/forbidden-phrases.md`

- 放禁用词、禁用句式、禁用结构

`references/examples.md`

- 放触发例子、正反例、前后对比

`references/ai-patterns.md`

- 放常见 AI 写作模式

`references/scoring.md`

- 放五十分评分体系

`references/analysis-lenses.md`

- 只有在要往深处拆的时候才用
- 平时改笔记和博客，不一定每次都要读

## 怎么用

我自己用的时候，顺序很简单。

先看原文到底想说什么，再把 AI 味最重的句子挑出来，然后才开始改。  
如果原文重点很多，我会先列重点，再动笔。  
如果里面有引用，我会把链接补到对应句子后面，不放到文末糊成一团。

## 英文场景

英文也能用。

主要处理这些问题：

1. 句子太像演讲稿
2. 空提示词太多
3. 品牌文案味太重
4. 结构太整齐，读起来发假

## 参考过的项目

我参考过一些相近的技能和仓库，主要看它们怎么写触发条件、怎么摆示例、怎么做前后对比：

1. [Aboudjem/humanizer-skill](https://github.com/Aboudjem/humanizer-skill)
2. [blader/humanizer](https://github.com/blader/humanizer/blob/main/SKILL.md)
3. [labarba/sciwrite](https://github.com/labarba/sciwrite)
4. [openclaw/skills docs-style](https://github.com/openclaw/skills/blob/main/skills/anderskev/docs-style/SKILL.md)

我自己的这套，重点还是放在笔记整理和博客输出，不是做品牌文案，也不是做花哨写作。
