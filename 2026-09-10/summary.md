# Fast Multi-objective Evolutionary Algorithms to Approximate the Set of Optimal and Nearly Optimal Solutions

## 论文与作者信息

- **标题**：Fast Multi-objective Evolutionary Algorithms to Approximate the Set of Optimal and Nearly Optimal Solutions
- **作者**：Carlos Segura、Angel E. Rodriguez-Fernandez、Carlos Hernández、Oliver Schütze（墨西哥 CINVESTAV 团队）
- **期刊**：IEEE Transactions on Evolutionary Computation（Early Access）
- **上线日期**：2026 年 6 月 29 日
- **DOI**：10.1109/TEVC.2026.3707993
- **开放获取**：是（CC BY 4.0）
- **链接**：https://doi.org/10.1109/TEVC.2026.3707993

## 解决的问题模型

针对多目标优化问题（MOP），决策者关心的不仅是 Pareto 最优解，还包括"近最优解"集合 N(Q, ε)：即那些略逊于最优、但仍可作为备选或替代方案的解。该集合既包含完整的 Pareto 集，也包含非最优但"接近最优"的解，从而为决策者提供更大的候选空间。论文要解决的核心问题是：如何用进化算法得到该近最优解集合的有限规模近似。

## 相关工作

此前同一团队已提出"近最优解集"与 ε-局部最优解的概念，并给出寻找多目标优化问题近最优解集、ε-局部最优解的进化方法，以及基于 Newton / Hausdorff 距离逼近 Pareto 前沿等工作。但这些方法未给出针对近最优解集合的专门进化算法与有限规模近似策略；多模态多目标优化（MMOP）领域的现有工作也只关注完整 Pareto 集，忽略了近最优解。

## 所提方法

提出两阶段框架 **TPEA-N(Q, ε)**：

1. **第一阶段**：任选一个现有多目标进化算法（MOEA）获得 Pareto 集近似。
2. **第二阶段**：专注检测"非最优但近最优"的解，核心创新是采用**基于聚类的替换策略**（clustering-based replacement）。
3. 结合专用数据结构和**双指针技术**（two-pointer technique），为双目标与三目标问题设计了高效的近最优解检测算法。
4. 定义了比较各类近最优解近似方法的统一评测体系。

## 创新点

1. 首次提出面向"近最优解集合有限规模近似"的进化算法框架 TPEA-N(Q, ε)。
2. 聚类驱动的替换策略，使第二阶段的种群既能保持多样性又能覆盖近最优区域。
3. 双目标 / 三目标近最优解的高效检测算法（专用数据结构 + 双指针），降低计算开销。
4. 定义了近似近最优解集合的统一评测方法，并在多个基准问题上验证了有效性。