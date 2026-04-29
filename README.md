# HumanWrite

这个仓库放的是一个写作改写技能。我平时用它整理笔记，也用它改博客草稿。很多草稿卡在表达上，句子太像模型口播，读起来发满、发硬、发假。这个技能就是拿来收这种地方的。

中文和英文都能用。它处理的是笔记、草稿、博客这类文字。公文、论文、法律条文我会单独处理，不放在这里。

用的时候我只盯几件事：原文重点别丢，顺序能理顺就理顺，模型腔压下去，正文里有引用的话，把链接补到对应句子后面。大概就是这么简单。

## 什么时候会用到

笔记很散，想整理成一篇能读的文章时，适合用它。博客草稿太像模型写的，想把语气压平时，也适合用它。原文判断想保留，只想把表达理顺，或者正文里已经带了引用，想把来源补清楚，也都可以放进这套技能里。

## 目录

目录不复杂，主要是把不同功能拆开，后面改起来省事。

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

`SKILL.md` 是主文件，触发条件、改写边界、工作顺序、自检都放在这里。`README.md` 就是这页，给人看。`GITHUB-LAUNCH.md` 放的是发 GitHub 时直接能用的材料，像仓库名、描述、topics 和发帖文案。`agents/openai.yaml` 只管展示名、短描述和默认提示词。

`references` 目录里放的是展开内容。`forbidden-phrases.md` 记禁用词和禁用句式，`examples.md` 放触发例子、正反例和前后对比，`ai-patterns.md` 收常见 AI 写作模式，`scoring.md` 放五十分评分体系。`analysis-lenses.md` 平时不一定每次都读，只有要把问题继续往深处拆的时候才会用到。

## 我怎么用

我自己用的时候，先看原文到底要说什么，再把最像模型口播的句子挑出来。原文重点如果很多，我会先列重点，再开始改。改的时候不追求把句子修得多漂亮，先把假、满、硬这些感觉压下去。原文里有引用，就把链接补到对应句子后面，不往文末堆一串网址。

## 英文场景

英文场景也能用。常见情况就是句子太像演讲稿，空提示词太多，品牌文案味太重，或者结构整齐得太用力，读起来发假。

## 参考过的项目

我参考过一些相近的技能和仓库，主要是看它们怎么写触发条件，怎么摆示例，怎么做前后对比。这里留几个链接，后面要继续改可以顺手回去看：

[Aboudjem/humanizer-skill](https://github.com/Aboudjem/humanizer-skill)  
[blader/humanizer](https://github.com/blader/humanizer/blob/main/SKILL.md)  
[labarba/sciwrite](https://github.com/labarba/sciwrite)  
[openclaw/skills docs-style](https://github.com/openclaw/skills/blob/main/skills/anderskev/docs-style/SKILL.md)

我自己的这套还是围着笔记整理和博客输出转，重点一直放在实用和好改。
