车牌分离下载脚本
===================

从一堆文字中分离出车牌，并获取磁力连接

Written by clojure.（我为什么要用 `clojuer` 写脚本咧？我肯定是疯了吧...)

Usage:
---------------

1. install [boot-clj](https://github.com/boot-clj/boot)
2. start boot repl
3. run `download-bangumi` function in repl.( see belowe)

-------------

Test in Liunx. (Ubuntu 14.04)

Test in Windows.

-------------------

Use script in repl
-------------------------

```clojure
boot.user>  (dowenload-bangumi "input.file" "output.file")
```


问题
----------------

1. 直接执行脚本，没有结果写入 `output file`. 脚本中的发送请求和接受请求在是在别的线程中执行的，所以主线程（-main)在没有结果返回时就执行结束了，接受到的请求无法写入`output-file`
2. 在分析完成文本中的车牌以后，将结果显示出来
3. 增加选项，只显示分析结果，不不进行获取 `magnet`.
