[TOC]

# 一、Python文件的两种用途

python文件总共有两种用途，一种是执行文件；另一种是被当做模块导入。

编写好的一个python文件可以有两种用途：

1. 脚本，一个文件就是整个程序，用来被执行
2. 模块，文件中存放着一堆功能，用来被导入使用

```python
# aaa.py

x = 1

def f1():
    print('from f1')


def f2():
    print('from f2')


f1()
f2()
```

```python
# run.py

import aaa
```

如果直接运行run.py会直接运行aaa.py中的`f1()`和`f2()`，但是如果我们在aaa.py中加上`if __name__ == '__main__':`这句话，则可以防止运行run.py时执行`f1()`和`f2()`。因为当aaa.py被直接执行，即当做执行文件的时候`__name__ == '__main__'`； 在aaa.py被当做模块直接运行的时候`__name__ == 'aaa'`。由此可以让aaa.py在不同的场景下有着不同的用法