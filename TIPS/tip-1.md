---
tip: 1
title: TIP的作用介绍
status: Active
type: 过程改进
author: xiao8 <1018053166@qq.com>
created: 2018-09-05
---

## 什么是TIP?

TIP是Taireum改进提案的缩写。TIP是为Taireum社区提供建议或描述Taireum流程或环境的新功能的设计文档。TIP应该提供特性的简明技术规范和特性的基本原理。TIP作者负责在社区内建立共识并记录不同意见。

## TIP 原理

我们希望TIPs成为提出新特性的主要途径，收集社区中的某个问题，并记录是否已进入Taireum下个版本的设计决策。因为TIP是作为版本存储库中的文本文件来维护的，所以它们的修订历史记录就是特性建议的历史记录。

对于Taireum使用者来说，TIPs是跟踪其实现进度的便捷方法。

## TIP 类型

以下是TIP的三种类型:

-  **标准 TIP** 针对Taireum项目的任何修改的提案，例如共识模块的更改，网络模块的更改，应用程序的规范和定义等。TIP标准可以分为以下几类。
  - **核心** - 核心功能的变更讨论
  - **TRC** - 应用程序的规范和约定，包括合约规范，例如联盟链中的通证定义规范，权限模型等
-  **建议 TIP** 描述Taireum目前存在的问题，向Taireum社区提供信息和建议，但不是新功能
-  **改进过程 TIP** 通过围绕目前Taireum的更新和实现，对过程进行优化，需要由社区达成共识。

强烈建议一个提案包含一个关键建议或想法，不能重复提交提案。

TIP必须符合某些最低标准。它必须清楚和完整地描述提案。

## TIP 工作流程

参与此过程的各方是您、拥有者或*TIP作者*、[*TIP编辑者*](# tips编辑者)和[*Taireum核心开发人员*]。

:warning: 在此之前，您可以先验证您的想法。可以先与Taireum社区用户进行交流探讨。该TIP最好能在社区建立一个共识。

您作为拥有者的角色来使用下面描述的风格和格式来编写TIP，在论坛中进行讨论，并围绕这个想法建立社区共识。下面是一个成功的技巧的过程:

```
[ WIP ] -> [ DRAFT ] -> [ LAST CALL ] -> [ ACCEPTED ] -> [ FINAL ]
```

每个状态更改由TIP作者请求，并由TIP编辑人员审阅。使用pull request更新状态。包括一个链接，人们应该继续讨论你的TIP。TIP编辑者将按照以下条件处理这些请求。

* **Active** -- 一些建议和过程TIP可能也具有“Active”状态，如果它们永远不打算完成。例如：tip-1(当前TIP)。
* **Work in progress (WIP)** -- 一旦拥有者问过Taireum社区的一个想法是否有可能得到支持，他们将会以pull request的形式写出一个草案。如果可以帮助人们，可以考虑加入一个实现。
  * :arrow_right: Draft -- 如果同意，TIP编辑者将为提示分配一个编号(通常是与TIP相关的问题或PR数字)，并合并您的pull request。TIP编辑者不会不合理地拒绝TIP。
  * :x: Draft -- 拒绝草案状态的原因包括太不集中、太宽泛、重复工作、技术上不健全、没有提供适当的动机或解决向后兼容问题，或者不符合[Taireum哲学]
* **Draft** -- 一旦第一稿被合并，您可以提交后续的pull request，并对草稿进行进一步修改，直到您认为成熟并准备好进入下一个状态为止。必须实现草案状态中的TIP，以考虑将其提升到下一个状态
  * :arrow_right: Last Call -- 如果同意，TIP编辑者将分配最后一次调用状态，并设置一个审查结束日期，通常是14天后。
  * :x: Last Call -- 如果仍然希望对草案进行修改，则将拒绝请求最后的通知状态。我们希望TIP避免在RSS上产生不必要的提案。
* **Last Call** -- 本TIP将在http://taireum.github.io/TIPs/网站(通过RSS订阅[last-call.xml](/last-call.xml))中列出。
  * :x: -- 如果出现大量未处理的技术投诉，将导致TIP返回到草稿。
  * :arrow_right: Accepted (当TIPs的类型为核心的时候) -- 如果没有重大变更或未处理的技术投诉将变为Accepted。
  * :arrow_right: Final (当TIPs的类型不为核心的时候) -- 如果没有重大变更或未处理的技术投诉将变为Final。
* **Accepted (当TIPs的类型为核心的时候)** -- 这个TIP掌握在Taireum客户端开发者手中。是否将其作为硬fork的代码由开发者自己决定。
  * :arrow_right: Final -- 当TIPs类型为核心类型的时候，则必须在至少三个可运行的Taireum客户端实现，才能被认为是最终的。当执行完成并被社区采纳后，该状态将更改为“Final”。
* **Final** -- 当TIPs状态为“Final”时，只能更新修正来错误。

其他例外情况包括:

* Deferred -- 推迟的核心建议
* Rejected -- 被核心开发者拒绝并且不会被实现
* Active -- 这与Final类似，但是表示一个提示，可以在不改变TIP编号的情况下进行更新。
* Superseded -- 取代之前的TIP



## TIP 格式和模版

提示应该以[markdown]格式书写。
图像文件应该包含在“assets”文件夹的子目录中，如下所示:当链接到提示中的图片时，使用相关链接，例如“../assets/tips-x/image.png”。

## TIP 头信息

每个提示必须以RFC 822样式的头信息开头，前面和后面必须有三个连字符(' --- ')。标题必须按照以下顺序显示。标为“*”的标头是可选的，如下所述。所有其他标头都是必需的

` TIP:` <TIP 编号> (编号由 TIP 编辑者决定)

` title:` <TIP 标题>

` author:` <作者列表 或者 作者的名称(s) 并且/或者 用户名(s), 或者 名称(s) and 邮箱(s). 以下是细节.>

` * discussions-to:` \<a url pointing to the official discussion thread\>

 - :x: `discussions-to` 不能成为 Github `Pull-Request`.

` status:` <Draft | Last Call | Accepted | Final | Active | Deferred | Rejected | Superseded>

`* review-period-end: YYYY-MM-DD

` type: `<规范 (核心, TRC)  | 建议 | 过程改进>

` * category:` <核心 | TRC>

` created:` <date created on, in ISO 8601 (yyyy-mm-dd) format>

` * requires:` <TIP 数量(s)>

` * replaces:` <TIP 数量(s)>

` * superseded-by:` <TIP 数量(s)>

` * resolution:` \<a url pointing to the resolution of this TIP\>

## 辅助文件

提示可能包括辅助文件，如图表。这些文件必须命名为tips-xxxx-y.ext，其中“XXXX”是提示号，“Y”是序号(从1开始)，“ext”被实际文件扩展名替换(例如“png”)。

## 更改 TIP 作者

有时需要讲TIP的作者换成其他用户。例如原作者已经没有兴趣更新该TIP。
如果你对该TIP有兴趣，可以与原作者和TIP编辑进行沟通。

## TIP 编辑者

当前 TIP 的编辑者

` * xiao8 (@1018053166)`

` * Zhihui Li (@itisaid)`

` * eric-wang (@eric-wang)`

## 历史

这份文件很大程度上源自阿米尔·塔基(Amir Taaki)写的[比特币BIP-0001]，反过来又源自[Python的PEP-0001]。在许多地方，文本只是简单地复制和修改。虽然PEP-0001文本是由Barry Warsaw, Jeremy Hylton和David Goodger编写的，但是他们不负责在Taireum改进过程中使用它，也不应该被Taireum或TIP特有的技术问题所困扰。请将所有评论直接发送给TIP编辑。

## 版权

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
