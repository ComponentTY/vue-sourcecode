## Vue的数据驱动，响应式数据原理是什么？

- ##### 什么叫数据驱动？

开发人员把重点放在数据及逻辑上，不需要再去关心视图的变化，通过数据的变更动态修改dom，达到数据影响视图的目的。

- ##### Vue的数据驱动原理是什么？

在mountComponent函数中有一个updateComponent函数，他的作用就是将render函数转为VNode，并且派发更新到真是dom上。这些内容后面说，mountComponent函数中最后调用了new Watcher，实例化了一个watcher，这个watcher