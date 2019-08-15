### 软链接与硬链接

参考文章：https://www.jianshu.com/p/dde6a01c4094

- 硬链接： 与普通文件没什么不同，inode 都指向同一个文件在硬盘中的区块。删除其中一个，另一个还在，占用2倍内存。
- 软链接： 保存了其代表的文件的绝对路径，是另外一种文件，在硬盘上有独立的区块，访问时替换自身路径。相当于Windows的快捷方式，Mac OS 的替身。删除原本文件，软链接失效。

```
ln myfile hard     # 硬链接 
ln -s myfile soft  # 软链接
```

![img](image.png)
