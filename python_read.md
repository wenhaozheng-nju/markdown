python 读书笔记
================

# 列表推导
` [i for i in range(10) if i % 2 == 0] `


## enumerate 的使用:

    seq = ["one", "two", "three"]
    for element in seq:
        seq[i] = '%d: %s' % (i, seq[i])
        i+= 1

    def _treatment(pos, element):
        return '%d: %s' % (pos,element)
    seq = ["one","two","three"]
    [_treatment(i,el) for i, el in enumerate(seq)]

## 生成器:

    def fibonacci():
        a,b = 0,1
        while True:
            yield b
            a,b = b, a+b

    fib = fibonacci()
    [fib.next() for i in range(10)]

有了yield的函数将不再是普通函数，其会返回一个迭代器，而且会在执行到yield的时候停止，下次调用时再接着执行，有点类似于*中断*


