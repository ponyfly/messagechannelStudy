通过MessageChannel实现iframe与主页面的通信
+ 主页面建立MessageChannel实例，通过portMessage将port2传递给iframe
+ iframe监听message事件，通过event.ports[0]获取port2
+ iframe通过port2.postMessage发送消息
+ iframe通过port2.onmessage监听消息
+ 主页面通过port1.postMessage发送消息
+ 主页面通过port1.onmessage监听消息
