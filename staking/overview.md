---
title: 概况
description: Thales提供质押功能，代币持有者可通过使用代币提名收集人并获得奖励
---

# Thales质押挖矿

![Staking Thales Banner](/images/staking/staking-overview-banner.png)

## 概览

Thales基于[Polkadot权益证明模型](https://wiki.polkadot.network/docs/en/learn-consensus)进行区块生产，因此区块链上有收集人（Collator）和验证人（Validator）。[收集人（Collator）](https://wiki.polkadot.network/docs/en/learn-collator)通过收集用户的交易并为中继链[验证人（Validator）](https://wiki.polkadot.network/docs/en/learn-validator)生成状态转移证明来维护平行链（在这一例子中为Thales）。

网络中质押权益的人将入选收集人群体（生产区块的节点）。而质押挖矿在这里起到重要作用。

收集人（以及参与其提名的代币持有者）在网络中持有权益。但如果行为不当，其权益会被削减。因此权益越高，网络安全性越高，收集人也更有可能入选，进行区块生产并赚取奖励，与其提名人分享收益。这样的机制能够激励网络成员进行质押挖矿，从而提升网络整体安全性。

## 般定义

--8<-- 'text/staking/staking-definitions.md'

目前，对于Thalesbase Alpha来说，上述参数具体如下：

|          变量          |      |                              值                              |
| :--------------------: | :--: | :----------------------------------------------------------: |
|     最低提名质押量     |      |     {{ networks.thalesbase.staking.min_nom_stake }} tokens     |
|     最低提名持有量     |      |     {{ networks.thalesbase.staking.min_nom_amount}} tokens     |
| 每位收集人的提名者限额 |      |       {{ networks.thalesbase.staking.max_nom_per_col }}        |
| 每位提名者的收集人限额 |      |       {{ networks.thalesbase.staking.max_col_per_nom }}        |
|          轮次          |      | {{ networks.thalesbase.staking.round_blocks }} blocks ({{ networks.thalesbase.staking.round_hours }} hours) |
|        绑定时长        |      |       {{ networks.thalesbase.staking.bond_lock }} rounds       |

## 奖励发放

在每个轮次的最后（{{ networks.thalesbase.staking.round_blocks }}区块），收集人将获得{{ networks.thalesbase.staking.bond_lock }}轮之前的收益奖励。

收集人加入收集人节点群后，将会对提名人所提供的服务收取佣金，奖励发放遵循以下规则：

 - 佣金将在发放的奖励中扣除
 - 收集人的奖励将根据其网络权益加佣金进行发放
 - 其余奖励将根据权益比例发放给每一个提名人

收集人的奖励组成可用下数学公式表示：

![Staking Collator Reward](/images/staking/staking-overview-1.png)

公式中的权益等于收集人绑定的代币数量与其总质押代币量之比（会计提名）。

每个提名人的奖励计算公式如下：

![Staking Nominator Reward](/images/staking/staking-overview-2.png)

公式中的权益等于提名人绑定的代币数量与收集人持有总代币量之比。

## 在Thalesbase Alpha上进行尝试

在Thalesbase Alpha测试网上，代币持有者可以进行质押挖矿并赚取奖励，以测试该系统（系统中的代币没有任何实际价值）。

具体使用方法请查看[此教程](https://docs.thales.network/staking/stake/)。