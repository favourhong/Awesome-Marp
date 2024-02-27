
[✨ README-en](https://github.com/favourhong/Awesome-Marp/blob/main/README-en.md)、[🎉 README-zh](https://github.com/favourhong/Awesome-Marp/blob/main/README.md)

# Awesome Marp：轻松取代 LaTeX Beamer！

## 为什么要做 Awesome Marp？

自从了解到 Marp 可以使用 Markdown 语法来创作 PPT 之后，我有两年多没有使用 PowerPoint 做过演示文稿了。

Marp 内置的原生主题样式数量少，并且呈现效果不好看，所以一直以来我也在尝试自定义 CSS 文件，来打造符合个人审美的 theme。我在边改造边用的过程中，这套模板也得到了几位朋友的喜爱。于是索性分享出来，希望能给到你一些帮助~ 

我给这套主题还起了个名字，`Awesome Marp`，算是一个阶段性总结吧。目前 v1.3版本提供了 6 种主题（分别是深色、绿色、蓝色、红色、紫色和棕色）和 38 种自定义样式。

首先，先来看一张效果动图吧~

![Awesome Marp 整体效果](./images/AwesomeMarp整体效果.gif)

怎么样？如果你也使用过 Marp 原生的 theme，一定会发现 Awesome-Marp 变化真的很大了。是的，我基于 Marp 的`default` 主题，做了不小的改动。

这是一个纯 CSS 的项目，所有的效果都是 CSS 语言实现的。因为并没有前端基础，所以我是一边学一边改，代码还有不少可以再完善优化的地方。但，完成比完善更重要嘛，一些小的问题可以日后迭代更新。于是，就决定将 Awesome Marp 上线了！


## 你需要了解的软件工具

就三样：用到的工具：软件 [Visual Studio Code](https://code.visualstudio.com) 或 [Obsidian](https://obsidian.md/)、[Marp for VScode（插件）](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)！

- Markdown 是一种**极轻量**的文本标记语言，允许人们使用***\*易读易写\****的纯文本格式编写文档，而且对于表格、代码、图片、公式等支持良好，在网站搭建、课程笔记/讲义、演示文稿、撰写学术论文等方面应用极为广泛。

- Markdown 编辑器（如 VS Code、Obsidian）

- Marp 是使用 Markdown 创作演示文稿的工具。

## Awesome Marp 的几个特色

- 支持 8 种**页面分栏**的样式：分别是两栏五五分、两栏六四分、两栏七三分、两栏四六分、两栏三七分、三栏三三分、两行分栏和品字型分栏

![4种页面分栏的呈现效果](./images/页面分栏.gif)

- 支持 6 种**非嵌套列表的分栏**样式：两列+有序列表+方形序号、两列+有序列表+圆形序号、两列+无序列表+方形序号、两列+无序列表+圆形序号、单列+有序列表+方形序号、单列+有序列表+圆形序号

![list列表分栏呈现的效果](./images/列表分栏.gif)

- 支持导航进度栏：

![导航进度栏的效果](./images/导航进度栏.gif)

- 支持 5 种类型的封面页：

![5种类型封面页的效果](./images/封面页.gif)

- 支持 3 种类型的目录页：

![3种目录页的效果](./images/目录页.gif)

- 支持 5 种自定义 Callouts（类似于 Beamer 的定理框）：

![5种自定义引用盒子的呈现效果](./images/引用盒子.gif)



- 小彩蛋：链接会自动增加一个小尾巴：

![链接的呈现效果](./images/链接.gif)

- 还可以自定义实现图片的水平排列方式：居中对齐、居左对齐或居右对齐 
	- 图片水平居中对齐：`![#c](./images/a.png)`  
	- 图片水平居右对齐：`![#r](./images/a.png)` 
	- 图片水平居左对齐：`![#l](./images/a.png)` 
- …… 

总结一下，像上面的这样的自定义样式，目前 Awesome Marp 1.3 版本一共支持 38 个！使用时只需要在页面指定局部指令，比如： `<!-- _class: trans -->`）

![38 种自定义样式](./images/38种自定义样式.png)  

不光如此，我还设计了 6 种主题色，想要切换 theme，只需要可在 YAML 区定义 `theme: <theme_name>`：

![6种主题颜色](./images/6种主题颜色.png)

![轻松切换主题](./images/切换主题.gif)

## 如何使用 Awesome Marp？

- 如何使用：
  - **搭配 VS Code**：直接使用 VS Code 打开 `Awesome-Marp` 文件夹
    - 如果你想「拿来即用」，直接根据我分享的 Markdown 源码文件，对照修改就好了~ 
    - 如果你对部分效果不满意、期望简单微调的话，目前在 `Awesome-Marp/themes` 下有 6 个 CSS 文件，这些 CSS 文件决定了 Markdown 源码的最终渲染效果，可以试着改一改~ 
    - 如果你能够自行定制个性化 CSS 文件，渲染前，别忘在 `Awesome-Marp/.vscode/settings.json` 里加上你的 CSS 文件路径~ 
  - **搭配 Obsidian**：安装 [Marp Slides 插件](https://github.com/samuele-cozzi/obsidian-marp-slides)，并配置相应 CSS 路径

- 字体：因担心版权问题，需自行下载字体并安装，Awesome Marp 用到的字体有：
  - 正文字体：`Latin Modern Math`、`方正宋刻本秀楷简体`，如果未安装，默认将使用 `Calibri` 和 `楷体`
  - 标题字体：`Optima LT Medium`、`方正苏新诗柳楷简体`，如果未安装，默认将使用 `Arial` 和 `黑体`
  - 脚注字体：`Charm` 和 `叶根友毛笔行书修正版`，如果未安装，默认将使用 `Calibri` 和 `楷体`
  - 代码字体：`Fira Code` 和 `霞鹜文楷等宽`，如果未安装，默认将使用 `Consolas` 和 `华文中宋`

## 更新记录

- `2024年1月13日` Awesome Marp v1.3 
  - 38 种自定义样式 
  - 增加两行分栏、品字型分栏等

- `2023年10月16日` Awesome Marp v1.2
  - 30 种自定义样式
  - 在 v1.1 基础上增加脚注（1个）、调节字体大小（4 个）共 5 个自定义样式
  - 新增免安装字体
- `2023年9月26日`  Awesome Marp v1.1
  - 25 种自定义样式
  - 在 v1.0 基础上增加固定标题行（2 个）、页面四六分栏、页面三七分栏（2 个）共 4 个自定义样式
- `2023年9月24日`  Awesome Marp v1.0
  - 21 种自定义样式

---

希望对你有帮助，欢迎交流 ~ 

创作不易，buy me a coffee 🤙~ 


<img alt="WeChatPay" src="https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309240907419.png" width="200"/>

