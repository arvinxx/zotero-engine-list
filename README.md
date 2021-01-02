# Zotero Engine List 检索引擎清单

启用引擎清单

![](https://gw.alipayobjects.com/zos/antfincdn/XnJTWqQaeo/831a8c93-c2b5-4dfe-b7b6-6d306eda732a.png)

## 使用方式

下载 [engine.json](https://raw.githubusercontent.com/arvinxx/zotero-enginelist/master/engines.json) 该引擎清单,放到 Zotero 库的 `/locate`下面。例如，我的 Zotero 路径为 `/Users/arvinxx/Zotero` ,那么把这个文件放到 `/Users/arvinxx/Zotero/locate` 目录下，然后重启 Zotero 即可。

## 简介

✅ ：启用状态； ⛔️ ：禁用状态

| 检索引擎               | 简介                                                                 | 领域                             | 状态 |
| ---------------------- | -------------------------------------------------------------------- | -------------------------------- | ---- |
| Google                 | 略                                                                   | 通用检索                         | ✅   |
| WikiPedia              | 略                                                                   | 通用检索                         | ✅   |
| Google Scholar         | 谷歌学术                                                             | 通用论文                         | ✅   |
| Semantic Scholar       | 一个基于 AI 构建的论文检索工具,用来找关键论文挺方便                  | 通用论文                         | ✅   |
| ACM                    | 计算机 HCI 领域论文检索专用                                          | 计算机/HCI 论文                  | ✅   |
| CrossRef               | DOI 的综合检索网站,只要有 DOI,用这个检索一般都能找到源网站           | 通用论文                         | ✅   |
| Sci-Hub URL            | Sci-Hub 就不介绍了                                                   | 自然科学/社会科学/人文科学类论文 | ✅   |
| Connected Papers       | 这个比较有意思,可以根据一篇论文查询其引用关系,论文综述检索时比较有用 | 检索                             | ✅   |
| LibGen                 | 查英文 PDF 的唯一权威                                                | 英文书籍                         | ✅   |
| 豆瓣读书               | 一般用于录入书籍元数据                                               | 中文书籍                         | ✅   |
| 全国图书馆参考咨询联盟 | 查中文书是否有 PDF 的权威网站                                        | 中文书籍                         | ✅   |
| World Cat              | 世界最大的图书馆目录网站,豆瓣上查不到的 ISBN 这上面都能查到          | 通用书籍                         | ✅   |
| CNKI                   | 中文论文的检索网,但估计以后是用不到了                                | 国内论文                         | ✅   |
| 豆瓣电影               | 搜电影,个人用不到                                                    | 电影                             | ⛔️  |
| Web of Science         | 没用过                                                               | 自然科学/社会科学/人文科学类论文 | ⛔️  |

## 奇技淫巧

### 配置文件软连接

【适用于 macOS 和 Linux】

利用软连接将仓库中的 `engine.json` 文件链接到 Zotero 库下：

```
ln -s /仓库路径/engines.json /Zotero库路径/locate/engines.json
```

这样就可以实现仓库中更新配置后，只需重启 Zotero 即可。

也可以用类似的方式配置文件链接到云盘，进而实现单配置文件的云端同步。
