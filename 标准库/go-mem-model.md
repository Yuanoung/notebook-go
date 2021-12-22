# The Go Memory Model

- `HB` Happens Before

- `NHB` Not Happens Before



1、导入包的Init HB 该包之前，所有包的Init HB main.main



2、协程的创建(go func()()) HB 协程的开始执行；协程的销毁 NHB 宿主的事件



3、no buf channel, receive HB send



4、buf channel

- send HB receive 
- close HB receive
- buf满了，The kth receive on a channel with capacity C happens before the k+Cth send from that channel completes.





[详细链接](https://golang.google.cn/ref/mem)