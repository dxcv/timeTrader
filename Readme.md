# 介绍
1. data提供统一的数据接口，供trader使用，可以切换数据源
整合多个数据源,约定数据格式，定义统一的接口方法，如果有新的数据源，处理成约定格式即可接入。
包括
(1)国信证券本地数据库
(2)tushare
2. trader负责策略回测与live交易
3. calendar定义交易日期
4. ./trader/strategy 存放所有交易策略
5. ./trader/order 存放所有下单类型
6. 易于使用的接口api，如下单、查询当前账户信息、回测结果保存等功能，提供统一的接口
7. signalSender负责发送交易信号到邮箱、微信等
8. optimizer负责对股票参数进行最优化


# 约定
## 命名规则
模块名: event,signalSender  
方法/函数: get_data  
类名: HistoryDataHandler  
对象: historyDataHandler  
常量: CONSTANT_VARIABLE  
变量: this_is_a_variable  

## 文档格式
'''
功能说明。

Parameter
---------
....

Return
---------
....

'''

## data数据结构

# 架构
采用事件驱动架构。

## 主目录
event：定义所有事件类型，可以根据需求定义不同的事件。  
data: 提供架构内所有数据支持。  
protfolio:账户  
protfolioHandler:账户维护  
executioner:撮合  
performance:评价  
riskManager:风控  
optimizer:最优化  
backtest:整合相关模块，实现回测功能  
setting:整合回测、live交易，提供封装后的顶层接口  

## 模块
### strategy
strategy:提供策略抽象，后续继承  
multiFactorStrategy:提供多因子策略抽象，后续策略继承  
sequentialFactorStrategy:提供序贯筛选策略抽象  

### calendar定义交易日期
calendar:提供交易日历  


### out
#### bt
保存回测结果  
#### live
保存live结果  

### log
日志。

# 计划
## 20170801
目前专注于日间回测部分，在完善日间回测后，再考虑分钟级回测。  
1. 完成基于国信证券本地数据库的data模块。
2. 完成基础基于后复权数据的回测程序，在该模式下仅支持按照金额下单。
3. 优化顶层api.
4. 完成基于不复权数据以及分红送股转增等数据的回测程序，在该模式下支持按照开盘价下单。
5. 完成基于tushare的实时行情接口，实现live交易功能

# 更新日志

