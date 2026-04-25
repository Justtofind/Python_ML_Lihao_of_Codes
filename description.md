# Python_ML_Lihao_of_Codes 项目说明

## 1. 项目定位
本项目是机器学习与数据分析课程的 Jupyter Notebook 实践集合，核心主题为银行用户信用风险评估。当前文档以开源展示视角整理，强调项目结构、方法流程与可复用经验。

说明：本说明基于对 notebook 文件的静态读取整理，不包含代码执行结果。

## 2. 开源展示目标
- 展示一个完整的信用风险分析与建模流程。
- 提供可读性较强的 Notebook 学习路径，便于课程复盘与方法复用。
- 作为后续脚本化改造（模块化工程）的基础。

## 3. 主要文件与内容
- `PandasPrac.ipynb`
  - 以 pandas/可视化基础练习为主。
  - 内容包含：Series/DataFrame 基础属性、缺失值检查、ydata_profiling 使用、matplotlib 与 seaborn 绘图、类别编码（`map`/`replace`）、热力图、单变量线性回归推导与实现练习。
  - 同时包含部分报错处理与知识补充笔记（如 `SettingWithCopyWarning`、`map` 与 `replace` 对比）。

- `CreditOfBank.ipynb`
  - 银行信用风险评估的主项目 notebook。
  - 按章节组织：
    - 数据探索：多表结构预览、字段类型和缺失值统计。
    - 数据清洗与再探索：剔除缺失值/异常类别，处理 `Unnamed` 列，进行可视化分析。
    - 特征工程：
      - 对用户、银行流水、信用卡账单、逾期信息进行处理。
      - 构建交易频率、收入支出、还款率、信用使用率等特征。
      - 多表合并得到最终建模数据集。
    - 模型预测：
      - 线性回归（预测信用分数）。
      - 逻辑回归（预测是否逾期），含样本不平衡处理（`class_weight='balanced'`）与分类评估流程。

- `README.md`
  - 项目入口说明（本次已同步更新）。

## 4. 数据与目录约定
从 notebook 内容可见，代码默认使用以下目录约定：
- 原始数据目录：`OrigionalData`
  - 常见文件名：`userinfo.csv`、`bank.csv`、`bill.csv`、`overdue.csv`
- 输出数据目录：`OutputData_COB`
  - 典型输出：`final_modeling_dataset.csv`、`ohe_vector_mapping.csv`

运行 notebook 前需确保上述目录和数据文件路径一致。

## 5. 数据敏感性声明
本项目涉及银行业务相关数据字段，存在敏感信息风险。为保护隐私与满足合规要求，仓库默认不公开原始数据。

如需申请数据用于学习或研究，请通过以下方式联系：
- 邮件联系项目维护者
- 在仓库中留言（Issue）

## 6. 技术栈与依赖
项目中出现的主要 Python 库包括：
- 数据处理：`pandas`、`numpy`
- 可视化：`matplotlib`、`seaborn`
- 统计分析：`scipy`
- 建模：`scikit-learn`
- 报告分析：`ydata_profiling`
- 图形后端相关：`PyQt5`（用于部分环境下 matplotlib 交互显示）

## 7. 当前项目特点
- 以教学/练习场景为主，强调步骤可读性和过程记录。
- Notebook 中包含较多中文注释和解释，便于学习回溯。
- `CreditOfBank.ipynb` 已具备较完整的数据科学流程骨架，可继续扩展为标准化脚本工程（如将数据处理、特征工程、建模拆分成 `.py` 模块）。

## 8. 可改进建议
- 将 notebook 中稳定逻辑抽离为 Python 脚本，降低重复代码。
- 增加 `requirements.txt` 或 `pyproject.toml`，明确依赖版本。
- 在 README 中补充数据字典、字段含义、运行顺序与评估指标说明。
- 为关键数据处理函数添加最小化测试样例，提升可复现性。
