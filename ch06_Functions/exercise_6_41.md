> 练习6.41：下面的哪个调用是非法的？为什么？哪个调用虽然合法但显然与程序员的初衷不符？为什么？

```
char *init(int ht, int wd = 80, char bckgrnd = ' ');
```

(a) init(); (b) init(24, 10); (c) init(14, '*');

---

(a) 非法，ht必须指定初始值。
(c) 虽然合法，但是却是将'*'隐式转换成int类型然后用于初始化wd，然而其初衷应该是用于初始化bckgrnd的。