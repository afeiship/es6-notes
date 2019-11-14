# es6 introdocution

## why es6
- ECMAScript 6.0（以下简称 ES6）
- JavaScript 语言的下一代标准，已经在 2015 年 6 月正式发布了。

## ECMAScript 和 JavaScript 的关系是
- 前者是后者的规格，后者是前者的一种实现（另外的 ECMAScript 方言还有 JScript 和 ActionScript）
- 日常场合，这两个词是可以互换的

## ES6 与 ECMAScript 2015 的关系
~~~
ES6 的第一个版本，就这样在 2015 年 6 月发布了，正式名称就是《ECMAScript 2015 标准》（简称 ES2015）。
2016 年 6 月，小幅修订的《ECMAScript 2016 标准》（简称 ES2016）如期发布，这个版本可以看作是 ES6.1 版，因为两者的差异非常小（只新增了数组实例的 `includes` 方法和指数运算符），基本上是同一个标准。
根据计划，2017 年 6 月发布 ES2017 标准。

因此，ES6 既是一个历史名词，也是一个泛指，含义是 5.1 版以后的 JavaScript 的下一代标准，涵盖了 ES2015、ES2016、ES2017 等等，而 ES2015 则是正式名称，特指该年发布的正式版本的语言标准。本书中提到 ES6 的地方，一般是指 ES2015 标准，但有时也是泛指“下一代 JavaScript 语言”。
~~~

## 语法提案的批准流程
~~~
任何人都可以向标准委员会（又称 TC39 委员会）提案，要求修改语言标准。
一种新的语法从提案到变成正式标准，需要经历五个阶段。每个阶段的变动都需要由 TC39 委员会批准。
~~~

Stage 0 - Strawman（展示阶段）
Stage 1 - Proposal（征求意见阶段）
Stage 2 - Draft（草案阶段）
Stage 3 - Candidate（候选人阶段）
Stage 4 - Finished（定案阶段）

> 一个提案只要能进入 Stage 2，就差不多肯定会包括在以后的正式标准里面。ECMAScript 当前的所有提案，可以在 TC39 的官方网站

## Harmony 代号的由来
2008 年 7 月，由于对于下一个版本应该包括哪些功能，各方分歧太大，争论过于激烈，ECMA 开会决定
中止 ECMAScript 4.0 的开发，将其中涉及现有功能改善的一小部分，发布为 ECMAScript 3.1
而将其他激进的设想扩大范围，放入以后的版本，`由于会议的气氛，该版本的项目代号起名为 Harmony（和谐）`
会后不久，ECMAScript 3.1 就改名为 ECMAScript 5


## 部署进度
> 查看 node 环境对相关特性的支持情况。
node --v8-options | grep harmony

## Babel 转码器
- Babel 的配置文件是.babelrc，存放在项目的根目录下。使用 Babel 的第一步，就是配置这个文件。
  ```json
  {
    "presets": [
      "@babel/env",
      "@babel/preset-react"
    ],
    "plugins": []
  }
  ```
- presets字段设定转码规则，官方提供以下的规则集，你可以根据需要安装。

