StorageEvent

+ 是一种Event，可以通过标准的Event监听器操作。
+ 当storage变化时候，事件会被派发到所有同域下的其他页面。
+ 触发变化的当前页面，没有事件派发。


所以，我们可以通过监听storage事件，来实现不同域下的两个页面的通信。

在我们的例子中在child1触发的storage事件，会被child2监听到，从而实现了通信。
同理反过来在child2触发的storage事件，会被child1监听到，从而实现了通信。
