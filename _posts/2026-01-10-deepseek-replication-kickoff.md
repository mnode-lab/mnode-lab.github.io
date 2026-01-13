---
layout: post
title: "DeepSeek V3 低成本复现实验启动"
date: 2026-01-10 10:00:00 +0800
author: "μNode Lab"
categories: [analysis, engineering-log]
tags: [DeepSeek, Infra, Cost-Analysis]
featured: true
excerpt: "专业拆解 DeepSeek 技术报告中的 Infra 成本账，更新环境信息，并提出用 500 万 RMB 复现 1 个亿集群并发能力的技术假设。"
---

## 叙事逻辑："DeepSeek 论文的低成本复现实验"

既然 DeepSeek 证明了通过极致 infra 优化可以降本，我们作为一个中立的技术团队，试图验证：**能否用消费级硬件 + 内存/ssd + 软件架构优化（Micro-Node 思路），将这个成本账门槛再降低一个数量级？**

### 价值主张

用 **500 万 RMB**（约 $700k）的成本，复现 DeepSeek 技术报告中 **1 个亿**（约 $15M）集群的并发能力（1600 并发）。

#### 行业标准方案

Nvidia H 系列集群（贵、缺货、标准答案）

#### New Option

较群 Micro-Node 集群（便宜、现货，需要技术动手能力和新的推理框架支持）。延伸到对应的分布式推理框架思想，为开源社区提供新的推理框架思路，为力源细路。

### 启动调性

**Cyberpunk / Hacker / Underdog**。不是一家芯片公司在卖产品，而是一个极客团队/中立 hacker 组织在挑战行业巨头的暴利定价体系。

### 风险控制

#### 海外

去"中国芯片厂商"标签，强化"开源硬件/社区项目"属性。

#### 国内

强调"降本增效"与"AI 基础设施新范式"。

---

## 核心问题

**现在用消费级硬件重新跑这笔成本账，性能到底能走到哪一步？**

这不是创业项目，没有融资计划。

纯粹技术验证，全程开源。

可能成功，可能失败，我们会如实记录。

---

## 接下来的计划

### 阶段一：定义与预热（第 1-3 周）

**目标**：内容预热，抛出"反直觉"或行业觉得"小众"的理论做开局讨论，引发关注（争议也不错）。

**核心动作**：根据之前的 blog，写一个对应的工程化设计文章。海外媒体矩阵开始工作。

**内容描述**：

1. **拆解论文**：专业拆解 DeepSeek 技术报告中的 Infra 成本账，更新一些当下的环境信息或数据（比如如果是 H200 呢？）。

2. **提出假设**：抛出"数群"架构图，如果用 40 台消费级或改机器（每台成本 <10 万）——用 SSD 做 Prefill，用 CPU+GPU 异构做计算，用普通网卡做互联。

3. **发出邀请**：宣称我们将用 $700k（500万RMB）的预算去验证这个架构，邀请社区监督或提供建议。

**渠道**：Hacker News, Twitter (X), Reddit (r/LocalLLaMA, r/MachineLearning, r/Hardware), GitHub Discussions。

---

## 资源准备

- **启动文章**：DeepSeek 论文的低成本复现实验，需要结合一些相关技术信息更新，把整套逻辑串顺一遍，抛出实验启动信号。
- **设定一个前台组织**，定性为 Open Research Challenge。
- **基础账号**（养号和配套工具的工作流）。

---

## 关于我们

**μNode Lab** | Micro-Node Research Group

Replicating DeepSeek V3 limits on consumer hardware.

Repo: [github.com/mnode-lab](https://github.com/mnode-lab)
