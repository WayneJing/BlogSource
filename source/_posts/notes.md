---
title: notes
date: 2016-07-05
categories: 电气工程
tags:
    - deferrable demand
    - 柔性建模
    - 机组组合
---

 Notes about [Large-scale integration of deferrable demand and renewable energy sources](http://ieor.berkeley.edu/~oren/pubs/No113.pdf)

#  ABSTRACT
> - [ ][stochastic unit commitment model](http://s3.amazonaws.com/academia.edu.documents/42998787/A_Stochastic_Unit-commitment_Model_for_t20160223-1673-5tjopb.pdf?AWSAccessKeyId=AKIAJ56TQJRTWSMTNPEA&Expires=1467280071&Signature=12zFdv9seJSAEfV1OBP2emAFj9I%3D&response-content-disposition=inline%3B%20filename%3DA_stochastic_unit-commitment_model_for_t.pdf) 随机机组组合模型  **？**
> - [ ]deferrable demand in power system 电力系统中的可暂缓需求**（可调性需求？）**
> - [x]reserve requirements 储能需求
> - [ ]the benefits of demand flexibility 需求弹性收益 **？**
> - [x]three demand response paradigms 三个需求响应的样例
> > - [ ]the centralized co-optimization of generation 发电的集中联合优化 **？**
> > - [x]demand by the system operator, demand bids 来自于系统操作人员和订单的需求
> > - [ ]the coupling of renewable resources with deferrable loads 可再生能源与可调性负载的耦合 **？**
>
> - [ ]motivate coupling as an alternative for overcoming the drawbacks of the two alternative demand response options 将耦合作为克服另外两个需求响应缺点的替代选项
> - [x]a dynamic programming algorithm for coordinating deferrable demand with renewable supply 一个用于协调可调性需求与可再生能源供给的动态算法
> - [ ]simulation results for a model of the [Western Electricity Coordinating Council](https://www.wecc.biz/Pages/home.aspx) 关于[西部电力协调理事会](https://en.wikipedia.org/wiki/Western_Electricity_Coordinating_Council)的模型仿真结果
> - [ ]load management 负载管理
> - [ ]power generation scheduling 电力发电规划
> - [ ]wind power generation 风力发电

---

<!-- more -->

# INTRODUCTION

> - high variability, unpredictable fluctuation, a limited control of output
> 与传统发电方式相比，可再生能源的关键缺陷在于它的高变化性，波动不可预测和输出仅在有限范围内可控
> - demand response
> 需求响应对于大规模的可再生能源是很有好处的
> - represent the balancing operations of the remaining grid by using a unit commitment model
> 用一个机组组合模型来表示当前电网的平衡措施来评估可再生能源与需求响应的影响
> - doesn't model the deferrable nature of various of various demand response or account for the uncertainty that is introduced by the large-scale integration of renewable resources
> 以往这个领域的研究没有就变化的需求响应的可调性特征建模，也没有考虑由大规模可再生能源导致的不确定性
> - economic dispatch model
> 经济调度模型
> - explore the direct coupling of deferrable consumers with renewable resources into a virtual resource through a contractual agreement based on a strike price that limits the impact of the coupled system on the rest of the network
> 探索了在限制耦合系统对于网络其他部分的影响的成交价下将可调性负载与可再生能源直接耦合接入虚拟。。。（不是很懂）

## Literature Review

> - high investment cost of backup reserves
> 后备储能设施的投入来保证系统的可靠操作
> -  quantifying reserve requirements as well as the impacts of renewable integration on operating costs
> 定量储藏要求和可再生能源对于运行损耗的影响
> - impact of renewable supply uncertainty on power system operations (focus)
> 可再生能源供应的不确定性对电力系统操作的影响
> - the potential benefits of demand response integration
> 一体化需求响应的潜在好处 **？**
> - demand function
> 需求函数
> - However, many flexible consumption tasks are best characterized as deferrable, in the sense that consumers need a certain amount of energy within a certain time window. As such, deferrable demand behaves much like a hydro or storage resource from the view point of the system operator. Electric vehicle charging, agricultural pumping, pre-cooling, and residential consumption such as laundry fit this characterization.
> **为什么更像一个水电或者储存？农业泵，洗衣机为什么相似？**
> - real-time pricing at the retail level
> 需要实时电价
> - volatility of wholesale electricity prices
> 批发电价的波动性
> - the [non-convex](https://en.wikipedia.org/wiki/Non-convexity_(economics)) costs of system operations
> 实时电价由于系统运行中的非凸成本（有绝对的需求时）不能表达出需求响应的经济价值      **为什么是非凸的？**
> - excessive startup and minimum load costs
> 上述问题会导致过多的启动和最小负载成本
> -  the system operator dispatches the system at a bulk scale and cannot control individual retail loads
> 只能在大规模上，不能分布式
> - concerns about defining market products that correspond to the types of services that loads can actually offer, which raises the need for reform in existing electricity markets
> 需要对现有市场进行改革

## Paper Contributions

> - **a stochastic unit commitment model that can be used in order to quantify the benefits of deferrable demand in mitigating the increased operating costs and day-ahead reserve requirements resulting from the random fluctuation of renewable energy supply**
> 一个可以用来量化可延缓需求在减少增长的运行损耗和由于可再生能源的随机波动导致的提前一天的存储需求
> - The use of stochastic planning models for simulating long-term market equilibrium in order to quantify generation investment in the face of long-term uncertainty
> 用随机规划模型来模拟长期市场均衡以用来量化面对长期不确定性情况下的发电投资
> - used in order to simulate the two-stage operation of day-ahead and real-time electricity markets
> 用来模拟提前一天的二阶操作和实时的电力市场
> - computational challenges
> - using an appropriate scenario selection technique to discretize the uncertainty space of the [problem](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4806110)
> - **extend existing models by simultaneously modeling the inter-temporal dependency of deferrable demand and renewable supply uncertainty**
> 跨时间段的依赖关系和可再生能源供给的随机性
> - present a contractual alternative for coupling the operations of renewable resources with deferrable demand that attempts to overcome the implementation barriers associated with centralized load dispatch and real-time pricing of retail loads, and compare the relative performance of each demand response paradigm in terms of system operating costs
> 展现了一个（（具备试图克服执行障碍和集中负载调度的可调需求的可再生资源的操作）与（基于零售负载的实时电价的耦合））的基于合同的替代选项，并且比较了在系统运行损耗中各个不同的需求响应模式的表现

---

# MODEL OVERVIEW



> - Uncertainty in the model is driven by renewable supply and demand.
> - Demand resources in the system are categorized as inflexible (firm) consumers with stochastic consumption patterns and deferrable consumers that require a fixed amount of energy within the day and adapt their instantaneous consumption patterns to the prevailing system conditions.
> 把需求分为了两类，一类是固定用户，消耗模式随机，另一类是可调用户，需求固定，消耗模式适配到系统即时状态
> - The decision support module in the upper portion of the figure simulates day-ahead market operations and is used for determining day-ahead reserve requirements when deferrable demand contributes to absorbing the variability of renewable energy supply
> - The evaluation module in the lower portion of the figure uses the reserves committed by the day-ahead model in order to compare the real-time operating costs of the system under the three demand response paradigms that are discussed in the introduction of the paper.

## Statistical Models
> - We use a second order autoregressive model for modeling demand and load.
> [二阶自回归模型](http://baike.baidu.com/link?url=0DvVl_b1tAPmWB1whlIPgAen-oIVPTw8beF-jQWMYxU5ajNrdJ_5a5x67zbcw3XoMMPr6oWcc_I-AKD76T-Ev_)用来模拟需求和负载
> - 固定需求与可再生能源产出是相互独立的（assumption）
> - employ a data set published by NREL which provides time series of wind speed at various geographic locations over a year
> - [Yule-Walker equations](https://en.wikipedia.org/wiki/Walker_circulation#Yule-Walker_equations)
> ![Probability distribution function of inflexible demand.|center|500x0](./1467355871705.png)
> Probability distribution function of inflexible demand
> - In the present analysis we use a single-area wind model and ignore transmission constraints in order to focus on the impact of demand response.
> 在现在的分析中，我们使用了单个区域的风力模型并且为了集中于需求响应忽略了传递约束 （没做多个区域和考虑传递约束的）
> - The problem of balancing the schedules of coupled resources with the rest of the system while respecting transmission constraints would be addressed by the system operator and would be reflected in locational marginal prices from the point of view of aggregators.
> 在考虑传递约束的情况下，平衡耦合资源规划与系统其他部分的问题会有系统操作员来解决，并且从聚合的角度来看 **？**，这个结果会反映在节点边际电价上
> -  the aggregator can hedge by buying financial transmission rights
> **？** 购买输电权。。对冲

## Stochastic Unit Commitment

> - assumes that the system operator co-optimizes the dispatch of flexible loads and generation resources
> 假设系统操作员可以同时协调控制柔性负载与发电资源
> - two-stage decision model where the first stage represents day-ahead unit commitment and the second stage represents real-time economic dispatch in the hour-ahead market, in hourly intervals, subsequent to the realization of uncertainty
> 一个第一阶段表示日超前机组组合模型第二阶段表示由于不确定性的实现因而以一小时为间隔的时超前市场上的实时经济调度的二阶决策模型
> - 操作员每小时能够计算出模型结果是基础

![](/images/1.png)

> `$S$`　　a discrete set of scenarios
> `$G$`　　set of gengrators
> `$G_s$`　　set of slow generators which commitment decisions are fixed in the day-ahead time frame `$G_s\in G$`, another part are fast generators that can adjust their commitment schedule in the second stage
> `$w_{gt}$`　　First-stage decisions
> `$z_{gt}$`　the binary unit commitment and startup decisions for slow generators
> `$u_{gst}$`　　the unit commitment of all generators
> `$v_{gst}$`　startup of all generators
> `$p_{gst}$`　　power output of all generators
> `$e_{st}$`　　The dispatch of deferrable loads (a second-stage decision variable)
> `$S_{g}$`　　startup cost for each generator
> `$K_g$`　　minimun load costs for each generator
> `$C_g$`　　constant fuel costs for each generator
> `$D_{st}$`　　net demand (the net of firm demand minus renewable power supply, represents the source of uncertainty)
> `$\mathcal{D}$`　　includes generator capacity constraints, ramping constraints, and minimum up and down times, where bold fonts indicate vectors.
> - The objective function of (1) minimizes operating costs.
> - Power balance is enforced in (2).
> - The constraint of (3) requires that deferrable loads be supplied an amount of energy within a given time window.
> - (4) enforces a limit of on the consumption (e.g., charge) rate of deferrable loads.
> - The non-anticipativity constraints on first-stage decisions is enforced in (5).
> - **all generators, including slow units, can adjust their production level in the second stage**
> - The solution of the stochastic unit commitment model is described in detail by [Papavasiliou [37]](https://perso.uclouvain.be/anthony.papavasiliou/public_html/uctestV3.pdf)

---
> About scenario selection algorithm
> - scenarios are selected according to their effect on expected cost and weighed such that their selection does not bias the objective function of the stochastic unit commitment formulation
> 场景是根据他们各自对于期望损耗的效果来权衡保证选择与随机机组组合模型的目标函数无关
> - The decomposition algorithm which is employed relies on a Lagrangian relaxation scheme for scenario decomposition.
> 分解算法基于[拉格朗日松弛算法](http://baike.baidu.com/link?url=vzPK82hLesPPe4MA_lGK1bcpHJDPaelhQf4B3T_geYEJM1_WCUh7oQPo4r34y1it7ZDY56U_fE3Kh1FhlYGai_)
> - The centralized stochastic unit commitment model presented in this section presumes the ability of the system operator to centrally monitor and control individual loads.
