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

图片:

![picture](./test.jpg)
