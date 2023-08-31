家人们快来更新旅游攻略吧，万一有一天真能一起出去玩呢🥰 

# 关于JourneyRightNow 🚀
JourneyRightNow是一个公开的（到目前为止）共享文档，供大家上传旅行记录、推荐旅行路线以及查阅攻略。
&nbsp;
**目前所有的内容都会被放置在Journey.md中**。那是一个markdown文档，markdown是一种记录语言格式，方便我们更好地排版。

# 提交提醒
**如果您是我们的一员**，您有权限直接提交（commit）这份文档的修改稿（可以直接在线编辑）。不过，提交时请注意格式，不要弄乱这份文档。如果您提交了错误的版本，您可以在github上回退文档版本。
&nbsp;
如果您不是我们的一员，您将只有阅读的权限，没有修改的权限。**请不要尝试提交！** 谢谢您的配合，并希望这份文档能帮助你获得更好的旅行体验。

# 提交步骤
## 确认权限
请确认您是我们的一员并且GitHub账号已经被认证。
不是我们的成员的账号的任何commit都会被删除。

## 后面的让lhy来写，你应该会用markdown吧
&nbsp;
&nbsp;
# Markdown指南

Markdown是一种轻量级标记语言，它以纯文本形式编写文档。markdown排版方便、美观，兼容性非常好（几乎完胜word）。

## 绝佳的兼容性

markdown兼容html超文本标记语言，也兼容Latex公式，支持内嵌媒体。目前主流网站框架都支持markdown编写，甚至作为唯一方式。

markdown文件（.md文件）需要一个编译器。目前，VSCode、Cursor等编辑器都支持markdown编译插件，不仅可以做到实时预览，而且能够到处pdf、html等一众格式。

Typora、GoodNote、OneNote和Notion等笔记软件也几乎都支持markdown。
&nbsp;
## 纯文本编辑
您可以把markdown当成txt使用，直接输入文字即可，得到的效果就是现在您正在阅读的正文部分，没有任何格式。

如果要为文档添加格式，需要用到简单的markdown语法。
## 基本语法
### 标题
在标题文字前加#即可（空格不能省略）：
```markdown
# 这是一级标题
## 这是二级标题
### 这是三级标题
``` 
以此类推
&nbsp;
### 加粗
使用两个星号表示加粗：
```markdown
**要加粗的内容**
```
效果就是：
**要加粗的内容**
&nbsp;
### 斜体
把文字左右分别用一个*号包起来：
```markdown
*倾斜的文字*
```
效果如下：
*倾斜的文字*

**如果要同时斜体和加粗，则用三个星号即可。**
&nbsp;
### 换行
正常换行用回车键即可。但是有时需要连空多行，markdown只会执行一个换行。这时需要用到`&nbsp;`
&nbsp;
### 删除线
要加删除线的文字左右分别用两个~~号包起来：
```markdown
~~要删除的文字~~
```
效果如下：
~~要删除的文字~~
&nbsp;
### 引用
```markdown
> 这是一级引用
>> 这是二级引用
>>> 这是三级引用
```
效果如下：
> 这是一级引用
>> 这是二级引用
>>> 这是三级引用
&nbsp;
### 列表
前导+、-、*均可。列表分级用tab。
```markdown
+ 这是一级列表
    + 这是二级列表
        + 这是三级列表
```
效果如下：
+ 这是一级列表
    + 这是二级列表
        + 这是三级列表

如果要有编号，则在编号后加点即可：
```markdown
1. 这是一级列表
2. 这是一级列表
    1.  这是二级列表
        1. 这是三级列表
```
效果如下：
1. 这是一级列表
2. 这是一级列表
    1. 这是二级列表
        1. 这是三级列表
&nbsp;
### 表格

```markdown
|表头|表头|表头|
|---|---|---|
|内容|内容|内容|
|内容|内容|内容|
```
效果如下：
|表头|表头|表头|
|---|---|---|
|内容|内容|内容|
|内容|内容|内容|
&nbsp;
### 内嵌媒体
如果要内嵌图片视频等，建议直接使用复制粘贴的办法。**这要求图片必须是网络图片，或图片与md文档必须位于同一文件夹下。**
所以上传时，要把图片或视频也一起上传。
&nbsp;
### Latex公式
markdown支持内嵌latex公式。
> 所有的Latex语法都可见于https://www.cnblogs.com/1024th/p/11623258.html

公式内容用两个$包起来：
```markdown
$牛顿第二定律：F=\frac{\text{d}p}{\text{d}t}$
```
效果就是$牛顿第二定律：F=\frac{\text{d}p}{\text{d}t}$
如果要求公式单独成行，就要用两个$$$包起来：
```markdown
$$牛顿第二定律：F=\frac{\text{d}p}{\text{d}t}$$
```
效果就是：$$ 牛顿第二定律：F=\frac{\text{d}p}{\text{d}t} $$
&nbsp;
### 分割线
三个或者三个以上的 - 或者 * 或者_都可以。
```markdown
---
***
___
```
效果就是：

---
***
___

&nbsp;
### 代码和代码块
把代码用`包起来：
```markdown
`print("hello,world)`
```
效果就是行内代码：`print("hello,world)`
如果需要代码块，就用三个```包起来：
```markdown
    ```python
    print("hello,world)
    print("\n")
    ```
```
在第一个```后加上代码的语言名称，可以实现高亮。
```py
print('hello,world')
print("\n")
```


