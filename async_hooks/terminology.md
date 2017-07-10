异步资源代表具有回调函数的一个对象. 这个回调函数可以被调用多次, 例如, `net.createServer`
里面的 `connection` 事件, 或者像是 `fs.open` 那样只有一次. 调用回调函数之前资源同样可以
被关闭. AsyncHook 不会明确的区分这些不同的情况, 而是将他们表示为一个资源这种抽象的概念.