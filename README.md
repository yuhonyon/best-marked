#best-marked
A markdown parser built for speed
> According to the marked to modify



## install
```hash
  npm i best-marked -S
```
* Add Chinese support
* Add the function of toc

## new options
* `tocPrefix:''  //toc class prefix`
* `ordered: true //toc order`
* `depthFrom: 1`
* `depthTo: 3`
* `orderStr:[]` //toc order name e.g [["一","二"...],["a","b","c"..],[1,2,3..]]


## example
code
```js
import marked from 'best-marked'
import highlight from 'highlight.js'

marked.setOptions({
  highlight: function(code) {
    return highlight.highlightAuto(code).value;
  },
  ordered: true,
  depthFrom: 1,
  depthTo: 2,
  orderStr: [
    [
      "一",
      '二',
      '三'
    ],
    [
      "1",
      '2',
      '3'
    ]
  ]
});

marked(mdStr) //out html
```
in
```
[TOC]
# title1
## subtitle1
## subtitle2
```
out
```
<ul>
  <li>
    <a href="#title1"><span>一.</span><span>title1</span></a>
    <ul>
      <li>
        <a href="#subtitle1"><span>1.</span><span>subtitle1</span></a>
      </li>
      <li>
        <a href="#subtitle1"><span>2.</span><span>subtitle2</span></a>
      </li>
    </ul>
  </li>
</ul>

<h1 id="title1">title1</h1>
<h2 id="subtitle1">subtitle1</h2>
<h2 id="subtitle2">subtitle2</h2>
```

------

> 根据marked包修改

## 安装
```hash
  npm i best-marked -S
```
* 添加中文支持(修改对中文不友好代码)
* 添加toc功能

## 新建字段
* `tocPrefix:''  //toc前缀`
* `ordered: true //toc order`
* `depthFrom: 1`
* `depthTo: 3`
* `orderStr:[]` //toc 序号 e.g [["一","二"...],["a","b","c"..],[1,2,3..]]
