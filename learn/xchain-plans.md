---
title: 跨链集成
description: Thales的跨链集成将支持基于波卡（Polkadot）的平行链及非波卡链（如以太坊）。
---

# 跨链集成方案

Thales所规划的重要功能之一，就是为开发人员人员提供更便利的方式来通过智能合约实现与其他波卡（Polkadot）生态系统各类项目的集成。

波卡（Polkadot）定义了低层级的集成协议，即“跨链消息传递 ”（XCMP）。通过 XCMP可达到波卡（Polkadot）网络各平行链之间的信息交互，共享可信逻辑，即“共享受保护的运行时执行飞地”模块（SPREE ）。截至本文撰写时（2020年7月），Parity已经在进行实施XCMP和SPREE的设计。在波卡（Polkadot）主网上线之后，XCMP结构和SPREE模块将作为波卡（Polkadot）中继链的升级功能发布，Thales计划在这些协议功能生效后，即可对各种集成场景执行并支持。

## 与波卡（Polkadot）平行链的集成

波卡（Polkadot）将起到与Linux系统相似的功能。这两个系统都是以开发人员为中心的平台，通过各种库来使应用程序开发变得更为便捷。

在Unix哲学中，用户根据某一功能需求来开发工具，并让该工具在满足这一特定功能方面做到最好。同样地，我们希望波卡（Polkadot）系统中的平行链也能实现这样的专门化功能。在Linux系统中，这些专门化工具可以进行结合，并使用bash shell脚本实现高阶效应。基于Thales的智能合约为专门化的智能合约和平行链功能提供“bash like”的环境配置，实现高阶效应。

目前来看，各个项目可能从一个或多个智能合约开始逐步迁移到Thales，最终成为Thales网络上的“原生应用程序”。如果这些项目需要更多的曝光或者想要直接控制自己的经济环境，那么还有可能成为波卡（Polkadot）系统中的平行线程或平行链。

## 与基于波卡（Polkadot）网络各类项目的集成

我们最初希望实现的是能将其他链上的代币转换成Thales平台上的代币，并在平台的DeFi和其他应用程序中使用。完成相应任务后，这些代币又可以重新转回或者转移到其他链。

随着波卡（Polkadot）网络集成功能的不断完善，我们将继续帮助开发人员通过智能合约获取这些集成功能，并通过Thales智能合约在各个区块链上创建新功能。

## 与以太坊的集成

Thales与以太坊的集成至关重要，只有这样才能为以太坊生态项目提供支持，尤其是混合部署——同时在以太坊和Thales网络上部署的项目。目前已有至少一个独立于Thales的项目在打造基于平行链的以太坊桥，功能进入运营后，就可以利用波卡（Polkadot）提供相应机制，在生态系统区块链和以太坊之间进行代币转移、状态和消息发送。

在平行链桥接功能实现之前，我们提供两种解决方案来帮助项目实现Thales与以太坊的集成：

 1. 我们提供了一个应用工具，可以将以太坊状态输出为二进制代码，从而再导入Thales。这一应用工具将实现单次、单向的信息迁移。
 2. 此外，我们还提供直接并入Thales的点对点以太坊桥，可以实现代币转移和跨链状态查询及消息传递。随着波卡（Polkadot）生态系统不断发展，我们希望今后能够出现更多的以太坊集成方案供项目进行Thales部署选择。