---
marp: true
size: 16:9
theme: am_red
paginate: true
headingDivider: [2,3]
footer: \ *初虹（虹鹄山庄）* *Awesome Marp：轻松取代 LaTeX Beamer！* *2024年1月13日（v1.3）*
---


<!-- _class: cover_a 
<!-- _header: "" --> 
<!-- _footer: "" --> 
<!-- _paginate: "" --> 

# Awesome Marp：轻松取代 LaTeX Beamer！

###### “用法简单、功能全面的个性化 PPT 模板”

@初虹
公众号：虹鹄山庄
发布时间：2024 年 1 月 13 日（v1.3）
<ch2099058972@163.com>
Awesome-Marp 地址：[GitHub 库](https://github.com/favourhong/Awesome-Marp)/[Gitee 库](https://gitee.com/favourhong/Awesome-Marp)

## Awesome Marp 有什么？

<!-- _class: cols2_ol_ci fglass toc_a  -->
<!-- _footer: "" -->
<!-- _header: "CONTENTS" -->
<!-- _paginate: "" -->

- [关于模板](#3)
- [封面页](#10) 
- [目录页](#16)
- [页面分栏与列表分列](#20)
- [引用、链接和引用盒子](#38)
- [导航栏](#45)
- [其他自定义样式](#48)
- [需要知道的基础知识](#56)
- [最后一页](#59)

## 1. 关于模板

<!-- _class: trans -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

## 1. 关于模板

- **开始之前：** 你需要知道这样几个工具，Markdown、Markdown 编辑器（VS Code 或 Obsidian）和 Marp。关于这三者是个啥，我不做详细地介绍，但在[第 55 页](#55)-[第 58 页](#58)会有一些凝练性的内容给你参考，同时我提供了不少的链接，也供你参阅。
- **为什么要开发 Awesome Marp？** 
  - Marp 原生仅提供 3 种主题（`default` / `gaia` / `uncover`），呈现效果一般。于是我根据自己的使用情况，边用边改造，陆续打磨了这样的一整套模板。
  - **目前发布的 v1.3 有 38 个自定义样式、6 种颜色的主题**（后面有呈现效果）
- **Awesome Marp 的几个特色：**
  - 支持分栏呈现、支持 Callouts（类似于 Beamer 中的定理框）、提供多种类型的封面页和目录页、可以实现导航进度栏、图片支持自定义居中/居左/居右对齐等 

- 本着「开箱即用」的原则，我将本项目文件夹打包上传到了[GitHub](https://github.com/favourhong/Awesome-Marp) 和 [Gitee](https://gitee.com/favourhong/Awesome-Marp)
- 用到的工具：软件 [Visual Studio Code](https://code.visualstudio.com) 或 [Obsidian](https://obsidian.md/)、[Marp for VScode（插件）](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)

## 1. 关于模板


- Awesome Marp 支持 38 个自定义样式，使用时需在页面指定（如 `<!-- _class: trans -->`）：

| 封面页    | 目录页  | 列表        | 引用盒子    | 其他 1                        | 其他 2                                                          |
| --------- | ------- | ----------- | ----------- | ----------------------------- | --------------------------------------------------------------- |
| `cover_a` | `toc_a` | `cols-2`    | `bq-black`  | 过渡页面 `trans`              | 图表等的标题 `caption`                                          |
| `cover_b` | `toc_b` | `cols-2-64` | `bq-purple` | 最后一页 `lastpage`           | 非嵌套无序列表的毛玻璃效果 `fglass`                             |
| `cover_c` |         | `cols-2-73` | `bq-red`    | 导航栏 `navbar`               | 脚注：`footnote`                                                |
| `cover_d` |         | `cols-3`    | `bq-blue`   | 标题固定+无底色 `fixedtitleA` | 调节字体大小：`tinytext`/`smalltext`/<br>`largetext`/`hugetext` |
| `cover_e` |         | `cols-2-46` | `bq-green`  | 标题固定+有底色 `fixedtitleB` |                                                                 |
|           |         | `cols-2-37` |             | 两列有序列表 `cols2_ol_sq/ci`                              |                                                                 |
|           |         | `rows-2`    |             | 两列无序列表 `cols_ul_sq/ci`                              |                                                                 |
|           |         | `pin-3`            |             | 单列有序列表 `col1_ul_sq/ci`                              |                                                                 |


## 1. 关于模板


- Awesome Marp 的主题色（6 种），可在 YAML 区切换 Theme，如 `theme: am_dark`：

| 深色      | 绿色       | 红色     | 蓝色      | 棕色       | 紫色
|---------|----------|--------|---------|----------|----|
| `am_dark` | `am_green` | `am_red` | `am_blue` | `am_brown` |`am_purple`|


## 1. 关于模板

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

## 1. 关于模板：更新日志

- [Awesome Marp：我开发了一整套 Marp 主题，Markdown 转换的 PPT 也可以很好看！](https://mp.weixin.qq.com/s?__biz=MzkwOTE3NDExOQ==&mid=2247486787&idx=1&sn=2652ddae81f50240844cb652780912e1&chksm=c13ff94bf648705da1ba986b91265e3ff018acaffcfa60d7807a81be22176005e7a2b4483627&scene=178&cur_album_id=3132459596339757070#rd)
- [Awesome Marp v1.1：标题行不随正文浮动，这下更像 Beamer 了！](https://mp.weixin.qq.com/s?__biz=MzkwOTE3NDExOQ==&mid=2247486800&idx=1&sn=527348e242576079e4bd6cd1823c823a&chksm=c13ff958f648704e40a202db6ad5fa215ef4c189d66403e161d6ace9828406a8747ac755684f&scene=178&cur_album_id=3132459596339757070#rd)
- [Awesome Marp v1.2：增加脚注、调节字体大小等样式～](https://mp.weixin.qq.com/s?__biz=MzkwOTE3NDExOQ==&mid=2247486825&idx=1&sn=56d632ce164831438ec87c1b20ed4c4c&chksm=c13ff961f64870774f069ab816340783d8f54fd6b89363b8d9412c593efc640851ce9edd8833&scene=178&cur_album_id=3132459596339757070#rd) 


## 下面让我们看看效果吧 ~  

<!-- _class: trans -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

## 2. 封面页

<!-- _class: trans -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

## 2. 封面页

- 大标题：采用一级标题 `# ` （如：`# Awesome Marp：自定义 Marp 主题`）
- 副标题：采用六级标题 `###### ` （如：`###### 打造简便又不失个性的演示文稿`）
- 本套模板提供 5 种封面页样式，使用时需要在页面中设定局部指令，如：`<!-- _class: cover_a -->` 
  - `cover_a`：[第 1 种](#1)
  - `cover_b`：[第 2 种](#12)
  - `cover_c`：预留 header 可设定学校 logo，footer 可设定校训 [第 3 种](#13)
  - `cover_d`：只预留了 footer 设定校训 [第 4 种](#14)
  - `cover_e`：预留 header 设定学校 logo，footer 设定学校 logo 和学校名称[第 5 种](#15)

- 如果已经设定了全局 footer、header 或页码，但又不期望在封面页中出现，可以 `<!-- _footer: "" -->` / `<!-- _header: "" -->` / `<!-- _paginate: "" -->` 分别将其局部隐藏起来
- 当标题文字超过页面宽度会溢出换行，这里可以使用 `<!-- fit -->` 根据页面宽度自动调整文字大小

---

<!-- _class: cover_b -->
<!-- _header: "" -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

# Awesome Marp：轻松取代 LaTeX Beamer！

###### “用法简单、功能全面的个性化 PPT 模板”

@初虹
公众号：虹鹄山庄
发布时间：2024 年 1 月 13 日（v1.3）
<ch2099058972@163.com>
Awesome-Marp 地址：[GitHub 库](https://github.com/favourhong/Awesome-Marp)/[Gitee 库](https://gitee.com/favourhong/Awesome-Marp)

---

<!-- _class: cover_c -->
<!-- _paginate: "" -->
<!-- _footer: 克明峻德，格物致知 -->
<!-- _header: ![](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309231557236.png) -->

# <!-- fit -->Awesome Marp：轻松取代 LaTeX Beamer！

###### “用法简单、功能全面的个性化 PPT 模板”

@初虹
公众号：虹鹄山庄
发布时间：2024 年 1 月 13 日（v1.3）
<ch2099058972@163.com>
Awesome-Marp 地址：[GitHub 库](https://github.com/favourhong/Awesome-Marp)/[Gitee 库](https://gitee.com/favourhong/Awesome-Marp)

---

<!-- _class: cover_d -->
<!-- _paginate: "" -->
<!-- _footer: "克明峻德，格物致知" -->

# <!-- fit -->Awesome Marp：轻松取代 LaTeX Beamer！

###### “用法简单、功能全面的个性化 PPT 模板”

@初虹
公众号：虹鹄山庄
发布时间：2024 年 1 月 13 日（v1.3）
<ch2099058972@163.com>
Awesome-Marp 地址：[GitHub 库](https://github.com/favourhong/Awesome-Marp)/[Gitee 库](https://gitee.com/favourhong/Awesome-Marp)

---

<!-- _class: cover_e -->
<!-- _paginate: "" -->
<!-- _footer: ![](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309231557236.png) -->
<!-- _header: ![](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309231558983.png) -->


# <!-- fit -->Awesome Marp：轻松取代 LaTeX Beamer！

###### “用法简单、功能全面的个性化 PPT 模板”

@初虹
公众号：虹鹄山庄
发布时间：2024 年 1 月 13 日（v1.3）
<ch2099058972@163.com>
Awesome-Marp 地址：[GitHub 库](https://github.com/favourhong/Awesome-Marp)/[Gitee 库](https://gitee.com/favourhong/Awesome-Marp)

## 3. 目录页

<!-- _class: trans -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

## 3. 目录页 

- Awesome Marp 提供了至少 2 种目录页样式，使用时同样需要设定局部样式
  - `toc_a`：需要将 header 的内容设定为 `CONTENTS`，即 `<!-- _header: "CONTENTS" -->`
  - `toc_b`：需要将 header 的内容设定为 `目录<br>CONTENTS<br>你的LOGO地址`，即 `<!-- _header: 目录<br>CONTENTS<br>![](./logo.png)-->`
  - 提供的几种分栏列表样式，也可以作为目录页使用，如 `<!-- _class: cols2_ol_ci fglass  -->`（效果见[这里](#32)）

- 类似地，如果已经定义了全局 footer 或页码，可以使用 `<!-- _footer: "" -->` / `<!-- _paginate: "" -->` 分别将其局部隐藏起来
- 目录页样式：[第 1 种](#2)、[第 2 种](#18)和[第 3 种](#19)

---

<!-- _class: toc_a -->
<!-- _header: "CONTENTS" -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

- [关于模板](#3)
- [封面页](#10) 
- [目录页](#16)
- [页面分栏与列表分列](#20)
- [引用、链接和引用盒子](#38)
- [导航栏](#45)
- [其他自定义样式](#48)
- [需要知道的基础知识](#56)
- [最后一页](#59)

---

<!-- _header: 目录<br>CONTENTS<br>![](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309231558983.png)-->
<!-- _class: toc_b -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

- [关于模板](#3)
- [封面页](#10) 
- [目录页](#16)
- [页面分栏与列表分列](#20)
- [引用、链接和引用盒子](#38)
- [导航栏](#45)
- [其他自定义样式](#48)
- [需要知道的基础知识](#56)
- [最后一页](#59)


## 4. 页面分栏与列表分列

<!-- _class: trans -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

## 4.1 页面分栏与列表分列：页面分栏

- Awesome Marp 提供了 8 种页面分栏方式，分别为：
  - `cols-2`：[两列分栏，五五平分](#23)
  - `cols-2-64`：[两列分栏，六四分](#24)
  - `cols-2-73`：[两列分栏，七三分](#25)
  - `cols-2-46`：[两列分栏，四六分](#26)
  - `cols-2-37`：[两列分栏，三七分](#27) 
  - `cols-3`：[三列分栏，平分](#28)
  - `rows-2`：[两行分栏](#29)
  - `pin-3`：[品字型分栏](#30)

- 如果某一栏为图片，可以将 `class=ldiv` 换成 `class=limg`，这样能够实现图片的垂直居中对齐呢（`class=ldiv` 为居上对齐）


## 4.1 页面分栏与列表分列：页面分栏

- 以 `<!-- _class: cols-2 -->` 为例，Markdown 的源码为：

```markdown
<!-- _class: cols-2 -->  
<div class=ldiv>  

第一列（左侧栏）的内容在这里

内容可以是普通纯文本，可以是列表，也可以是引用块、链接、图片等
</div>

<div class=rdiv>

第二列（右侧栏）的内容在这里
</div>
```

- 如果是分三栏（`<!-- _class: cols-3 -->`），还需要再增加 `<div class="mdiv"></div>` 标签


## 《荷塘月色》（两栏五五分）

<!-- _class: cols-2 -->

<div class=ldiv>

曲曲折折的荷塘上面，弥望的是田田的叶子。叶子出水很高，像亭亭的舞女的裙。

层层的叶子中间，零星地点缀着些白花，有袅娜地开着的，有羞涩地打着朵儿的；正如一粒粒的明珠，又如碧天里的星星，又如刚出浴的美人。

微风过处，送来缕缕清香，仿佛远处高楼上渺茫的歌声似的。这时候叶子与花也有一丝的颤动，像闪电般，霎时传过荷塘的那边去了。

叶子本是肩并肩密密地挨着，这便宛然有了一道凝碧的波痕。叶子底下是脉脉的流水，遮住了，不能见一些颜色；而叶子却更见风致了。

—— 朱自清《荷塘月色》  [返回](#21)
</div>

<div class=rimg>

<!-- ![#c](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309221014499.png) -->
![#c](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309221630151.png)
</div>

## 《春》（两栏六四分）

<!-- _class: cols-2-64 -->

<div class=limg>

![#c](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309201217248.png)
</div>

<div class=rdiv>

盼望着，盼望着，东风来了，春天的脚步近了。

一切都像刚睡醒的样子，欣欣然张开了眼。山朗润起来了，水涨起来了，太阳的脸红起来了。

小草偷偷地从土里钻出来，嫩嫩的，绿绿的。园子里，田野里，瞧去，一大片一大片满是的。坐着，躺着，打两个滚，踢几脚球，赛几趟跑，捉几回迷藏。风轻悄悄的，草软绵绵的。

—— 朱自清《春》

[返回](#21)
</div>

## 经典散文诗篇（两栏七三分）

<!-- _class: cols-2-73 -->

<div class=limg>

![#c](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309221010523.png)

</div>

<div class=rdiv>

经典的散文诗篇有：

- 朱自清：《荷塘月色》
- 林清玄：《月到天心》
- 郁达夫：《古都的秋》
- 张爱玲：《花落的声音》
- 余光中：《听听那冷雨》
- 张抗抗：《牡丹的拒绝》
- 丰子恺：《杨柳》
- 周作人：《乌篷船》
- 郑振铎：《石湖》
- 梁实秋：《雅舍》

[返回](#21)
</div>

## 《春》（两栏四六分）

<!-- _class: cols-2-46 -->

<div class=ldiv>


盼望着，盼望着，东风来了，春天的脚步近了。

一切都像刚睡醒的样子，欣欣然张开了眼。山朗润起来了，水涨起来了，太阳的脸红起来了。

小草偷偷地从土里钻出来，嫩嫩的，绿绿的。园子里，田野里，瞧去，一大片一大片满是的。坐着，躺着，打两个滚，踢几脚球，赛几趟跑，捉几回迷藏。风轻悄悄的，草软绵绵的。

—— 朱自清《春》

[返回](#21)
</div>

<div class=rimg>

![#c](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309201217248.png)
</div>

## 经典散文诗篇（两栏三七分）

<!-- _class: cols-2-37 -->

<div class=ldiv>


经典的散文诗篇有：

- 朱自清：《荷塘月色》
- 林清玄：《月到天心》
- 郁达夫：《古都的秋》
- 张爱玲：《花落的声音》
- 余光中：《听听那冷雨》
- 张抗抗：《牡丹的拒绝》
- 丰子恺：《杨柳》
- 周作人：《乌篷船》
- 郑振铎：《石湖》
- 梁实秋：《雅舍》

[返回](#21)
</div>

<div class=rimg>

![#c](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309221010523.png)
</div>

## 夏与秋（三栏三平分）

<!-- _class: cols-3 -->

<div class=ldiv>

![#center](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309201206630.png)

</div>

<div class=mdiv>

![#center](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309201151809.png)

![#center](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309201158036.png)
</div>

<div class=rdiv>

![#center](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309201154535.png)

[返回](#21)
</div>


## 高山与沙漠（两行分栏）

<!-- _class: rows-2 -->

<div class="timg">

![#c h:250](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202401131736186.png)
</div>

<div class="bimg">

![#c h:260](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202401131737821.png)
</div>

## 《宇宙的奥秘》（品字型分栏）

<!-- _class: pin-3 -->

<div class="tdiv">

> 四百年前，两位截然不同的科学家突破了当时已知世界的边界。1609 年在威尼斯，伽利略・伽利雷透过望远镜观察星辰，并制作仪器和进行实验。在布拉格，科班出身的神学家约翰内斯・开普勒发现了行星运动定律，奠定了近代天体物理学的基础，并思考着宇宙的宏伟构造。托马斯・德・帕多瓦以至今较少受到关注却扣人心弦的通信往来为基础，讲述了这两位类型如此迥异的学者之间不对等的关系，以及他们如何在同样的时刻却以各自的方式探索星辰的奥秘。在彼此的鉴照下，他们的远见与固执、睿智与无知得以呈现。这是一部介绍新科学的崛起以及近代来临之际的巨大变革的作品。  ——《宇宙的奥妙》
</div>

<div class="limg">

![#c](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202401131712626.png)
</div>

<div class="rimg">

![#c h:260](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202401131713779.png)
</div>


## 4.2 页面分栏与列表分列：列表分列

Awesome Marp v1.3 提供了 6 种列表分列的方式，分别为：

- `cols2_ol_sq`：呈现效果为[有序列表 + 方形序号](#32)
- `cols2_ol_ci`：呈现效果为[有序列表 + 圆形序号](#33)
- `cols2_ul_sq`：呈现效果为[无序列表 + 方形序号](#34)
- `cols2_ul_ci`：呈现效果为[无序列表 + 圆形序号](#35)
- `col1_ul_sq`：呈现效果为[有序列表 + 方形序号](#36)
- `col1_ul_ci`：呈现效应为[有序列表 + 圆形序号](#37)


## 《微观经济学：现代观点》

<!-- _class: cols2_ol_sq fglass -->

渲染效果为**有序列表+方形序号**
自定义样式为：`<!-- _class: cols2_ol_sq fglass -->`

- 偏好和效用
- 预算约束和消费者的最优选择
- 需求函数
- 劳动力和储蓄的供给函数
- 福利经济学：单人模型和多人模型
- 企业理论：单投入品和多投入品模型
- 完全竞争市场
- 完全垄断、垄断竞争与双寡头垄断
- 博弈论
- 交换经济与生产经济
- 外部性与公共品
- 不确定性、期望效用和不对称信息

[返回](#28)


## 《微观经济学：现代观点》

<!-- _class: cols2_ol_ci fglass -->

渲染效果为**有序列表+圆形序号**
自定义样式为：`<!-- _class: cols2_ol_ci fglass -->`

- 偏好和效用
- 预算约束和消费者的最优选择
- 需求函数
- 劳动力和储蓄的供给函数
- 福利经济学：单人模型和多人模型
- 企业理论：单投入品和多投入品模型
- 完全竞争市场
- 完全垄断、垄断竞争与双寡头垄断
- 博弈论
- 交换经济与生产经济
- 外部性与公共品
- 不确定性、期望效用和不对称信息

[返回](#28)

## 《置身事内》

<!-- _class: cols2_ul_sq fglass -->

渲染效果为**无序列表+方形序号**
自定义样式为：`<!-- _class: cols2_ul_sq fglass -->`

- 第一章：地方政府的权力与事务 
- 第二章：财税与政府行为 
- 第三章：政府投融资与债务 
- 第四章：工业化中的政府角色 
- 第五章：城市化与不平衡 
- 第六章：债务与风险 
- 第七章：国内国际失衡 
- 第八章：政府与经济发展

[返回](#28)

## 《置身事内》

<!-- _class: cols2_ul_ci fglass -->

渲染效果为**无序列表+圆形序号**
自定义样式为：`<!-- _class: cols2_ul_ci fglass -->`

- 第一章：地方政府的权力与事务 
- 第二章：财税与政府行为 
- 第三章：政府投融资与债务 
- 第四章：工业化中的政府角色 
- 第五章：城市化与不平衡 
- 第六章：债务与风险 
- 第七章：国内国际失衡 
- 第八章：政府与经济发展

[返回](#28)

## 《微观经济学：现代观点》

<!-- _class: col1_ol_sq fglass -->

渲染效果为**单列+有序列表+方形序号**
自定义样式为：`<!-- _class: col1_ul_sq fglass -->`

- 预算约束和消费者的最优选择
- 劳动力和储蓄的供给函数
- 福利经济学：单人模型和多人模型
- 企业理论：单投入品和多投入品模型
- 完全竞争市场
- 完全垄断、垄断竞争与双寡头垄断
- 交换经济与生产经济
- 不确定性、期望效用和不对称信息

## 《微观经济学：现代观点》

<!-- _class: col1_ol_ci fglass -->

渲染效果为**单列+有序列表+圆形序号**
自定义样式为：`<!-- _class: col1_ul_ci fglass -->`

- 预算约束和消费者的最优选择
- 劳动力和储蓄的供给函数
- 福利经济学：单人模型和多人模型
- 企业理论：单投入品和多投入品模型
- 完全竞争市场
- 完全垄断、垄断竞争与双寡头垄断
- 交换经济与生产经济
- 不确定性、期望效用和不对称信息

## 5. 引用、链接和 Callouts

<!-- _class: trans -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

## 5. 引用、链接和 Callouts

- 引用的呈现效果为：

> 合成控制法 (Synthetic Control Method) 最早由 Abadie and Gardeazabal (2003) 提出，用来研究西班牙巴斯克地区恐怖活动的经济成本，属于案例研究范畴 (Case Study)。

- 链接的呈现效果：
  - [经管数据清洗与 Stata 实战：三大地级市数据库和 CSMAR 上市公司数据](https://mp.weixin.qq.com/s/D0cYVPJJsNiu61GcYwV6cg)
  - [Stata 基础：从论文文件夹体系的建立说起](https://mp.weixin.qq.com/s?__biz=MzkwOTE3NDExOQ==&mid=2247486489&idx=1&sn=2eb51e85a01541c7a552a9434e087512&scene=21#wechat_redirect)
- Callouts 是 Awesome Marp 提供的自定义的样式，有 5 种颜色可选：
  - [紫色](#40)：`bq-purple`
  - [蓝色](#41)：`bq-blue`
  - [绿色](#42)：`bq-green`
  - [红色](#43)：`bq-red`
  - [黑色](#44)：`bq-black`

## 5. 引用、链接和引用盒子

<!-- _class:  bq-purple -->

- 自定义样式为：`<!-- _class:  bq-purple -->`

> 合成控制法 (Synthetic Control Method) 
> 
> SCM 最早由 Abadie and Gardeazabal (2003) 提出，用来研究西班牙巴斯克地区恐怖活动的经济成本，属于案例研究范畴 (Case Study)。Athey & Imbens (2017) 认为它是过去 15 年计量方法领域最重要的创新。<br>
> 合成控制法的基本思想是：虽然无法找到巴斯克地区的最佳控制地区，但可对西班牙的若干大城市进行适当的线性组合（赋予不同的权重），以构造一个更为贴切的「合成控制地区」 (Synthetic Control Region)，然后将真实的巴斯克地区与「合成的巴斯克地区」进行对比，即可得到恐袭的影响。

[返回](#39)

## 5. 引用、链接和引用盒子

<!-- _class:  bq-blue -->

- 自定义样式为：`<!-- _class:  bq-blue -->`

> 合成控制法 (Synthetic Control Method) 
> 
> SCM 最早由 Abadie and Gardeazabal (2003) 提出，用来研究西班牙巴斯克地区恐怖活动的经济成本，属于案例研究范畴 (Case Study)。Athey & Imbens (2017) 认为它是过去 15 年计量方法领域最重要的创新。<br>
> 合成控制法的基本思想是：虽然无法找到巴斯克地区的最佳控制地区，但可对西班牙的若干大城市进行适当的线性组合（赋予不同的权重），以构造一个更为贴切的「合成控制地区」 (Synthetic Control Region)，然后将真实的巴斯克地区与「合成的巴斯克地区」进行对比，即可得到恐袭的影响。

[返回](#39)

## 5. 引用、链接和引用盒子

<!-- _class:  bq-green -->

- 自定义样式为：`<!-- _class:  bq-green -->`

> 合成控制法 (Synthetic Control Method) 
> 
> SCM 最早由 Abadie and Gardeazabal (2003) 提出，用来研究西班牙巴斯克地区恐怖活动的经济成本，属于案例研究范畴 (Case Study)。Athey & Imbens (2017) 认为它是过去 15 年计量方法领域最重要的创新。<br>
> 合成控制法的基本思想是：虽然无法找到巴斯克地区的最佳控制地区，但可对西班牙的若干大城市进行适当的线性组合（赋予不同的权重），以构造一个更为贴切的「合成控制地区」 (Synthetic Control Region)，然后将真实的巴斯克地区与「合成的巴斯克地区」进行对比，即可得到恐袭的影响。

[返回](#39)

## 5. 引用、链接和引用盒子

<!-- _class:  bq-red -->

- 自定义样式为：`<!-- _class:  bq-red -->`

> 合成控制法 (Synthetic Control Method) 
> 
> SCM 最早由 Abadie and Gardeazabal (2003) 提出，用来研究西班牙巴斯克地区恐怖活动的经济成本，属于案例研究范畴 (Case Study)。Athey & Imbens (2017) 认为它是过去 15 年计量方法领域最重要的创新。<br>
> 合成控制法的基本思想是：虽然无法找到巴斯克地区的最佳控制地区，但可对西班牙的若干大城市进行适当的线性组合（赋予不同的权重），以构造一个更为贴切的「合成控制地区」 (Synthetic Control Region)，然后将真实的巴斯克地区与「合成的巴斯克地区」进行对比，即可得到恐袭的影响。

[返回](#39)

## 5. 引用、链接和引用盒子

<!-- _class:  bq-black -->

- 自定义样式为：`<!-- _class:  bq-black -->`

> 合成控制法 (Synthetic Control Method) 
> 
> SCM 最早由 Abadie and Gardeazabal (2003) 提出，用来研究西班牙巴斯克地区恐怖活动的经济成本，属于案例研究范畴 (Case Study)。Athey & Imbens (2017) 认为它是过去 15 年计量方法领域最重要的创新。<br>
> 合成控制法的基本思想是：虽然无法找到巴斯克地区的最佳控制地区，但可对西班牙的若干大城市进行适当的线性组合（赋予不同的权重），以构造一个更为贴切的「合成控制地区」 (Synthetic Control Region)，然后将真实的巴斯克地区与「合成的巴斯克地区」进行对比，即可得到恐袭的影响。

[返回](#39)


## 6. 导航栏

<!-- _class: trans -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

## 6. 导航栏

<!-- _class: navbar -->
<!-- _header: \ ***@Awesome Marp*** *关于模板* *封面页* *目录页* *分栏与分列* *引用盒子* **导航栏** *基础知识*-->

- 一句题外话：打造 Awesome Marp 模板的最早初衷就是来自几位公众号粉丝朋友的询问，「Marp 是否也能实现想 Beamer 那样的顶部导航栏？」为了实现导航栏的效果，我又多学了一些 CSS 的知识，这套模板才得以成型

- 自定义样式为 `navbar`：`<!-- _class: navbar -->` 
- 导航栏修改自 header，最前面必须加入 `\ `
- 当前活动标题，使用粗体 `**粗体**`
- 其余非活动标题，使用斜体 `*斜体*`
- 如果左侧有文字，需要使用斜粗体 `***粗斜体***`
- 默认根据内容自动分配间距，如果希望右对齐，可以手动增加空格的方式来推动右对齐 


## 6. 导航栏

<!-- _header: \ ***@Awesome Marp*** *关于模板* *封面页* *目录页* *分栏与分列* *引用盒子* **导航栏** *基础知识*-->
<!-- _class: navbar -->

这张页面的部分 Markdown 源码：

```markdown
<!-- _class: navbar -->
<!-- _header: \ ***虹鹄山庄***      

- 自定义样式为 `navbar`：`<!-- _class: navbar -->` 
- 导航栏修改自 header，最前面必须加入 `\ `
- 当前活动标题：使用粗体 `**粗体**`
- 其余非活动标题：使用斜体 `*斜体*`
- 如果左侧有文字：使用斜粗体 `***粗斜体***`
- 默认根据内容自动分配间距，如果希望右对齐，可以手动增加空格的方式来推动右对齐 
``` 

## 7. 其他自定义样式

<!-- _class: trans -->
<!-- _footer: "" -->
<!-- _paginate: "" -->



## 7.1 固定标题行：更像 Beamer 了（`fixedtitleA`）

<!-- _class: fixedtitleA -->

- 自定义样式：`<!-- _class: fixedtitleA -->`
  
  - 使当前页面的标题栏固定在顶部，而非随着内容的多少浮动
  
  - 同时，页面内容也会从顶部起笔，而非垂直方向上居中显示


## 7.1 固定标题行：更像 Beamer 了（`fixedtitleB`）

<!-- _class: fixedtitleB -->


<div class="div">

- 自定义样式：`<!-- _class: fixedtitleB -->`
  
  - `fixedtitleB` 相比于 `fixedtitleA`，标题增加了底色色块，同时缩小了标题大小
  
  - 其余效果与 `fixedtitleA` 相同 
  
  - 但是页面正文内容需要包裹在 `<div class="div'></div>` 标签中 
</div>

---

<!-- _class: footnote -->

<div class="tdiv">

#### 7.2 脚注的自定义样式：`footnote`

使用方法：

- 自定义样式：`<!-- _class: footnote -->`
- 页面除脚注外的其他内容，写在 `<div class = "tdiv"></div>` 
- 页面的脚注内容，写在 `<div class = "bdiv"></div>` 

举个例子，展示一下显示效果：

- 一方面，经济金融化程度的加深，使得金融部门能够凭借资本跨期配置提前抽取其他部门的未来价值，从而扩大金融和非金融部门之间的外部收入差距$^1$。另一方面，经济金融化不断增加企业股东权力，促使企业更加追求股东价值最大化，这一导向将弱化普通劳动者阶层的议价能力，食利者阶层的财产性收入增加必然会挤压劳动收入份额，从而扩大了内部收入差距$^2$。

</div>

<div class="bdiv">

1 张甜迪. 金融化对中国金融、非金融行业收入差距的影响[J]. 经济问题, 2015(11): 40-46.
2 Hein E. Finance-dominated capitalism and re-distribution of income: a Kaleckian perspective[J]. Cambridge Journal of Economics, 2015, 39(3): 907-934.
</div>

## 7.3 调节文字大小的自定义样式

<!-- _class: largetext -->

对于字体大小的调节，直接修改 CSS 文件应该很方便的。但有小伙伴提出，“希望可以增加字体调节的自定义样式”，于是目前提供了四种微调样式：

- 自定义样式 1：`<!-- _class: tinytext -->` （是默认字体大小的 0.8 倍）
- 自定义样式 2：`<!-- _class: smalltext -->` （是默认字体大小的 0.9 倍）
- 自定义样式 3：`<!-- _class: largetext -->` （是默认字体大小的 1.15 倍）
- 自定义样式 4：`<!-- _class: hugetext -->` （是默认字体大小的 1.3 倍）

比如，本页面采用的自定义样式为 `largetext` 

## 7.4 图表标题的自定义样式：`caption`

<!-- _class: caption -->

- 通过 `<div class="caption">宇宙的奥妙</div>` 来定义图表的标题 

![#c h:380](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202401131712626.png)

<div class="caption">
宇宙的奥妙
</div>


## 需要知道的基础知识……

<!-- _class: trans -->
<!-- _footer: "" -->
<!-- _paginate: "" -->


## Markdown 概览

<!-- _header: \ ***@Awesome Marp*** *关于模板* *封面页* *目录页* *分栏与分列* *引用盒子* *导航栏* **基础知识**-->
<!-- _class: navbar -->

- Markdown 是一种**极轻量**的文本标记语言，允许人们使用**易读易写**的纯文本格式编写文档，而且对于表格、代码、图片、公式等支持良好
- 应用广泛：网站、课程笔记/讲义、演示文稿、撰写学术论文等
- Markdown 基础语法：
  - 参阅：[Markdown 中文文档](https://markdown-zh.readthedocs.io/en/latest/)、[Markdown 指南](https://www.markdown.xyz/)、[Markdown 菜鸟教程](https://www.runoob.com/markdown/md-tutorial.html)
  - 标题 `#`、粗体 `** **`、斜体 `* *`、删除线 `~~ ~~`、分割线 `---`、超链接 `[]()`
  - 引用 `>`、列表 `-` / `1. `、代码块 
  - 脚注 `[^1]` / `[^1]:`、待办事项 `[ ]` / `[x]`
- Markdown 进阶语法：
  - 图片 `![]()`：本地路径、网络路径（参阅：[图床与 PicGo——让你爱上记录与分享](https://sspai.com/post/65716)）
  - 数学公式：行内公式 `$...$`、行间公式 `$$...$$`
  - 支持 HTML 元素：`<br>`/`<hr>`/`<b></b>`/`<i></i>`/`<kbd></kbd>` 等
  
## 推荐的 Markdown 编辑器

<!-- _class: cols-2-64 navbar -->
<!-- _header: \ ***@Awesome Marp*** *关于模板* *封面页* *目录页* *分栏与分列* *引用盒子* *导航栏* **基础知识**-->

<div class=ldiv>

**VS Code**
- Visual Studio Code[下载地址](https://code.visualstudio.com/Download)
- VS Code 插件：
  - 配合 Markdown：[Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)、[Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
  - 图床：[PicGo](https://marketplace.visualstudio.com/items?itemName=Spades.vs-picgo)
  - 格式化文档：[Pangu-Markdown](https://marketplace.visualstudio.com/items?itemName=xlthu.Pangu-Markdown)
  - Markdown 转 PPT：[Marp for VScode](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)
  - Markdown 转思维导图：[Markmap for VScode](https://marketplace.visualstudio.com/items?itemName=gera2ld.markmap-vscode)
  - 配合 Zotero：[Citation Picker for Zotero](https://marketplace.visualstudio.com/items?itemName=mblode.zotero)、[Pandoc Citer](https://marketplace.visualstudio.com/items?itemName=notZaki.pandocciter)

</div>

<div class=rdiv>

**Obsidian**
- [Obsidian 主页](https://obsidian.md/)
- 基于 Markdown 的本地知识管理软件
- 除官方同步和发布功能外，对个人使用者完全免费
- 功能丰富、插件众多、开发社区活跃

</div>


## Marp 基本用法

<!-- _header: \ ***@Awesome Marp*** *关于模板* *封面页* *目录页* *分栏与分列* *引用盒子* *导航栏* **基础知识**-->
<!-- _class: navbar fixedtitleB -->

<div class="div">

- 几个字总结 [Marp](https://marp.app/)：使用 Markdown 创作演示文稿
  - 来自 Marp 官方网页的一段话：Marp (also known as the Markdown Presentation Ecosystem) provides an intuitive experience for creating beautiful slide decks. You only have to focus on writing your story in a Markdown document.

- 在 Markdown 文件的顶部 YAML 区域，通过 `marp: true` 启动 Marp，然后即可开启侧边预览，VS Code 界面左边是代码区域，右边为预览区域
- 内容遵循 Markdown 语法，但 Marp 增加了一些内置指令，而且指令分为全局指令和[局部指令](https://marpit.marp.app/directives?id=local-directives-1)，全局指令建议放置于 YAML 区，局部指令位于当前页面，不同页面通过 `---` 切分
- 推荐阅读：Marpit [官方文档](https://marpit.marp.app)及[中译版](https://caizhiyuan.gitee.io/categories/skills/20200730-marp.html#%E5%8A%9F%E8%83%BD)，五分钟学会 Marp[（上）](https://www.lianxh.cn/news/97fccdca2d7a5.html)、[（下）](https://www.lianxh.cn/news/521900220dd33.html)
</div>

## Marp 基本用法

<!-- _header: \ ***@Awesome Marp*** *关于模板* *封面页* *目录页* *分栏与分列* *引用盒子* *导航栏* **基础知识**-->
<!-- _class: navbar -->

```yaml
---
marp: true        # 开启 Marp 
size: 16:9        # 设定页面比例，常见有 16:9 或 4:3，默认为16:9
theme: gaia       # 切换主题，内置 3 种样式的主题，可以自定义主题
paginate: true    # 开启页码
headingDivider: 2 # 通过二级标题切分页面，省去手动换页的麻烦
footer: 初虹 # 设置页脚区域的内容，如果设定页眉的内容，则为 header
---
```

- 如果想让页面同时被多个级别的标题切分，比如，以二级~四级标题分割页面，可以 `headingDivider: [2,3,4]` 
- 想要使得多个自定义样式渲染同一个页面，可直接将不同自定义样式以空格连接，比如：`<!-- _class: cols-2-64 fglass -->`


---

<!-- _class: lastpage -->
<!-- _footer: "" -->

###### 欢迎交流 ~ 

<div class="icons">

- <i class="fa-solid fa-envelope"></i>
  - 邮箱：ch2099058972@163.com
- <i class="fa-brands fa-weixin"></i> 
  - 微信：favourhong  
- <i class="fa-solid fa-house"></i> 
  - 公众号：虹鹄山庄

<div>

## 创作不易，buy me a coffee 🤙~ 

<!-- _class: trans -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

<br>

![#c w:300](https://mytuchuang-1303248785.cos.ap-beijing.myqcloud.com/picgo/202309240907419.png)
