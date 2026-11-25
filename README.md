# Data Analysis Projects 数据分析项目集

信息与计算科学本科背景，目标方向：数据分析 / 统计建模。本仓库存放两个完整的分析项目，从数据清洗、探索分析到建模评估与业务结论。

## 项目一：电信客户流失预测（Telco Customer Churn）

- **业务问题**：哪些客户最可能流失？流失与什么因素有关？优先挽留谁？
- **数据**：Kaggle Telco Customer Churn，7043 名客户、21 个字段
- **方法**：pandas 清洗（处理 TotalCharges 空格导致的伪缺失）→ 探索分析（合约类型 / 在网时长 / 月费与流失的关系）→ 独热编码 + 分层抽样划分 → 逻辑回归 vs 随机森林对比 → 系数解释
- **评估**：Accuracy / Precision / Recall / F1 / ROC-AUC（流失客户仅占约 26%，不只看 Accuracy）
- **参考结果**：逻辑回归 ROC-AUC 0.836、Recall 0.575，略优于随机森林；最能降低流失风险的因素是在网时长与两年合约，最能拉高风险的是光纤服务
- **文件**：`project1-telco-churn/telco_churn_starter.ipynb`

## 项目二：淘宝用户行为分析（进行中）

- **数据**：阿里天池 UserBehavior（抽样约 100 万条，行为类型 pv / buy / cart / fav）
- **计划**：MySQL 存储与 SQL 取数 → Python 清洗 → 转化漏斗、留存分析、RFM 用户分层 → 可视化看板

## 技术栈

Python（pandas / numpy / scikit-learn / matplotlib / seaborn）、SQL（MySQL）、Jupyter Notebook
