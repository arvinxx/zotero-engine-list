# Zotero 检索引擎清单

![][version-url] [![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release) ![][license-url]

[version-url]: https://img.shields.io/github/v/release/arvinxx/zotero-enginelist
[license-url]: https://img.shields.io/github/license/arvinxx/zotero-enginelist

## 简介

Zotero 检索引擎可以基于 Zotero 的元数据快速跳转检索。

### 引擎简介

| 检索引擎               | 简介                                                                                   | 用处/领域                        | 状态 |
| ---------------------- | -------------------------------------------------------------------------------------- | -------------------------------- | ---- |
| Google                 | 略                                                                                     | 通用检索                         | ✅   |
| WikiPedia              | 略                                                                                     | 通用检索                         | ✅   |
| Google Scholar         | 谷歌学术                                                                               | 通用论文                         | ✅   |
| Semantic Scholar       | 一个基于 AI 构建的论文检索工具,用来找关键论文挺方便                                    | 通用论文                         | ✅   |
| CrossRef               | DOI 的综合检索网站,只要有 DOI,用这个检索一般都能找到源网站                             | 通用论文                         | ✅   |
| ProQuest               | 收录了全球各个学科的英文硕士和博士学位论文，并主要提供 1997 年之后学位论文的全文下载。 | 通用论文(硕博)                   | ✅ ️ |
| Sci-Hub URL            | Sci-Hub 就不介绍了                                                                     | 通用论文                         | ✅   |
| ACM                    | 计算机 HCI 领域论文检索专用                                                            | 计算机/HCI 论文                  | ✅   |
| Connected Papers       | 这个比较有意思,可以根据一篇论文查询其引用关系,论文综述检索时比较有用                   | 文献综述                         | ✅   |
| LibGen                 | 查英文 PDF 的唯一权威                                                                  | 英文书籍                         | ✅   |
| 豆瓣读书               | 一般用于录入书籍元数据                                                                 | 中文书籍                         | ✅   |
| 全国图书馆参考咨询联盟 | 查中文书是否有 PDF 的权威网站                                                          | 中文书籍                         | ✅   |
| World Cat              | 世界最大的图书馆目录网站,豆瓣上查不到的 ISBN 这上面都能查到                            | 通用书籍                         | ✅   |
| iJournal 爱期刊        | 期刊影响因子检索                                                                       | 论文                             | ✅   |
| CNKI                   | 中文论文的检索网,但估计以后是用不到了                                                  | 国内论文                         | ✅   |
| 豆瓣电影               | 搜电影,个人用不到                                                                      | 电影                             | ⛔️  |
| Web of Science         | 没用过                                                                                 | 自然科学/社会科学/人文科学类论文 | ⛔️  |

✅ ：启用状态； ⛔️ ：禁用状态

## 使用方法

### 下载

点击右侧 [Releases](https://github.com/arvinxx/zotero-engine-list/releases) 最新版,然后点击 `engines.json` 进行下载。

![](https://gw.alipayobjects.com/zos/antfincdn/ZvHNOnAe9j/90570276-9854-4727-8401-07c14a4931fa.png)

## 手动创建

如果因为网络问题无法下载，可以手动创建一个 `engines.json` 文本文件，然后将 [src/engines.json](https://github.com/arvinxx/zotero-engine-list/blob/master/src/engines.json) 中所有文本内容复制保存即可。

### 安装

下载完成该引擎文件后，需要将该文件放到 Zotero 库的 `/locate`下面，方可完成安装。
例如，如果 Zotero 路径为 `/Users/arvinxx/Zotero`，那么把上述文件放到以下目录：

```
/Users/arvinxx/Zotero/locate
```

完成放置后，重启 Zotero 即可。

![](https://gw.alipayobjects.com/zos/antfincdn/%24zkLytwaI%24/25c32391-88b6-422c-9725-28b615cbae49.png)

## 启用的引擎清单

本引擎清单所启用的引擎如下：（只有选中条目后方可查看）

### 图书

![](https://gw.alipayobjects.com/zos/antfincdn/1RZF5Wkvjm/4fd6a5bc-9392-48cb-891f-206d308dee43.png)

### 论文

![](https://gw.alipayobjects.com/zos/antfincdn/8mopbkZqpN/62ebb9ac-266b-4571-8265-8ef3562f7d96.png)

## 奇技淫巧

### 配置文件软连接

【适用于 macOS 和 Linux】

利用软连接将仓库中的 `engine.json` 文件链接到 Zotero 库下：

```shell
ln -s /仓库路径/src/engines.json /Zotero库路径/locate/engines.json
```

例如:

```shell
ls -s /Users/arvinxx/CodeProjects/zotero-engine-list/src/engines.json /Users/arvinxx/Zotero/locate/engines.json
```

这样就可以实现仓库中更新配置后，只需重启 Zotero 即可。

也可以用类似的方式配置文件链接到云盘，进而实现单配置文件的云端同步。

### 如何添加新引擎

请移步 [创建 Zotero 引擎](https://www.yuque.com/arvinxx/research/create-new-engine)

## LICENSE

[MIT](./LICENSE) ® Arvin Xu
