---  
url: https://github.com/Kenshin/simpread/discussions/3999?sort=new  
title: 简悦 + SimpRead Unread Sync + Obsidian 打造第二大脑「养成游戏」  
date: 2023-11-12 07:04:17  
tag:   
banner: https://images.unsplash.com/photo-1697366672245-3116e94b52fc?crop=entropy&cs=srgb&fm=jpg&ixid=M3w0Njc1ODd8MHwxfHJhbmRvbXx8fHx8fHwxfHwxNjk5NzQzNzE0fA&ixlib=rb-4.0.3&q=85&fit=crop&w=763&max-h=540  
banner_icon: 🔖  
created: 2023-11-12T07:03  
updated: 2023-11-30T13:34  
---  
  
这是来自 [简悦社区](https://t.me/simpread) 用户 [1wingedangel](https://github.com/1wingedangel) 的基于 Obsidan + [SimpRead Unreader Sync](https://github.com/Kenshin/simpread/discussions/2889) 的工作流分享，非常适合 Obsidian 与简悦深度用户使用。  
  
## 最终成形图  
  
使用 Obsidian Plugin：SimpRead Sync · Templater · QuickAdd · Obsidian42 - Text Transporter · Tasks · Banners  
  
![](https://user-images.githubusercontent.com/81074/171083910-3bcb010f-f00e-4500-a65d-69f8e54043c9.png)  
  
## 忏悔  
  
首先，我要先向上帝忏悔。因为我没能忍受住恶魔的呢喃以及能够尝试新插件的诱惑，等我醒悟过来已经 Too Late，在一天一天被催更的压力之下，才有了今天这篇文章。什么 `我会让这篇教程和 ob sync 插件一起发布。` 你个恶魔。  
  
## 工作流程  
  
由于篇幅可能会比较长，我先简单介绍一下我准备分享的工作流程：  
  
*   收集文章的统一入口我选择使用 [Raindrop.io](https://app.raindrop.io/) 。选择 Raindrop 的原因是跨平台、分类方便、免费无限制。一般文章默认保存在 `未分类` 。然后就不管了。  
*   阅读时间开始，从 Raindrop 打开文章。大致看一下文章的标题与开头内容，判断是否值得阅读。标题党、开头提不起兴趣的直接关闭，有兴趣的通过快捷键或者右键菜单把当前页面加入稍后读。  
*   重载页面让简悦更新该页面的稍后读信息，然后进入阅读模式。开始第一遍的快速阅读，判断是否需要收藏。如果有值得收藏的亮点，通过 Live Editor 清除多余的内容 （什么 `下载XX派客户端，关注XX派公众号，解锁全新阅读体验 📰`之类）。  
*   修改稍后读的元数据。主要是修整稍后读的标题（去除多余的因素，如标题末尾可能会出现的 `- 网站名称`）以及备注和标签。我一般会把文章标题进行简化后填写在备注里。比如这篇文章：[用「乐高」思维做成的产品是什么样的？Notion 和他的 GTM 策略](https://sspai.com/post/72987)，我可能就会简化标题并在备注里写： `Notion 和他的 GTM 策略`。因为前面那句话只是为了吸引读者来阅读，对于收藏没有太大意义还占篇幅。快速阅读完毕之后通过简悦同步助手导出离线 HTML 文件到本地。关闭页面，回到 Raindrop 把文章拖动到左侧边栏的分类中，进入下一篇文章继续。  
*   **接下来的阅读就不需要网络了**。精读时间开始，打开简悦稍后读。此时稍后读的阅读模式会加载本地的离线 HTML 文件，开始精读并且对感兴趣的段落进行标注。根据不同的需要给标注添加备注文本，具体下面再说。如果文章实在精辟值得全文收藏，直接`复制 Markdown 到剪贴板`。修改稍后读元数据里的 `描述` ，一般写上这篇文章对自己的第一印象如何，有什么收藏意义。  
*   把标注通过 Simpread Sync 插件导入 Obsidian 。有全文收藏的需要的话创建二级标题 `Article` ，再直接粘贴 Markdown 的内容。  
*   进行标注拆解和编写永久笔记。通过 Obsidian 的各种神奇的插件把标注或者文章内容通过引用块的方式编进自己的永久笔记（MOC）里。我个人习惯把 Heading 作为原子笔记单位，每个 Markdown 文档其实都是 MOC。到这一步，知识才算是放进了自己的笔记系统里。  
  
## 解释说明  
  
### 为什么不用简悦的 API，而是用 Raindrop  
  
**因为我收藏的文章比较乱**。简悦毕竟是国内用户比较多，适配的网站还是国内网站为主。国外的文章简悦的适配没有那么完美，所以需要 Live Editor 进行一定程度的修剪和编辑。然后 Raindrop 的分类操作非常直观方便，只需要拖动到侧边栏的相应分类就可以了，既不是输入关键词补全也不是从一个下拉选单里找。  
  
### 为什么不在阅读模式下添加标注  
  
**因为网页页面阅读模式无法加载本地 HTML 文件**。由于标注是根据文本内容以及其上下文来判断它在文章内的具体位置，所以如果 Live Editor 编辑过的本地 HTML 文件与原始网页差异过大，就会出现标注位置错乱的问题。所以我选择干脆**在稍后读里深度阅读本地加载的 HTML 文件然后添加标注**，尽量避免在阅读模式中进行。代价就是无法使用任何阅读模式下的插件，不过由于后述的 Obsidian 新版插件，这个就不再是一个问题了。  
  
### 为什么需要快速阅读  
  
快速阅读是为了保存离线 HTML 文件，说快速阅读只是显得自己很厉害 （喂）其实现实情况是大致扫一下文章是否值得精读以及进行 Live Editor 编辑修整文章而已。  
  
## Obsidian 插件的使用  
  
原本的 Obsidian 的 Simpread sync 插件 仅仅用来同步稍后读信息和标注内容的。后来简悦开发者开发出了简悦的导入到 Obsidian 的插件，支持了 Local REST API、新生的 Markdown 模板引擎，让我这个需要频繁使用 Live Editor 修整文章的本地文件用户感到无比空虚。于是我把一堆 Obsidian 联动 Zotero 的神奇玩法插件像霰弹枪般丢给了简悦作者之后，这恶魔还真的给我更新了 simpread Sync 插件，**可直接通过 Obsidian Command 选择并导入稍后读信息和稍后读的功能，并且支持新生的 Markdown 模板引擎**。  
  
![](https://user-images.githubusercontent.com/396190/170810610-f25e5ffa-6267-4524-a7c0-59a8b2713434.png)  
  
（暴露了我之前都没好好写描述）  
  
具体的使用方法请参考官方文档（如果有的话。没有的话催更）。我这边就把我个人的部分关键配置分享一下。  
  
### 可能要用到的 Obsidian 插件  
  
先说核心插件：  
  
*   日记插件  
*   模板插件  
*   页面预览插件  
  
第三方插件：  
  
*   SimpRead Sync （通过 BRAT 安装）  
*   Calendar  
*   Dataview  
*   Templater  
*   QuickAdd  
*   Obsidian42 - Text Transporter  
*   Tasks  
*   Banners  
  
### 文件命名方式  
  
由于我选择通过稍后读的备注写了文章的简化后标题，所以我导入稍后读和标注到 Obsidian 的文件的命名方式是 `SR{{id}}@{{note}}` 。不使用 `{{mode}}` 是因为我选择把标注和全文一起放在一个 markdown 文档内，而不是分开来保存。  
  
### 稍后读元数据模板  
  
Simpread Sync 插件的模板分两部分： `Unread Markdown Template` 和 `Annotation Markdown Template`。虽然不知道作者这样命名的意图，我理解为一个是稍后读元数据的相关模板，另一个是标注的相关模板。由于新生 Markdown 模板引擎的高度扩展性，最后我的稍后读元数据模板是这样的：  
  
```  
---  
title: "{{title}}"  
alias:   
<% if ( unread.note && unread.title != unread.note ) { %>  - "{{note}}"  
<% } %>  - "{{title}}"  
created-date: <%% tp.date.now("YYYY-MM-DDTHH:mm:ss.SSSZZ") %>  
type: Simpread  
<% if (unread.img) { %>banner: "<%- unread.img %> "  
banner_icon: 🔖  
<% } -%>  
tag: {{ |tag| | }}  
---  
  
# {{title}}  
  
> [!example]- Links    
> [🧷内部链接](<{{int_uri}}>) [🌐外部链接](<{{ext_uri}}>)   
  
%%  
> [!example]+ **Comments**    
>  | Date___ | Comments |  
> | ------- | -------- |  
>   
>  **Description**:: {{desc}}  
%%  
  
> [!md] Metadata    
> **标题**:: [{{title}}]({{url}})    
> **日期**:: [[{{create|yyyy-mm-dd}}]]    
<% if ( unread.annotations.length > 0 ) { %>  
## Annotations  
  
{{annotations}}  
<% } -%>  
<% if ( unread.tags.includes('Highlights') ) { %>  
![[<%% tp.file.title %>_mentions#Highlight Mentions]]  
<% } -%>  
<% if ( unread.refs ) { %>  
## Reference     
{{-|refs}}    
<% } %>  
  
  
```  
  
需要注意的是，根据严格 的 Markdown 格式要求，**callouts 中的每一行文字末尾都需要两个空格**。除非你关闭了 Obsidian 的 `严格换行` 开关。  
  
效果是这样的：  
  
![](https://user-images.githubusercontent.com/396190/170810651-8d7da912-d61b-42a8-bcd9-988f2dabf63f.png)  
  
### 简悦 Markdown 官方模板库  
  
这些模板也可以应用于简悦的 [Markdown 模板增强插件](https://github.com/Kenshin/simpread/discussions/3725)，我也将此模板放到了 [简悦 Markdown 官方模板库](https://github.com/Kenshin/simpread/discussions/2153#discussioncomment-2839811)。  
  
更多模板可以 [看这里](https://github.com/Kenshin/simpread/discussions/2153)。  
  
#### alias 的设置  
  
由于稍后读备注中简化标题的存在，所以该文献笔记的 `alias` 包含了完整标题和简化标题两种形式。如果没有简化标题或简化标题完全等于完整标题的时候不显示简化标题。  
  
#### banners 的设置  
  
简悦导出的稍后读其实是有题图的。我们可以通过 `unread.img` 放在 Frontmatter 的 `banner` 里显示这个题图。可以通过鼠标拖动题图来调整显示的区域。icon 能选择 twemoji 里的绘文字，具体参考一下 Banners 插件的帮助文档。  
  
如果不喜欢用网络上的图片做题图，你也可以用 quicker 来自动下载后替换。这个我就不展开了。  
  
#### 这个 Comments 什么鬼  
  
灵感抄自 Obsidian 的 Discord 频道中有人分享的 **在 Markdown 文档中通过 dataview 的形式显示所有日记中提及该文档的文本段落**。原本只是显示提及该文档的文本，然后被我魔改成 **通过 quickadd 快速在今日日记添加针对该文档的评论，并且可在文档内显示所有评论，按日期分组**。  
  
首先，在 vault 里创建一个 md 文档，**保存在模板文件夹里**：  
  
```  
```js quickadd  
const activeFile = this.app.workspace.getActiveFile();  
    if (!activeFile) {  
        new Notice("No active file", 5000);  
        return;  
    }  
//console.log("active file=", activeFile);  
return activeFile.basename;  
```  
  
  
```  
  
然后在 quickadd 的设置界面里添加一个新的 template 命令：  
  
*   Capture to：`你的日记文件夹/{{DATE:YYYY-MM-DD}}`  
*   Insert After：填上你用来放 log 的 Section  
*   勾上 `Insert at end of section`  
*   Capture Format 见下：  
  
```  
- {{DATE:HH:mm}} 更新文档：{{LINKCURRENT}}  
  - cmnt:: @@[[{{TEMPLATE:刚才创建的md文档路径}}|✒️]] {{VALUE}}  
  
  
```  
  
设置好后在任意文档运行这个 quickadd 命令就会弹出一个框让你输入评论，回车之后就会在今日的日记显示该评论：  
  
![](https://user-images.githubusercontent.com/396190/170810676-9bff8715-4618-469c-a639-a420bd24355f.png)  
  
最后这个 log 也会同时出现在这篇文档的相应的 dataview 中了。用子列表结构是为了兼容 Obsidian Memos。这个技巧可以应用于所有的笔记，**这一整个 callouts 模块也建议保存为模板然后随时调用于所有的永久笔记**。  
  
#### 为什么要把 Comments 的 Callout 用注释框起来  
  
这是为了打印成 PDF 或者是发布到网上时忽略这个 callout。  
  
#### 默认折叠 Comments callouts  
  
虽然我这边没有这样子操作，你如果平时不太想看到 Comments callouts 的全部内容，可选择将 callouts 默认折叠（把 `+` 换成 `-`）。此时为了在折叠状态下也能直观地看到 `{{desc}}` ，可通过 dataview 的 inline expressions 把稍后读描述直接显示在 callouts 的标题上面：  
  
`> [!example]+ **Comments**`  
  
把这句换成：  
  
``> [!example]- **Comments**: {{desc}} ``  
  
![](https://user-images.githubusercontent.com/396190/170810688-0f8b2dd9-26e6-4dd7-82a1-c7762c3a93d7.png)  
  
想要再复杂一点的如日记上的最新的记录文本之类，就写 inline dataviewjs 吧。我就不展开了…… 对了，实现了记得告诉我怎么做（喂  
  
#### templater 模板有时候不会转换  
  
templater 的一般玩家…… 呸，一般用户会设置成当你新建文档的时候自动运行全局替换的操作，所以当文档已存在，而简悦同步插件只是覆盖原来的内容的话， templater 不会自动运行替换操作 。碰到这种情况就再运行一次 `Replace templates in the active file` 的命令。  
  
#### Highlight Mentions 有什么用  
  
大家可能在浏览网页文章的时候会发现，**文章下面的评论比文章内容有价值多了**。但是，简悦大部分情况下并不能完成文章评论内容的截取和标注的操作。如果直接在文献笔记上追加这个章节的内容，那么哪天不小心运行了简悦同步就会被覆盖。所以我决定曲线救国，用了一系列的方法去解决摘录文章评论的问题：  
  
*   如果发现文章下面的评论区里有价值的内容，在稍后读的元数据里添加标签 `Highlights`  
*   简悦的稍后读元数据导出模板将会根据有无这个 `Highlights` 标签自动在 `Annotation` 和 `Reference` 两个章节之间追加一个 `Highlight Mentions` 的章节，内容指向另一个文档 `[[稍后读文献笔记_mentions#Highlight Mentions]]`  
*   通过 quickadd 新建 `稍后读文献笔记_mentions.md`，然后在相应的章节里追加精华评论的内容。  
*   就算简悦插件把这个文献笔记内容覆盖，由于评论内容在另一个文档里，所以不会覆盖这些内容。也能正常显示。  
  
接下来就差怎么用 quickadd 去新建这个笔记了。 很可惜，quickadd 不支持快速创建一个基于当前笔记文件名的笔记，于是我打开了 Javascript 菜鸟教程，看了大概 4 个小时左右，写了一个 js 脚本来解决这个问题：  
  
```  
module.exports = async (params) => {  
  console.log("Starting...")  
  console.log(params);  
  const currentFile = params.app.workspace.getActiveFile();  
  if (!currentFile) {  
      new Notice("No active file.");  
      return;  
  }  
  console.log("Found active file: ", currentFile.basename);  
  
  const currentFileName = currentFile.basename;  
  const currentFilePath = currentFile.path;  
  const newFilePath = currentFilePath.replace(/\.md$/g,'_mentions.md');  
  console.log("the New File Path:", newFilePath);  
  
  const dvTitle = params.app.plugins.plugins.dataview.api.page(currentFilePath).title;  
  if (!(dvTitle)) var currentTitle = currentFileName;  
  else var currentTitle = dvTitle;  
  console.log(dvTitle);  
  console.log(currentTitle);  
  
  const content = '---\ntype: Mentions\ncreated-date: <% tp.date.now("YYYY-MM-DDTHH:mm:ss.SSSZZ") %>\n---\n\n# ' + currentTitle + "\n\n- **LiteratureNotes**:: [[" + currentFileName + "]]  \n\n## Highlight Mentions\n\n";  
    
  console.log(`Path: ${newFilePath}.\nContent: ${content}`);  
    
  if (!(await params.app.vault.adapter.exists(newFilePath))) {  
    await params.app.vault.create(newFilePath,content);  
  }  
  else {  
    new Notice(`File ${newFilePath} already exists.` , 5000);  
  }  
  console.log("Finished!");  
}  
  
```  
  
然后再到 quickadd 新建一个 macro 命令，加载这个 js 文件即可。运行这个 quickadd 命令，就能成功创建一个 mentions 的笔记：  
  
![](https://user-images.githubusercontent.com/396190/170810712-2753a80f-55dc-49d2-ab83-3f7e69c36143.png)  
  
回到文献笔记上，也显示出了这个精华评论：  
  
![](https://user-images.githubusercontent.com/396190/170810719-26a9162d-859d-4cb2-adf4-69804243fa67.png)  
  
#### 有时候标注导入时间非常长， Obsidian 卡住了……  
  
因为标注里包含了离线图片。导入时间会随着图片的大小相应地延长，此时 Obsidian 就处于任何操作都无法进行的地步…… 我目前也只能等，然后用 quicker 脚本把离线图片统统替换成本地图片…… 具体就看相关的讨论或者自行解决吧，好像用万能的 python 也可以解决。  
  
### 标注模板  
  
先丢模板：  
  
```  
<%  
let colors = [ '#B4D9FB', '#ffeb3b', '#a2e9f2', '#a1e0ff', '#a8ea68', '#ffb7da' ],  
    color  = colors[ annote.color ];  
if (unread.note && unread.title != unread.note) {  
var filetitle = unread.note;  
}  
else {  
var filetitle = unread.title;  
}  
let wikilinks = "[[SR" + unread.idx + "@" + filetitle + "|📄]]";  
-%>  
<% if (annote.note.startsWith("######")) { %>  
<%   
let note = annote.note.slice(7);  
-%>  
###### <% if (note) { %><%- note %><% } else { %>{{an_text}}<% } %>  
<% } else if (annote.note.startsWith("######")) { %>  
<%   
let note = annote.note.slice(6);  
-%>  
###### <% if (note) { %><%- note %><% } else { %>{{an_text}}<% } %>  
<% } else if (annote.note.startsWith("####")) { %>  
<%   
let note = annote.note.slice(5);  
-%>  
#### <% if (note) { %><%- note %><% } else { %>{{an_text}}<% } %>  
<% } else if (annote.note.startsWith("###")) { %>  
<%   
let note = annote.note.slice(4);  
-%>  
### <% if (note) { %><%- note %><% } else { %>{{an_text}}<% } %>  
<% } else { %>  
> <%- wikilinks %> Highlights [🧷](公司NAS-丰团团.md) [🌐](<{{an_ext_uri}}>) {{#|an_tag| }}    
{{{html_format|>|{{an_html}}}}}  
<% if (annote.refs) { -%>  
{{> - 🔗|an_refs}}  
<% } -%>  
<% if (annote.note) { -%>  
<% if (annote.note.startsWith("todo:") == false) { -%>  
>    
> - 📝{{an_note}}  
  
^sran-{{an_id}}  
<% } else { -%>  
<%   
let note = annote.note.slice(6);  
-%>   
^sran-{{an_id}}  
  
- [ ] <%- note %> #web ^srtask-{{an_id}}  
<% } -%>  
<% } else { %>  
^sran-{{an_id}}  
<% } -%>  
<% } -%>  
  
  
```  
  
效果图（节选）：  
  
![](https://user-images.githubusercontent.com/396190/170810730-e75c1f34-ab79-4f03-b0a5-2c20855e7c51.png)  
  
有很多地方和默认推荐的模板差不多，我就提几个默认模板里没有的。  
  
#### 标注的外部引用  
  
对应的占位符是 `{{an_refs}}` 。虽然作者没有明说这个东西干什么用，但是我后来发现，**外部引用可以不止是 URL 地址**。比如 Markdown 链接，又比如指向 Obsidian 里的 MOC 的 Wikilinks，来与其他永久笔记建立双链。那怎么在简悦的稍后读里快速输入 Obsidian 的双链呢？我通过 quicker 写了一个简单的脚本进行实现：  
  
2022-05-14_17-13-52.mp4<video src="https://user-images.githubusercontent.com/396190/170810813-fe709ea9-f6e2-46de-b91a-0939482c89a3.mp4" control></video>  
  
#### 标题定制  
  
*   当标注的备注文本以 `###` 开头，则导出到 Obsidian 的时候该位置的标注会被转换成 `### 标注文本` 。  
*   上述的标注标题化可对应 3 级标题至 6 级标题。由于标注部分是二级标题，所以不做一级和二级标题的定制。  
*   当标注的备注文本为 `### 任意文本内容` 时，标注会被转换成 `### 任意文本内容` 。此时和标注文本内容无关。也就是说，**你如果想要在文献笔记里添加标题，只需要在稍后读里随便找一个对应位置的文本添加标注，然后备注文本改成自己想要的文本内容就可以了**。为了与其他标注做区分，你可以选择使用不同的标注颜色或者风格。  
  
#### 给标注自动添加任务  
  
当标注的备注文本是`todo: 任意文本内容`的时候，则导出到 Obsidian 时，该标注后面会追加一个 Obsidian Tasks 格式的任务。任务文本为：`- [ ] 任意文本内容 #web ^srtask-{{an_id}}`。通过 Obsidian 的 Tasks 插件在其他任务笔记添加 tasks 相关的代码块即可提取该任务。  
  
```  
```tasks  
not done  
path does not include templates  
no scheduled date  
description includes #web  
starts before tomorrow  
hide task count  
```  
  
  
```  
  
效果：  
  
![](https://user-images.githubusercontent.com/396190/170810843-b10341c1-5526-456b-9f7f-95ac0354e42e.png)  
  
当然这个做法也是有一定缺点：  
  
*   Backlink 里会显示 Section 名。和上面的标题定制一起使用而上面的标题和标注没有太多关系，会比较尴尬  
*   重新导出标注到 Obsidian 的时候，任务也会被重置；嘛重新标记完成就是了  
  
### 整理笔记  
  
把标注导出到 Obsidian，也并不代表你学到了东西。按照卡片盒笔记法（此处省略几百字…… 老生常谈了，详情请自行查找有关文章然后用简悦标注一下导出到 Obsidian）  
  
不扯淡了，我就简单介绍一下自己关于整理笔记的想法吧。（注：并没有说我现在就是这么做的，目前正在努力付诸实践……）  
  
#### 永久笔记  
  
永久笔记，我个人理解是主要分两大类：  
  
*   XXX 是什么  
*   如何 XXX  
  
任何一个知识点用语言概括下来就是这两种。反正我是想不出其他的了。所以我个人认为，网页文章标注的整理也是基于这个规则来拆解原子笔记单位。  
  
当然这样子拆解成原子笔记，想必 Obsidian 的 Vault 里会蹦出大量的 `XXX是什么` 的笔记。双链关系图谱可以玩出花，然而没什么用。所以我选择通过 MOC 的概念把相关的知识点汇总起来，各个原子笔记单位以 Section 的形式保存在 MOC 里：  
  
*   XXX 是什么 （MOC）  
    *   XXX 的 YYY 是什么 （Section 1）  
    *   如何 把 XXX 给 ZZZ 了 （Section 2）  
  
从科研工作者的角度看，MOC 就像是一篇综述，高度汇总了多个引用文献的内容，把这些知识点链接了起来。  
  
#### 简悦标注系统的应用  
  
简悦标注导出的是原文，然后就是外部引用、备注文本。导入到 Obsidian 之后，我们可以把这些内容拆解成前面所述的两类。  
  
比如我看了一篇关于简悦导出到 Obsidian 的文章。我可能标了很多关于 `如何把简悦标注导出到 Obsidian` 的标注，此时我可能会：  
  
*   导出标注到 Obsidian （文献笔记）  
*   新建一篇 `如何把简悦标注导出到 Obsidian` 的笔记，然后根据自身的尝试写好 “实验” 记录  
*   引用文献笔记的标注内容做溯源  
  
到这里，标注模板上预先设置的 Block ID 就有用了。通过 `Obsidian42 - Text Transporter` 插件，在标注引用块里任意位置右键就可以选择 `Copy block embeds from this selection` 以及 `Copy block embeds as an alias` ，就可以快速地把这段标注贴到别的笔记里。  
  
![](https://user-images.githubusercontent.com/396190/170810857-6d81105e-4b06-456e-8994-14d20ece9c4f.png)  
  
然后每个 Hightlight 前面的笔记图标悬停鼠标就可以溯源。在这里我也推荐这个叫 `Hover Editor` 的神器。  
  
![](https://user-images.githubusercontent.com/396190/170810847-c6b62d50-30bd-4293-a471-a949cdf1874d.png)  
  
那么随着自己的文章阅读积累，越来越多的简悦标注导出的文章出来，`如何把简悦标注导出到其他平台` 的 MOC 就出来了，然后随着你越来越多地了解简悦的其他功能，`简悦是什么` 的 MOC 也就随之出来了……  
  
所以 Obsidian 其实是一个第二大脑养成的游戏，非常上头根本停不下来。  
  
# 补充  
  
以下内容来自简悦官方。  
  
关于简悦与 Obsidian 的更多联动方案，[请看这里](https://github.com/Kenshin/simpread/discussions?discussions_q=label%3Aobsidian)。  
  
   
  
请教一下大佬  
  
标注的外部引用    
对应的占位符是 {{an_refs}} 。虽然作者没有明说这个东西干什么用，但是我后来发现，外部引用可以不止是 URL 地址。比如 Markdown 链接，又比如指向 Obsidian 里的 MOC 的 Wikilinks，来与其他永久笔记建立双链。那怎么在简悦的稍后读里快速输入 Obsidian 的双链呢？我通过 quicker 写了一个简单的脚本进行实现  
  
这个地方的 quicker 脚本请问能分享一下吗？我找了很久没找到  
  
   
  
[@1wingedangel](https://github.com/1wingedangel)  
  
请问那个评论模板解析不出来应该怎么解决，dataview 没有显示出评论，是复制你的代码后需要哪里改一下吗  
  
![](https://user-images.githubusercontent.com/55050981/199924043-cddc20d4-cf1d-490d-8863-31bacd342b9e.png)  
  
   
  
嗨，各位。  
  
简悦官方针对新用户或不喜欢配置的用户，发布了一个新功能：**Obsidan 配置库**。  
  
细节请看下面，几分钟就能配置成完成。  
  
![](https://camo.githubusercontent.com/093ac4351ff1633e5a52a8277978ec67ab9921093f65c019c6231cfb25cb8719/68747470733a2f2f696d67732e7a68756261692e6c6f76652f63363236363738666636623634646431616339646664616536636636643138382e706e67)  
  
针对新用户的一步到位的 Obsdian 配置库。  
  
## 🗂 配置库  
  
[简悦 · 配置库](https://www.yuque.com/kenshin/simpread/ds8zk0) 是简悦官方推出的一套针对新用户的极简配置方案，方便新用户用最快的方式使用简悦的各种高级服务，配置库内置了常用的双链笔记用法，如：Notion、Obsidian、Logseq、Roam Research，同时包含了简悦在阅读模式上的一些常规插件：Live Editor、题图、Safari 阅读模式等。  
  
## 💡 特点  
  
用户仅需要下载对应的配置库，修改里面的 UID 为自己的高级账户 UID，即可实现简悦的各种高级操作。  
  
## 💁‍♂️ 受众  
  
新用户或者不想使用手动配置的用户。  
  
## 📝 如何使用  
  
1️⃣ 下载  
  
2️⃣ 修改为自己的 UID  
  
3️⃣ 将必要的文件夹复制粘贴到相应位置  
  
✅ Done！  
  
## 📚 Obsidian 配置库  
  
## 📝 特点  
  
1️⃣ 加入稍后读，自动将本地快照和 Markdown 导入到 Obsidian  
  
2️⃣ 加入标注时，自动将标注内容导入本地快照和 Obsidian  
  
3️⃣ 改变稍后读或标注的元数据时，自动将改动的内容保存到本地快照和 Obsidian  
  
4️⃣ 在 Obsidian 中直接内置好了简悦的标注系统，可直接在 Obsidian 实现标注  
  
## 📖 区别  
  
![](https://camo.githubusercontent.com/56dd1b1346d73b07f4ef51c044b2cffba62654a0e9fc6facde3165f2b7a24605/68747470733a2f2f696d67732e7a68756261692e6c6f76652f66346135316438653866623434303132383162303766383262663062633764312e706e67)  
  
## 📘 极速版  
  
🔗 [Github](https://github.com/Kenshin/simpread-configs/blob/main/obsidian@little/Getting%20Started.md) | [语雀](https://www.yuque.com/kenshin/simpread/xkuecp)  
  
不需要同步助手，无任何配置，支持 Markdown 形式的快照，自动同步标注，适合 Obsidain + 简悦的尝鲜用户。  
  
## 📙 基础版  
  
🔗 [Github](https://github.com/Kenshin/simpread-configs/blob/main/obsidian@localrestapi/Getting%20Started.md) | [语雀](https://www.yuque.com/kenshin/simpread/cg33gh)  
  
需要同步助手，几乎无任何配置，支持本地快照，自动同步标注，适合 Obsidain + 简悦的轻量级用户。  
  
## 📗 高级版  
  
🔗 [Github](https://github.com/Kenshin/simpread-configs/blob/main/obsidian@sync/Getting%20Started.md) | [语雀](https://www.yuque.com/kenshin/simpread/wq35mh)  
  
需要同步助手，几乎无任何配置，支持本地快照，自动同步标注，可在 Obsidian 中标注，适合 Obsidain + 简悦的重度用户。