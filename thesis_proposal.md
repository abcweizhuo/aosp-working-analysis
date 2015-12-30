% 开题报告
% 韩慧阳 @ 计算机系高性能所 | 导师：陈康
% \today

# 毕设题目
基于大数据的安卓隐藏开发过程的分析和AOSP未来版本feature的预测
（题目不太会写，不知道主题对不对）

# 研究目的

 - 根据AOSP的开源特性确定将来版本将会出现的新的feature或者将会减少的现有feature
 - 为当前的安卓软硬件看法提供方向性的参考

# 研究现状
目前相关的研究比较少，主要的研究方向集中在一下几个方向：

 - 开源软件（OSS）中非开发人员（缺陷检测、报告人员等）对整个软件开发的影响
 - OSS开发过程中maillist、BUGDB、gitlog等记录的开发过程的可信性
 - 版本控制系统（CVS）在OSS开发过程中的扮演的角色以及从中可以得到哪些有效信息
 - 从安卓历史版本的变迁中总结其开发倾向及特性变化的影响因素
 - 从大量的自然语言或数据中提取有效信息
 - OSS开发过程、规则、特点等的研究

# 动机及意义
##动机

 - 作为安卓的开源项目AOSP应用很广泛，基于其正在开发的第三方软件和ROM也很多
 - 安卓的内部开发过程是隐藏的，第三方开发者针对安卓feature的开发比较盲目
 - 缺少方向性造成了大量的无用功
 - OSS的隐藏开发过程跟开发过程中的maillist、BUGDB、gitlog有很大关联
 - OSS对email和CVS的依赖性很强
 - OSS开发中的Problem Reports（PRs）对其最终的发布版本有一定的指导意义

##意义

 - 预测AOSP未来的开发方向
 - 给第三方开发者提供一定的方向
 - 如有可能，抽象出OSS的开发模式，建立开发模型
 - 通过分析OSS开发的影响因素规避风险

# 主要观点、内容、重点和难点
##主要观点
 - AOSP增加的新特性一定可以从CVS开发日志中找到线索，且其最终是否会出现在下一个发布版本受PRs影响
 - 成功的OSS核心团队一般10-20人
 - OSS开发过程缺少面对面或者电话等传统交流方式，email和PRs中有大量的有效信息
 - 目前已有的数据挖掘算法已经支持我们从gitlog和maillist中获取我们需要的信息
 - AOSP开发模式已经成熟，因此我们可以从其之前的开发历史中得到验证
 - AOSP开发过程中的gitlog和maillist、BUGDB可以得到

##内容

 - 获取、清洗过滤、训练需要的数据
 - 根据AOSP的开发历史建立数学模型
 - 验证、修正建立的模型
 - 对未来的AOSP版本做出有根据的预测
 - 抽象出适用于一般的OSS的数学模型

##重点和难点
重点：
 
 - 获取到有用的规范化的原始数据
 - 根据数据和历史信息建立数学模型
 - 证实预测的可信性
难点：

 - 随着时间改变开发团队内部的规则改变可能使数据提取和最终的预测阶段更加复杂
 - maillist中的数据格式混乱，提取有效信息难度较大
 - 数学模型的选择上，太过特化的模型不足以体现OSS的共性，失去了预测意义；一般的模型可能不能很好服从AOSP的开发历史
 - 新特性的发布和旧特性的删减有太多不可控因素

# 研究基础

 - 伤检分流（Triage）对OSS的发展方向的影响正在得到重视
 - 开源开发模式研究资料比较多
 - 大量成功的数据挖掘算法可以学习
 - 个人有大数据处理方向的基础
 - 接下来将要调研的AOSP的开发历史

# 研究方法
总结了一下可能用到的研究方法如下：

 - 调查、描述：查阅文献、获取原始数据，根据初步处理的结果先进行直观判断，预估实现的可能性和程度
 - 建模、实验：进一步调研并确立合适的数学模型，从历史数据验证和修正
 - 比较研究：为防止特化，可与其他同时期并且类似的OSS进行对比研究，同时也增强了可信性

# 阶段任务规划

 - 一：数据集的采集和清洗、格式化
 - 二：分析数据，形成直观模型，寻找合适的数学模型并进行预测试（中期前）
 - 三：根据历史数据集和同类数据集最终确定回归模型，对AOSP的发展进行下一步预测，证实其可信性
 - 四：扩展预测模型，抽象出与具体的OSS无关的预测框架，如果不能分析其局限性和限制因素

# 成果
基本成果：

 - 一个可从开发过程分析开发中的重要事件，并预测AOSP feature的增删的工具
 - 一篇研究性论文

进阶成果：

 - 基本适用于典型OSS的预测框架

# 参考资料

------------------

- [Impact of Triage: a Study of Mozilla and Gnome](https://github.com/openthos/aosp-working-analysis/blob/master/papers/esem13-xie.pdf)
- [Two Case Studies of Open Source Software Development: Apache and Mozilla](https://github.com/openthos/aosp-working-analysis/blob/master/papers/mozilla.pdf)
- [Coding Together at Scale: GitHub as a Collaborative Social Network](https://github.com/openthos/aosp-working-analysis/blob/master/papers/icwsm14_github.pdf)

# 致谢

------------------

\centerline{\includegraphics[height=3in]{images/thanks.jpg}}
<p align="center"><img src="" height="90%" /></p>