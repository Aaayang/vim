# vim

## 模式

```
// 普通模式
vim test
```

```
// 插入模式
i
```

```
// 命令行模式
ESC => : => wq aaa.txt
```

i 插前
a 插后
:
wq
esc = ctrl + [


:e a.txt 命令行模式下打开文件

j 下
k 上
h 左
l 右
w 下一个单词
b 上一个单词


i 光标前
I 行首
A 行尾
a 光标后
o 后一行
O 前一行
cw 删除从当前开始到一个单词的最后


:w 文件名 可以另存为一个新的文件



:q! 强制退出不保存
:q 退出
:wq! 强制退出并保存

:w <文件路径> 另存为
:saveas <文件路径> 另存为
:x 保存并推出
:wq 保存并推出

Shift + zz 普通模式下退出


x/Delete 删除游标字符
X 删除游标前一个字符


cw/dw 删除从当前开始到一个单词的最后，不适用与中文

d$/D 删除至行尾

d^ 删除至行首

dG 删除至文档末尾

d1G 删除至文档首部


2dd 删除两行

10x 删除10个字符
3dd 删除3行


dw/daw(delete a word) 删除一个单词
dnw 删除n个单词，n替换为数字




:set nu 显示行号

nG 普通模式想，游标移动到第n行

gg 游标移动到第一行
G  游标移动到最后一行


Ctrl+o 快速回到上一次光标所在位置

// 行内跳转

b 单词的开头
e 单词的结尾
w 下一个单词的开头

ge 前一个单词结尾

0/^ 行头
$   行尾


f<字母> 向后搜索字母并跳转到第一个匹配的位置
F<字母> 向前搜索字母并跳转到第一个匹配的位置

t<字母> 向后搜索<字母>并跳转到第一个匹配位置之前的一个字母
T<字母> 向后搜索<字母>并跳转到第一个匹配位置之前的一个字母


~ 将游标所在字母换成大/小写



v 进入试图模式，y 复制一个字符

yy 复制游标所在的整行
y^/0 复至行首，不包含光标所在字符
y$ 复至行尾，含光标所在位置

yw 复制一个单词
y2w 复制两个单词
yG 复制至文档末
y1G 复制至文档开头

普通模式使用p粘贴至光标下
P粘贴至光标上

dd 其实是剪切，而非单纯删除

ddp 快速交换光标所在行与他下面的行，先删除再粘贴也好理解



r+<待替换字母> 将游标所在字母替换为指定字母

R 连续替换直到按下Esc

cc 替换整行，即删除游标所在行，并进入插入模式

cw 替换一个单词，即删除一个单词，并进入插入模式

C 替换游标以后至行末，就是删除，多了一个自动进入插入模式

~ 反转游标所在字母大小写

u{n} 撤销一次或n次操作

U 撤销当前行的所有修改



```
// 快速缩进

>> 向右缩进
<< 向左缩进
```

:set shiftwidth=10 设置缩进为10个字符

:ce 命令使本行内容居中
:ri 居右
:le 居左


// 查找

/<内容> 向下查找
?<内容> 向上查找
n 向下继续查找
N 向上继续查找

\* 向下寻找游标所处的单词
\# 向上寻找游标所处的单词

g\* 部分符合该单词即可
g\# 同上


// 多文件编辑

vim 1.txt 2.txt
默认进入1.txt 的编辑页面
:n 进入2.txt
