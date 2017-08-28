# rx-hub

> 通过`水池`，集中管理和监视 `数据流`， 将数据当作 `水流`一样来管理。

> 数据从`数据源`流出（比如一个点击事件流），在不同的`水管`中流动变换，最终流向`目的地`(比如界面UI)。

> 依赖[RxJS][https://github.com/ReactiveX/RxJS]。

## Overview

![rx-hub data flow](ccqgithub.github.io/res/imgs/rx-hub-flow.jpg).

- `Hub`: 水流集散中心（数据中转中心），用来安装监听各种数据流动，所有的数据流必须经过此处。
- `Pipe`: 水管（数据管道），安装在`Hub`之上，每一个`Pipe`可以将流入的数据进行变换，然后流出。
- `Converter`: 换流站（数据变换），一个`Pipe`应该有一个`Converter`，一个`Converter`可以被多个`Pipe`复用。
- `Store`: 水池（数据持久存储），

## 结构

- sources： 数据源
- dests：数据修改目的地
- actions：沟通交流数据源 和 数据目的地
