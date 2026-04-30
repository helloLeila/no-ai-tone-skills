# no-ai-tone-skills

`no-ai-tone-skills` 是一个去AI味改写通用技能，主要拿来整理AI生成的内容笔记成笔记或者博客，改掉 AI 生成文本里的模型腔，目前AI回复会生成海量的信息，如果不加以整理很快会过眼云烟，吐出的token也浪费了，所以这个技能帮助AI输出成笔记或者博客的口吻。

这套技能更适合内容已经有了、表达还不顺的时候。原文重点要保住，顺序能理顺就理顺，正文里有引用的话，就把链接补到对应句子后面。

中文和英文都能用，平时更适合笔记、博客、评论、说明文这类文本，公文、论文、法律条文不放在这里处理。

## 这套技能做什么

常见用法基本就是这几类：

- 把零散笔记整理成一篇能读的文章
- 把博客草稿里的模型腔压下去
- 保留原文判断，只整理表达和顺序
- 给正文补来源链接
- 做改写前后对比

如果只是查资料，不改文字，这套技能就用不上。

## 适合什么文本

笔记、博客草稿、技术总结、评论、说明文、知识库草稿都适合。英文笔记和英文博客草稿也可以直接用。英文场景里，常见问题通常是句子太像演讲稿，空提示词太多，或者品牌文案味太重。

## 怎么装

如果你在本地用 skills，目录放进去就行。

```bash
skills/
  no-ai-tone-skills/
```

如果你已经有技能安装器，也可以按你自己的方式挂进去。这里不绑定某一个平台的安装命令，目录结构保持完整就行。

## 怎么用

直接这样用就行：

```text
帮我把这段笔记整理成一篇能发博客的版本。
帮我去掉这段中文里的 AI 味，保留原意。
原文重点不要动，你可以调顺序。
帮我把查到的文章观点补进去，并把原文链接放好。
Rewrite this in plain English and keep the original point.
```

我自己用的时候，先看原文到底要说什么，再把最像模型口播的句子挑出来。原文重点如果很多，就先列重点，再开始改。改的时候不追求把句子修得多漂亮，先把假、满、硬这些感觉压下去。原文里有引用，就把链接补到对应句子后面，不往文末堆一串网址。

## 文件怎么分

目录不复杂，主要是把规则拆开，后面好改。

```text
no-ai-tone-skills/
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

`SKILL.md` 是主文件，触发条件、改写边界、工作顺序、自检都放在这里。`GITHUB-LAUNCH.md` 放的是发 GitHub 时直接能用的材料，像仓库名、描述、topics 和发帖文案。`agents/openai.yaml` 管展示名、短描述和默认提示词。

`references` 目录放的是展开内容。`forbidden-phrases.md` 记禁用词和禁用句式，`examples.md` 放触发例子、正反例和前后对比，`ai-patterns.md` 收常见 AI 写作模式，`scoring.md` 放五十分评分体系。`analysis-lenses.md` 只有在要把问题继续往深处拆的时候才会用到。

## 这套技能现在管到什么程度

现在已经把几层东西拆开了：

- 禁用词和禁用句式
- 常见 AI 写作模式
- README 和说明文的特殊约束
- 50 个触发例子
- 五十分评分
- 深度分析视角

这套规则管的不只是句子顺不顺，也会处理说明文里那种整齐口播感、硬分类句、反转句和空过渡词。

## 参考过的项目

README 的结构，我参考过一些同类仓库，主要看它们怎么摆项目简介、安装、用法和文件说明。你刚提到的 [Humanizer-zh](https://github.com/op7418/Humanizer-zh) 这一版有几个地方值得学：首页第一屏比较直，安装和使用说明放得靠前，文件说明也比较完整。我把这些结构上的优点吸收进来了，没有照着它的口气写。

另外也看过这些：

- [Aboudjem/humanizer-skill](https://github.com/Aboudjem/humanizer-skill)
- [blader/humanizer](https://github.com/blader/humanizer/blob/main/SKILL.md)
- [labarba/sciwrite](https://github.com/labarba/sciwrite)
- [openclaw/skills docs-style](https://github.com/openclaw/skills/blob/main/skills/anderskev/docs-style/SKILL.md)
