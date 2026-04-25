# Python_ML_Lihao_of_Codes

本仓库是一个面向学习与展示的机器学习实践项目，主题为银行信用风险评估。项目以 Notebook 形式完整记录了从数据探索到模型预测的分析流程。

## 项目亮点
- 端到端流程：数据探索 -> 数据清洗 -> 特征工程 -> 模型训练与评估。
- 双模型实践：线性回归（预测分数）与逻辑回归（预测是否逾期）。
- 可视化分析：包含分布图、箱线图、相关性热力图、ROC 曲线等。
- 教学友好：Notebook 中保留了较完整的步骤解释与问题修正过程。

## 项目说明
详细说明见 [description.md](description.md)

核心内容概览：
- `PandasPrac.ipynb`：pandas 基础、缺失值检查、可视化练习、编码方法与统计学习补充。
- `CreditOfBank.ipynb`：信用风险评估主流程（探索、清洗、特征构建、线性回归、逻辑回归）。
- 数据目录约定：`OrigionalData`（输入）与 `OutputData_COB`（输出）。

## 数据声明（重要）
项目涉及银行业务相关数据字段，可能包含敏感信息。

出于数据合规与隐私保护考虑，仓库不直接公开原始数据文件。如需获取数据用于学习或研究，请通过以下方式联系：
- 邮件联系项目维护者
- 在仓库中留言（如 Issue）

## 使用说明
1. 准备 Python 环境并安装 notebook 中使用到的依赖（如 pandas、numpy、matplotlib、seaborn、scikit-learn、scipy、ydata_profiling、PyQt5）。
2. 按 notebook 中的路径约定准备数据文件：`userinfo.csv`、`bank.csv`、`bill.csv`、`overdue.csv`。
3. 建议先阅读 [description.md](description.md)，再按章节顺序执行 notebook。

## Git 说明
- 仓库以 `.ipynb` 学习记录为主。
- 大文件（超过 Git 平台限制）需使用大文件管理方案（如 Git LFS）或避免直接纳入仓库。
