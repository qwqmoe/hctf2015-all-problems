# 教务处

貌似很多人认为这个是个web题Orz。

这道题目应该是最好玩的题目了。

首先是`strncpy`函数的一个大坑。这个函数不保证添加结尾0.所以只要构造一下，就可以让strlen函数返回的长度大于0x80.然后我长度是用一个byte储存的。这就造成的整形溢出。然后就是标准的堆溢出流程了。