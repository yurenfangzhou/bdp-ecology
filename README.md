# 数据平台介绍
 
# 1、数据平台总入口 
# https://github.com/wlhbdp/bdp-base

1.1 base-search
    
    技术：java, db，es
    搜索系统 
    统一搜索入口，搜索nosql db、es、db的数据   
    
1.2 base-common

    技术：java, db, spring cloud
    公共系统
    属于公共系统抽离，提供基础公共服务
  
1.3 base-task
    
    
    任务管理系统
    场景1：数据分析的task管理
    场景2：跑数据的task管理
    场景3：定时task管理

1.4 base-canal

    数据binlog采集
    配置mysql binlog, 实时采集到kakfa队列，然后基于kafka队列做spark计算
    
1.5 base-spider

    基础爬虫系统
    提供基础爬虫服务：扩展为gold爬虫，store爬虫

1.6 base-dts
    
    封装数据传输系统，基于数据进行互传，暴露接口服务给其他服务调用
    基于dataX封装数据传输系统
    
1.7 base-alarm

    基于grafana、promethus做一个运维告警系统
    运维告警系统
    

1.8 base-apm

    基于skywalking搭建分布式应用调用追踪系统，用于系统调优和排查调用错误
    Skywalking 应用分布式监控系统

1.9 base-config
    
    统一配置中心，从这里获取配置
    apollo 配置中心
    
1.10 base-report
    
    扩展为gold、store的报表系统
    报表系统

1.11 架构图

1.12 集群
    (集群维护)


# 2、金铺数据分析 https://github.com/wlhbdp/bdp-gold

2.1 个性化推荐系统 gold-recommender

2.2 日志收集系统 gold-logclient gold-logserver

2.3 人群画像系统 gold-profile

2.4 数据传输系统（删除)

2.5 实时计算系统

2.6 反作弊系统 gold-anti-fraud

2.7 多维度分析系统 gold-multianaly

2.8 商场系统 linjiashop
    
    埋点：
        前端埋点，后端起一个服务，实时消费kafka队列的消息，然后做流计算统计
        前端调用埋点api到后端上报到kafka数据一致，前端调用失败 后端上报失败，失败重传 数据格式校验
        android开发埋点：https://github.com/foolchen/AndroidTracker


# 3、店家数据分析 https://github.com/wlhbdp/bdp-store

3.1 智能营销推荐分析

3.2 消费者画像分析

3.3 店家信誉声量分析

3.4 topN商品分析

3.5 累计评论分析

3.6 宝贝详情分析

3.7 增量销售数据分析

3.8 活动效果分析

3.9 爬虫系统

3.10 店家Dashboard系统



# 4、运维管理平台 bdp-devops https://github.com/wlhbdp/bdp-devops

4.1 发布平台



# 5、数据中台 bdp-hub https://github.com/wlhbdp/bdp-datahub

5、数据中台

5.1 数据目录服务

5.2 数据分析服务

5.3 数据消费者图谱

5.4 数据开放服务

5.5 数据供需对接

5.6 数据治理服务

5.7 数据存储

    大数据存储

    分布式数据库

    内存数据库

    文档数据库

    并行数据仓库

    关系型数据库

5.8 主题库服务




# 6 应用中台 https://github.com/wlhbdp/bdp-apphub

6.1 应用开放服务

6.2 统一身份认证

6.3 统一消息推送

6.4 消息队列服务

6.5 表单引擎

6.6 统一支付服务

6.7 统一用户中心

6.8 微服务

6.9 云容器平台
    
    包含服务管理（查看docker容器配置，添加容器实例，授权记录，操作记录，
    历史版本回溯，k8s启停服务，操作记录，对比yaml配置，更新服务）
    任务管理、配置管理、镜像构建（包括环境变量和参数配置）、应用日志


# 7 知识探索 https://github.com/wlhbdp/bdp-explore

7.1 应用服务

7.2 运营服务

7.3 流程编排

7.4 模版服务

7.5 图像服务

7.6 语义服务

7.7 语音服务

7.8 模型服务

7.9 算法管理

7.10 适配服务


# 8 安全管理 https://github.com/wlhbdp/bdp-security

8.1 安全专家服务

8.2 数据脱敏

8.3 数据审计

8.4 安全接入

8.5 安全核查

8.6 应用安全

8.7 业务安全

8.8 日志审计

8.9 安全监测


# 9、客户数据中台 https://github.com/wlhbdp/bdp-cdp
 
    全面融合线下线上数据的客户数据中台

9.1 数据采集
    
    客户触点： 全终端、全渠道、全类型
    
    数据类型：线下/线上、业务数据、客户属性、三方数据

9.2 数据融合

    超级ID融合
    
    多数仓调度
    
    自动化ETL
    
    智能匹配
    
        
9.3 标签管理

    基础标签
    
    智能标签
    
    自助标签
    
    行为创建
    
    ID上传
    
    组合运算
    

9.4 客户洞察

    客户群体画像
    
    一方DMP
    
    个体洞察
    
    场景标签分析
    
    人群管理
    
    
# 10 业务中台 https://github.com/wlhbdp/bdp-businesshub

    核心优势
    
    全渠道、全链路业务协同
    
    从加工生产到销售订单，打造拉动式“柔性”供应链。在加工环节、采购流程、库存管理、物流运输、财务管控等各业务线形成数据通道。通过可视化、规范化的管理流程，全面提升企业效率。
    
    AI人工智能辅助决策
    
    借力AI、通过模型与算法，进行预测与模拟，辅助企业制定销售目标、明确营销方向、优化品类格局、改善仓储布局，提升企业价值。
    
    多平台无缝连接
    
    支持市场主流社交平台、第三方电商平台、物流平台、仓储平台、财务等系统的无缝对接，快速响应企业市场需求。
    
    场景解释
    
    客户痛点
    
    √ 供应链弹性低、效率低、成本高。
    
    √ 仓库周转慢、库存积压重。
    
    √ 企业IT孤岛、协作慢、运营效率低。
    
    √ 营销成本高、命中率底。
    
    
    √ 业务探索和创新难，经营决策难。
    
    解决方案
    
    业务中台 + 数据中台 
    
    业务中台——支持多系统、多平台业务数据接入，打通各业务线壁垒、形成全方位、可视化业务中心，快速响应灵活多变的前端业务。
    
    数据中台——沉淀业务数据、利用AI进行数据挖掘与分析，形成多层面、多角度的数据监控和分析，为业务的决策和自动化服务等企业需求提供科学依据。 
    
    实现价值
    
    √ 打造柔性供应链，实现拉动式生产。
    
    √ 打通信息壁垒，协同企业各部门高效运转。
    
    √ 以顾客为中心，个性化精准营销。
    
    √ 以数据为依托，辅助企业智能决策。
    
    √ 协助企业快速响应并融入创新市场。
    
    
 有开源的一个框架BigDataPlatform
 我要么设计100个系统的架构图
 如果让我先画最小可用的整个链路系统，然后在衍生迭代，似乎是可行的
 但是我很多不会，这个过程我还需要补全学习一些能力
 问题来了，我是全部补全能力后，再进行开发，还是基于现在的能力做一些事情
   目前欠缺一些能力，需要补全学习
   创业方向能力、前端开发能力、dart移动开发能力、flink开发能力，产品经理能力，项目经理能力，开发主管，架构师，算法能力，springcloud能力, 微服务能力，k8s能力，运维能力，分布式系统能力
 架构是很重要的，需要技术超群，然后动手能力超强
 
 
 实体店铺数据分析、先扎实各项技术和各项能力
