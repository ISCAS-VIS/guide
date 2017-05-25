# PROJECT

针对课题组内正在进行或预备开源的各个项目，提供项目代码结构与组织规范、文档介绍等内容，以便后人参考借鉴与学习

## 目录

- [项目组织](#项目组织)
- [Markdown 简要介绍](#什么是-markdown)

## 项目组织

### 必要的项目结构

不论一个项目是否对外开源，项目根目录下都应该有一个 README 说明文档，推荐使用 Markdown 语法来书写，详情见[Markdown 简要介绍](#什么是-markdown)。README 中至少需要包含以下内容：

* 项目名称
* 项目作用与介绍
* 项目运行（安装）方法，代码结构介绍及注意事项
* 项目详细文档（地址）
* 项目贡献途径

其中，项目运行方法中应该简明地将项目依赖的运行环境（软件版本等信息）、项目运行方法及常见的一些注意事项给出，同时对于项目代码，应给出项目的代码结构，具体的函数入口以及重要实现方法的说明，代码中应该具有必要的注释说明；详细文档中对于 API 接口的说明应具体包括输入数据格式及类型，函数计算返回结果及类型，函数中具体用到的关键技术概况；项目贡献途径中应给出读者是否可以贡献代码，如何贡献的说明，一般情况下，开源项目允许其他用户在发现项目错误时通过提起 issue 的形式通知团队成员，并允许其他用户通过 pull request 向项目贡献代码。

API 格式与结构可以参考 d3.js V4 API 文档,随机节选一段如下所示:

> <a name="voronoi_polygons" href="#voronoi_polygons">#</a> <i>voronoi</i>.<b>polygons</b>(<i>data</i>) [<>](https://github.com/d3/d3-voronoi/blob/master/src/voronoi.js#L19 "Source")
> 
> Returns a sparse array of polygons, one for each unique input point in the specified *data* points, corresponding to the cells in the computed Voronoi diagram. Equivalent to:
> 
> ```js
> voronoi(data).polygons();
> ```
> 
> See [*diagram*.polygons](#diagram_polygons) for more detail. Note: an [extent](#voronoi_extent) is required.

README 中其他选填的内容包括：项目持续集成、测试覆盖率、代码质量；开源许可证说明；相关资源；项目讨论社区（例如 Gitter）等等。

项目目录下除了 README 说明外，应该存放该项目的所有开源代码。代码应该通过文件夹等形式组织好，并在 README 中给出项目代码组织的简要介绍，有关具体 API 使用以及代码结构可以在详细文档中进一步描述。

*代码在本地与服务器间进行同步时请务必注意不要将用户名、密码、私钥、凭证等隐私信息（通过.gitignore在本地处理）上传到服务器上。*

### 开发方法

你可以通过 SSH 连接 Github，也可以使用 Github 提供的客户端进行登陆域项目管理。Github 提供有强大的代码组织及相关功能，包括Git版本控制，Issue讨论管理，Wiki组织，访问统计等等，其中 Wiki 可以作为一个单独的项目进行管理。

* [Github 客户端下载](https://desktop.github.com/)
* [GitHub Desktop Documentation](https://help.github.com/desktop/)

相应操作系统的使用教程请自行搜索查看。

### 协作管理

* **TEAM设置**：代码仓库可以添加 TEAM 并设置权限，其中 Admin 管理者权限可以 read、clone、push、给仓库添加成员；Write 写权限只能 read、clone、push；Read 读权限只能 read、clone；
* **Collaborators设置**：设置中点击添加 Collaborators，输入对方Github ID，等待对方回复；

### 开源许可证的选择

* [Choose an open source license](https://choosealicense.com/)

## 什么是 Markdown

Markdown 是一种方便记忆、书写的纯文本标记语言，用户可以使用这些标记符号以最小的输入代价生成极富表现力的文档：譬如您正在阅读的这份文档。它使用简单的符号标记不同的标题，分割不同的段落，**粗体** 或者 *斜体* 某些文字，更棒的是，它还可以

### 1. 制作一份待办事宜 Todo 列表

- [ ] 支持以 PDF 格式导出文稿
- [ ] 改进 Cmd 渲染算法，使用局部渲染技术提高渲染效率
- [x] 新增 Todo 列表功能
- [x] 修复 LaTex 公式渲染问题
- [x] 新增 LaTex 公式编号功能

### 2. 高亮一段代码

```python
@requires_authorization
class SomeClass:
    pass

if __name__ == '__main__':
    # A comment
    print 'hello world'
```

### 3. 绘制表格

| 项目        | 价格   |  数量  |
| --------   | -----:  | :----:  |
| 计算机     | \$1600 |   5     |
| 手机        |   \$12   |   12   |
| 管线        |    \$1    |  234  |

### 4. 更详细语法说明

想要查看更详细的语法说明，可以参考如下资源:

- [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
- [Markdown 语法说明 (简体中文版)](http://wowubuntu.com/markdown/)
- [Markdown在线编辑阅读器](https://www.zybuluo.com/)

总而言之，不同于其它 *所见即所得* 的编辑器：你只需使用键盘专注于书写文本内容，就可以生成印刷级的排版格式，省却在键盘和工具栏之间来回切换，调整内容和格式的麻烦。**Markdown 在流畅的书写和印刷级的阅读体验之间找到了平衡。** 目前它已经成为世界上最大的技术分享网站 GitHub 和 技术问答网站 StackOverFlow 的御用书写格式。
