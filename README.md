家人们快来更新旅游攻略吧，万一有一天真能一起出去玩呢🥰 

# 关于JourneyRightNow 🚀
JourneyRightNow是一个公开的（到目前为止）共享文档，供大家上传旅行记录、推荐旅行路线以及查阅攻略。

`旅游路线推荐`文件夹下，每一个文件都是一条推荐的旅游路线。**您在提交时，提交备注必须是您的署名（或其他任何您愿意的名字）**。当然这个文件夹下**也欢迎单纯推荐景点**（而不能组成一条完整可行的路线）。Every step counts！

`旅游攻略`文件夹下，您可以提交旅游攻略和旅游经历。由于有些攻略或经历会携带照片，为整齐起见，每一份攻略都单独成一个文件夹。**您在提交时，提交备注必须是您的署名（或其他任何您愿意的名字）**。

`饭店推荐.md`文件，您可以向其中提交您推荐或不推荐的餐馆。格式已经附在文件中了，请按照格式编辑。

---

# 提交提醒
+ **如果您是我们的一员**，您有权限直接提交（commit）这份文档的修改稿（可以直接在线编辑），或者git clone至本地后修改提交。**请注意，每次提交时的备注必须是您的署名！这有助于一目了然看出每个文档的作者。如果您一定要在备注里写其他内容，务必在文档文件名里署名**。如果您提交了错误的版本，您可以在github上回退文档版本。

+ **如果您不是我们的一员**，那么我们更推荐您只是阅读这些文档（当然，我们欢迎您的到访）。如果您觉得**有必要**添加一些修改，请您严格按照格式撰写，并提出pull request。感谢您的配合，并希望这份文档能帮助你获得更好的旅行体验。

# 提交步骤
并入之后的Git教程一起讲解。

# **Git**
## 安装Git
  前往 `git-scm.com` 下载git的安装包
  @import "GitNote\Img\capture_20230901230901739.bmp"
  在运行时注意该选项选择`Visual Studio Code` 这将方便后续的文本编辑
  @import "GitNote\Img\capture_20230901230807024.bmp"
  其余选项均为默认，一路左键。
  安装完成后，选择一个空文件夹并右键，会有 `Open Git GUI here` & `Open Git Bash here` 的选项，我们一般选用 `Open Git Bash here` ，下文也以此为例。
  @import "GitNote\Img\2023-09-01 231440.png"

---
## 安装Github桌面端
  由于使用命令行工具（Powershell、Git Bash等）时，梯子无法为它们提供代理服务，所以会导致出现无法从本地连接到远程仓库的问题
  @import "GitNote\Img\capture_20230902094737792.bmp"
  所以我们需要下载Github Desktop
  @import "GitNote\Img\capture_20230902094940511.bmp"
  在该软件内，可以使用梯子稳定访问远程仓库。

---
## 主要操作
- ### 创建一个本地 Repository(仓库) 或者 Remote   Clone an Existing Repository from Remote
  首先我们需要设置 `user.name` and `user.email`，如下图，用`git config --global`指令来设置。
  @import "GitNote\Img\capture_20230816194548760.bmp"
  - 如果我们希望在本地创建一个Repository（可以理解为一个由git来掌管的文件夹，内含一个隐藏文件夹`.git `）
  @import "GitNote\Img\capture_20230816200122993.bmp"
  我们使用`git init` 命令来使当前文件夹成为一个新的Repository *(因为我已经创建过Repository了所以图中报错了)*
  @import "GitNote\Img\capture_20230816195605712.bmp"
  - 如果我们希望将Remote（远程仓库）如：Github、Gitlab等中的内容复制到本地，以便本地编辑，我们先获取远程仓库的URL
  @import "GitNote\Img\capture_20230901223446253.bmp"
  然后使用`git clone URL` 命令将URL所指的远程仓库克隆至本地，系统会创建一个名为仓库名的文件夹(克隆时需挂梯子)。
  @import "GitNote\Img\capture_20230901223918741.bmp"

- ### `Add` & `Commit` 操作
  现在，我们将于本地开始使用该仓库, 我们创建一个  `File.txt` 作为例子。
  @import "GitNote\Img/image.png"
  我们可以使用 `git status` 命令来查询工作区的状态（有无文件被修改，修改操作的概要，有无文件被同步等等）
  @import "GitNote\Img\capture_20230816200943877.bmp"
  这里显示该仓库中有一个“未被追踪的文件” *Untracked file --- File.txt* （意指文件被修改但是该修改没有被暂存并且没有被提交） 

  使用 `git add File.txt` 命令来将文件的修改操作移动至暂存区（“暂存区”概念与“工作区”相对，修改操作只有在移动至暂存区后才可以被Commit提交）
  @import "GitNote\Img\capture_20230816201604214.bmp"
  然后使用 `git commit` 命令来提交所有处于暂存区的修改操作。

  在这一步，系统会自动打开一个编辑器（Powershell、VScode等）来让我们编辑 *Commit Message* 提交信息（通常包含了对于修改操作的概括与解释）. 此处我们的提交信息是 "Add 'Version1' " 编辑完毕后点击右上角的 `√` 。
  @import "GitNote\Img\capture_20230816201749609.bmp"
  @import "GitNote\Img\capture_20230816201820192.bmp"

- ### Create New Branches and Merge 创建新的分支以及合并
  使用 `git branch newbranchName` 来从Master（Github上默认为Main）分支或者其他分支处创建一个新的分支。

  使用 `git checkout targetbranchName` 命令来将工作区范围移动至目标分支，下图中我们新建了`new` 分支，并移动至该分支。
  @import "GitNote\Img\capture_20230816202221579.bmp"
  新创建的分支会复制Master/Main（或者其他源分支）内的所有内容。现在我们来编辑`new`中的文件内容。
  @import "GitNote\Img\capture_20230816202525641.bmp"
  然后提交。

  这里，我们使用  `git commit -m "message"` 命令来简化编辑 *Commit Message* 的过程（`-m` 之后的字符串即 *Commit Message* ）
  @import "GitNote\Img\capture_20230816202819727.bmp"
  然后我们再切换至 `Master` 分支

  使用 `git merge targetbranchName` 命令来将目标分支合并至当前分支。
  @import "GitNote\Img\capture_20230816203143206.bmp"
  但是如果两个分支在其相同位置存在不同的修改操作，这将会导致 *Merge Clash* 合并冲突。比较复杂，这里不做解释。

- ### `Ignore` 操作
  如果我们不希望git追踪某些文件, 我们可以在工作区使用 `touch .gitignore` 命令来创建一个 `.gitIgnore` 文件
  @import "GitNote\Img\capture_20230816211057251.bmp"
  @import "GitNote\Img\capture_20230816211107509.bmp"
  然后我们将我们希望不被追踪的文件的文件名输入保存在`.gitIgnore` 文件中。
  @import "GitNote\Img\capture_20230816211151895.bmp"
  使用 `git status` 命令，w我们发现 `ignoreMe!. txt` 现在已经不再被追踪了。注意：在不被追踪的文件之中的任何修改操作都不会被git记录，所以需要谨慎对待）
  @import "GitNote\Img\capture_20230816211203433.bmp"
  @import "GitNote\Img\capture_20230816211326518.bmp"

- ### `Log` 操作
  我们可以使用 `git log` 命令来查看该仓库之中所有的历史Commit信息。
  @import "GitNote\Img\capture_20230816211757234.bmp"

- ### `fetch` & `pull` 操作
  有时他人编辑了仓库内的文件并将其同步（ `push` 操作，下文会进行讲解）至远程仓库，我们可以先使用 `fetch` 操作来获取新增的修改操作。（由于上文提到的网络问题，所以在这里我们使用Github Desktop。）然后再使用 `pull` 操作来拉取哪些修改后的文件。在此之后，所有的最新版文件都将被从远程同步至本地。
  @import "GitNote\Img\capture_20230902095349366.bmp"
  `fetch` 与 `pull` 的区别：
  - `fetch` 只是获取远程仓库中相较于本地所新增的修改操作，在 `fetch` 完毕后会列出表格提示用户，但并不会直接对工作区的文件进行修改。
  - `pull` 则是将 `fetch` 到的所有新增操作全部应用于本地工作区，会导致本地文件的增删修改。有一定风险，需要在仔细思考后再进行 `pull` ，不然可能出现自己正在编辑的文件被他人的修改顶替的事故<sup>1</sup>。

  >1：出现这种事故时，Git会报告错误，并且停止 `pull` ，提示用户可以跳转至文件编辑器（一般是VScode）来比较本地与远程产生冲突的两个版本，并且决定保留哪一个，或者是全部保留。


- ### `push` 操作
  无论在仓库内进行何种文件修改操作（创建、删除、修改等），Git都将sa其记录下来。
  待修改工作结束，将所有想要提交的修改 `add` 然后 `commit` 即可。
  但是 `commit` 之后，这些修改仅仅只是储存在本地，无法与Github上的远程仓库同步。
  所以这里我们就会引出 `push` 操作，通过该操作，我们可以将Commit于本地的修改操作同步至远程仓库。
  @import "GitNote\Img\capture_20230902101118277.bmp"
---
## 现实应用举例
  大家一般都是使用文本编辑器或者集成开发环境来进行文件编辑，而这些成熟的软件一般也集成了图形化界面的Git（上文介绍的主要操作都是在Git Bash这一命令行界面下进行的）。在了解了命令行的Git指令后，使用图形化Git将会得心应手、无师自通、逍遥自在。下文我们以VScode为例，进行现实场景的模拟。
  当我们使用VScode打开一个仓库（带有 `.git` 文件夹 的文件夹）时，VScode会自动识别到它，并且会提示可以进行源代码管理。进行的文件修改操作都同样会被记录下来。末尾的大写字母代表了修改操作类型
  - A: 本地新增的文件
  - C: 文件的一个新拷贝
  - D: 本地删除的文件
  - M: 文件的内容被修改
  - R: 文件名被修改了
  - T: 文件的类型被修改了
  - U: 文件没有被合并
  @import "GitNote\Img\capture_20230902101746734.bmp"
  点击右侧的 `+` 即 `git add` 此文件，将它放入暂存区。然后点击 `√ 提交` 进行 `git commit` 。
  @import "GitNote\Img\capture_20230902102943545.bmp"
  系统会跳转至一个文件来编辑 *Commit Message*。在第一行输入信息即可。完毕后点击右上角的 `√`
  @import "GitNote\Img\capture_20230902103352106.bmp"
  至此，我们已在本地完成了修改的提交，然后正如上文，我们使用 `Github Desktop` 来将提交的修改 `push` 至远程仓库，不再赘述。
  在 `Github.com` 的 `commit` 页面。我们可以看到所有同步至远程仓库的提交信息，亦可查看每次提交的详情。
  @import "GitNote\Img\capture_20230902103919156.bmp"
  @import "GitNote\Img\capture_20230902103859160.bmp"

---
## 附录
  没啥附录，以后可能会有。但是目前还没有。

---
### ———— By Goway Lee😽

---
<br>

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
---

