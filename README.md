2014.05.14--linux-vim
=====================

第一级 – 存活
-------------

安装 vim

启动 vim

什么也别干！请先阅读

当你安装好一个编辑器后，你一定会想在其中输入点什么东西，然后看看这个编辑器是什么样子。但vim不是这样的，

请按照下面的命令操作：

启 动Vim后，vim 在 Normal 模式下。
    

让我们进入 Insert 模式，请按下键i。

此时，你可以输入文本了，就像你用“记事本”一样。

如果你想返回 Normal 模式，请按 ESC 键。

现在，你知道如何在 Insert 和 Normal 模式下切换了。下面是一些命令，可以让你在 Normal 模式下幸存下来：


i → Insert 模式，按 ESC 回到 Normal 模式.

x → 删当前光标所在的一个字符。

:wq → 存盘 + 退出 (:w 存盘, :q 退出)   （ ps: :w 后可以跟文件名 ）

dd → 删除当前行，并把删除的行存到剪贴板里

p → 粘贴剪贴板


第二级 – 感觉良好
-------------

上面的那些命令只能让你存活下来，现在是时候学习一些更多的命令了，下面是我的建议：（所有的命令
都需要在Normal模式下使用，如果你不知道现在在什么样的模式，你就狂按几次ESC键）

各种插入模式

a → 在光标后插入

o → 在当前行后插入一个新行

O → 在当前行前插入一个新行

cw → 替换从光标所在位置后到一个单词结尾的字符

简单的移动光标

0 → 数字零，到行头

^ → 到本行第一个不是blank字符的位置（所谓blank字符就是空格，tab，换行，回车等）

$ → 到本行行尾

g_ → 到本行最后一个不是blank字符的位置。

/pattern → 搜索 pattern 的字符串（陈皓注：如果搜索出多个匹配，可按n键到下一个）

拷贝/粘贴 （陈皓注：p/P都可以，p是表示在当前位置之后，P表示在当前位置之前）

P → 粘贴

yy → 拷贝当前行当行于 ddP

Undo/Redo

u → undo

<C-r> → redo

打开/保存/退出/改变文件(Buffer)

:e <path/to/file> → 打开一个文件

:w → 存盘

:saveas <path/to/file> → 另存为 <path/to/file>

:x， ZZ 或 :wq → 保存并退出 (:x 表示仅在需要时保存，ZZ不需要输入冒号并回车)

:q! → 退出不保存 :qa! 强行退出所有的正在编辑的文件，就算别的文件有更改。

:bn 和 :bp → 你可以同时打开很多文件，使用这两个命令来切换下一个或上一个文件。    



第三级 – 更好，更强，更快
-------------

先恭喜你！你干的很不错。我们可以开始一些更为有趣的事了。在第三级，我们只谈那些和vi可以兼容的命令。

###更好###

. → (小数点) 可以重复上一次的命令

N<command> → 重复某个命令N次

2dd → 删除2行

3p → 粘贴文本3次

下面是一个示例，找开一个文件你可以试试下面的命令：

    100idesu [ESC] → 会写下 “desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu       desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu       desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu       desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu desu       desu desu desu desu desu desu desu desu desu desu desu desu desu “

. → 重复上一个命令—— 100 “desu “.

输入3. → 重复 3 次 “desu” (注意：不是 300，你看，VIM多聪明啊).
