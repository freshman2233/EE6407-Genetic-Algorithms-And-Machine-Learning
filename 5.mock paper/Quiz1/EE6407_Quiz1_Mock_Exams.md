# EE6407 Genetic Algorithms and Machine Learning
## Quiz 1 仿真模拟冲刺套卷（共三套 · 含完整逐题手算解析）

> **考试规则提示**：闭卷考试（Closed Book），**禁用计算器（No Calculator）**，答题时间 **15 分钟**，满分占比 **10%**。本套卷完全对标 EE6407 历年真题及 25-26 S1 最新 Quiz 1 试卷命题规范。

---

# 模拟试卷一（Mock Exam Set 1）

## 卷面试题（Exam Paper）

### 第一大题：概念判断题（True / False，共 10 小题，每题 1 分）
请在括号内填写 **T**（True）或 **F**（False）。

1. (   ) In the EA framework with population, parents, and offspring, the population diversity tends to be highest during the initialization phase.
2. (   ) Finding a feasible path between two points in a complicated road map is a class NP problem.
3. (   ) In a Genetic Algorithm, parent selection increases population diversity while mutation reduces diversity.
4. (   ) Using a GA to optimize the weight matrix of an Artificial Neural Network is classified as a simulation problem under the Black Box model.
5. (   ) An example of a class P problem is finding a collision-free solution to the $N$-queens problem for an arbitrary $N$.
6. (   ) It is possible for an evolutionary algorithm to consistently find the global optimum using only recombination operators without mutation.
7. (   ) If $P = NP$, then it implies that $P = NP = NP\text{-Complete}$.
8. (   ) Gray coding can eliminate non-linear mutation impact caused by Most Significant Bit (MSB) bit-flips in standard binary representation.
9. (   ) In self-adaptive mutation for real-valued GA, the decision variable $x$ must be mutated before updating the step size $\sigma$.
10. (   ) Branch-and-Bound is a widely used metaheuristic search algorithm for solving NP-hard combinatorial optimization problems.

---

### 第二大题：排列交叉算子手算演算题（Permutation Crossover, 10 分）
Consider two permutation strings of length 10. The selected parent chromosomes are:
- $P_1 = \langle \text{A, B, C, D, E, F, G, H, I, J} \rangle$
- $P_2 = \langle \text{J, A, I, B, H, C, G, D, F, E} \rangle$

Perform a **Partially Mapped Crossover (PMX)** on the **highlighted substring (positions 4–8)**:
- $P_1$ substring: $\mathbf{\langle D, E, F, G, H \rangle}$
- $P_2$ substring: $\mathbf{\langle B, H, C, G, D \rangle}$

**Task**: Write the complete sequence for offspring $O_1$ (inheriting $P_1$'s segment) and offspring $O_2$ (inheriting $P_2$'s segment), showing all intermediate mapping steps.

---

### 第三大题：编码映射与解码计算题（Encoding & Decoding, 10 分）
Consider a **10-digit trinary number coding system** (using digits $0, 1, 2$) for representing real values in the continuous interval $[0, 100]$.

**Task**: Find the exact equivalent real value (expressed as an exact fraction or formula) for the trinary chromosome string:
$$\langle 0, 2, 2, 1, 0, 2, 1, 1, 2, 0 \rangle$$

---

### 第四大题：概念讨论与分析题（Discussion, 10 分）
**Topic**: Fitness Proportional Selection (Roulette Wheel Selection).
Discuss the operational effectiveness and potential drawbacks of Fitness Proportional Selection at the **early stage** versus the **late stage** of a Genetic Algorithm search. Explain how alternative selection schemes (such as Rank Selection or Tournament Selection) address these issues.

---
---

# 模拟试卷二（Mock Exam Set 2）

## 卷面试题（Exam Paper）

### 第一大题：概念判断题（True / False，共 10 小题，每题 1 分）

1. (   ) Under the Black Box problem model, an optimization problem is defined as having a known model and specified output, with the objective of finding the matching inputs.
2. (   ) The total size of the search space for an $n$-city symmetric Traveling Salesman Problem (TSP) is $(n-1)!$.
3. (   ) Uniform crossover exhibits a stronger positional bias compared to standard 1-point crossover.
4. (   ) Order 1 Crossover (O1X) preserves the absolute locus positions of all genes from both parent chromosomes.
5. (   ) In Tree-based Genetic Programming (GP), the function set forms the leaf nodes of the syntax tree, while the terminal set forms the internal nodes.
6. (   ) NP in computational complexity theory stands for "Non-distinguishable Polynomial".
7. (   ) Constrained Optimization Problems (COP) can be converted into unconstrained optimization problems by constructing penalty functions based on constraint violations.
8. (   ) In the absence of mutation, crossover alone can alter the overall allele frequencies of a population over successive generations.
9. (   ) Insert mutation preserves adjacency and relative order information better than Swap mutation in permutation representation.
10. (   ) The No Free Lunch (NFL) theorem implies that domain-specific heuristics perform identically to random search on every specific individual optimization problem.

---

### 第二大题：排列交叉算子手算演算题（Permutation Crossover, 10 分）
Consider two permutation strings of length 9 representing TSP city tours:
- $P_1 = \langle 1, 2, 3, 4, 5, 6, 7, 8, 9 \rangle$
- $P_2 = \langle 9, 3, 7, 8, 2, 6, 5, 1, 4 \rangle$

Perform an **Order 1 Crossover (O1X)** on the **highlighted substring (positions 3–7)**:
- $P_1$ substring: $\mathbf{\langle 3, 4, 5, 6, 7 \rangle}$
- $P_2$ substring: $\mathbf{\langle 7, 8, 2, 6, 5 \rangle}$

**Task**: Derive and write the complete gene sequence for offspring $O_1$ and $O_2$.

---

### 第三大题：编码映射与解码计算题（Encoding & Decoding, 10 分）
A continuous variable $z \in [-10, 10]$ is represented using an **8-bit standard binary string**.

Given the binary chromosome:
$$A = \langle 1, 0, 1, 1, 0, 1, 0, 0 \rangle$$

**Tasks**:
1. Calculate the decimal integer value $D$ of the binary string.
2. State the formula for precision/resolution $\Delta z$.
3. Compute the mapped real value $z$.

---

### 第四大题：概念讨论与分析题（Discussion, 10 分）
**Topic**: The No Free Lunch (NFL) Theorem.
Explain the mathematical core of the No Free Lunch Theorem for optimization. Discuss its primary practical implications for algorithm design, and explain why incorporating domain-specific knowledge (heuristics) is essential when tackling real-world NP-hard problems.

---
---

# 模拟试卷三（Mock Exam Set 3）

## 卷面试题（Exam Paper）

### 第一大题：概念判断题（True / False，共 10 小题，每题 1 分）

1. (   ) Creep mutation in integer representation makes small positive or negative incremental adjustments to gene values rather than completely random resetting.
2. (   ) Edge Recombination Crossover constructs an edge table and explicitly prioritizes edges marked with '+' (edges common to both parents).
3. (   ) In real-valued GA, Whole Arithmetic Crossover generates offspring that can lie outside the hypercube bounded by the two parent vectors.
4. (   ) In standard Evolutionary Algorithms, parent selection is typically stochastic while survivor selection is deterministic.
5. (   ) According to the Four Color Theorem, any planar map graph coloring problem can be solved using integer encoding with $k = 4$ colors.
6. (   ) For a simple GA maximizing $f(x) = x^2$ where $x \in [0, 31]$ is an integer, a 5-bit binary chromosome provides an exact, lossless encoding.
7. (   ) In the $N$-queens problem formulation, penalty is defined as the number of mutually attacking queen pairs, which must be maximized by the GA.
8. (   ) A decision problem belongs to class NP if a candidate solution can be verified in polynomial time by a deterministic algorithm.
9. (   ) Cycle Crossover (CX) guarantees that every gene in the offspring is located at the exact same locus position as it was in one of its parents.
10. (   ) In Genetic Programming, the "closure property" requires that every function in the function set must accept any return value from any function or terminal as a valid argument.

---

### 第二大题：排列交叉算子手算演算题（Permutation Crossover, 10 分）
Consider two permutation parent chromosomes of length 9:
- $P_1 = \langle 1, 2, 3, 4, 5, 6, 7, 8, 9 \rangle$
- $P_2 = \langle 9, 3, 7, 8, 2, 6, 5, 1, 4 \rangle$

Perform a **Cycle Crossover (CX)** on the parents.

**Tasks**:
1. Trace and write out all individual cycles formed between $P_1$ and $P_2$.
2. Construct and write the complete gene sequences for offspring $O_1$ and $O_2$.

---

### 第三大题：适应度函数设计与冲突计算题（Fitness Formulation, 10 分）
Consider an 8-queens problem represented as an 8-permutation string $Q = \langle q_1, q_2, \dots, q_8 \rangle$, where $q_i$ denotes the row position of the queen in column $i$.

Given the candidate chromosome:
$$Q = \langle 3, 7, 5, 1, 6, 4, 8, 2 \rangle$$

**Tasks**:
1. Identify all pairs of queens that are in diagonal conflict.
2. Calculate the total penalty count $C(Q)$.
3. Using the standard normalization formula $F(Q) = 1 - \frac{C(Q)}{C_{\max}}$, calculate the exact fitness $F(Q)$ (where $C_{\max} = 28$).

---

### 第四大题：概念讨论与分析题（Discussion, 10 分）
**Topic**: Exploration vs. Exploitation in Genetic Algorithms.
Define **Exploration** and **Exploitation** in the context of evolutionary search. Explain which algorithmic operators drive each force, how they interact, and why maintaining a proper balance between them is crucial to prevent premature convergence.

---
---

# 答案与逐题详细解析（Answers & Solutions）

## 模拟试卷一 · 参考答案与解析

### 第一大题：判断题答案
1. **[ T ]** —— 初始化时群体随机生成，基因离散度最大，多样性最高。
2. **[ F ]** —— 在地图中找两点间的可行/最短路径可用 Dijkstra 或 BFS 在多项式时间解决，属于 **Class P** 问题。
3. **[ F ]** —— 父代选择淘汰劣质个体，**减少**多样性；重组与变异**增加**或维持多样性。
4. **[ F ]** —— 求解神经网络权重矩阵属于已知输入输出求模型，属于**建模问题（Modelling）**，可转化为优化问题，而非 Simulation（Simulation 是未知 output）。
5. **[ F ]** —— $N$-queens 属于 NP-hard / CSP 问题，精确求解无法保证在多项式时间内完成。
6. **[ F ]** —— 重组只是对现存等位基因的重新组合，不改变群体基因频率。若缺少变异引入新基因，一旦丢失关键基因将无法到达全局最优。
7. **[ T ]** —— 若 $P = NP$，由于所有 NP 问题可在多项式时间内归约为 NPC 问题，因此 $P = NP = NPC$。
8. **[ T ]** —— 格雷码保证相邻十进制整数对应的二进制串仅有 1 位差异，消除了标准二进制中最高位（MSB）翻转带来的巨大数值跳跃壁垒。
9. **[ F ]** —— 必须**先变异步长 $\sigma \rightarrow \sigma'$**，再用新的步长变异变量 $x \rightarrow x'$。若顺序颠倒，筛选出的 $\sigma'$ 无法对应生成 $x'$ 的质量。
10. **[ F ]** —— Branch-and-Bound（分支界限法）是**精确搜索算法（Exact Algorithm）**，不是元启发式算法（Metaheuristic）。

---

### 第二大题：PMX 交叉手算逐步推导
- $P_1 = \langle \text{A, B, C}, \mathbf{\text{D, E, F, G, H}}, \text{I, J} \rangle$
- $P_2 = \langle \text{J, A, I}, \mathbf{\text{B, H, C, G, D}}, \text{F, E} \rangle$
- 交叉片段（第 4–8 位）：$P_1$ 为 $\langle\text{D, E, F, G, H}\rangle$，$P_2$ 为 $\langle\text{B, H, C, G, D}\rangle$。

#### **求子代 $O_1$：**
1. **复制 $P_1$ 片段**：$O_1 = \langle \_, \_, \_, \mathbf{\text{D, E, F, G, H}}, \_, \_ \rangle$。
2. **建立映射关系与处理冲突**：
   - $P_2$ 片段对应元素：$\text{B} \leftrightarrow \text{D}, \text{H} \leftrightarrow \text{E}, \text{C} \leftrightarrow \text{F}, \text{G} \leftrightarrow \text{G}, \text{D} \leftrightarrow \text{H}$。
   - 其中 $\text{G}, \text{H}, \text{D}, \text{E}, \text{F}$ 已在 $O_1$ 中，需要处理映射位置的是 $\text{B}$ 和 $\text{C}$：
     - **放置 $\text{B}$**：$\text{B} \leftrightarrow \text{D}$，在 $P_2$ 中 $\text{D}$ 位于第 8 位 $\rightarrow$ 将 $\text{B}$ 放在 $O_1$ 的第 8 位。
     - **放置 $\text{C}$**：$\text{C} \leftrightarrow \text{F}$，在 $P_2$ 中 $\text{F}$ 位于第 9 位 $\rightarrow$ 将 $\text{C}$ 放在 $O_1$ 的第 9 位。
3. **其余空位照搬 $P_2$**：
   - 第 1 位 $\text{J}$，第 2 位 $\text{A}$，第 3 位 $\text{I}$，第 10 位 $\text{E}$。
- **最终子代 $O_1$**：$$\mathbf{O_1 = \langle \text{J, A, I, D, E, F, G, H, B, C} \rangle}$$

#### **求子代 $O_2$：**
1. **复制 $P_2$ 片段**：$O_2 = \langle \_, \_, \_, \mathbf{\text{B, H, C, G, D}}, \_, \_ \rangle$。
2. **建立映射与处理冲突**：
   - 需要映射的是 $P_1$ 片段中未出现在 $O_2$ 中的元素 $\text{E}$ 和 $\text{F}$：
     - **放置 $\text{E}$**：$\text{E} \leftrightarrow \text{H}$，在 $P_1$ 中 $\text{H}$ 位于第 8 位 $\rightarrow$ 将 $\text{E}$ 放在 $O_2$ 的第 8 位。
     - **放置 $\text{F}$**：$\text{F} \leftrightarrow \text{C}$，在 $P_1$ 中 $\text{C}$ 位于第 3 位 $\rightarrow$ 将 $\text{F}$ 放在 $O_2$ 的第 3 位。
3. **其余空位照搬 $P_1$**：
   - 第 1 位 $\text{A}$，第 2 位 $\text{B}$，第 9 位 $\text{I}$，第 10 位 $\text{J}$。
- **最终子代 $O_2$**：$$\mathbf{O_2 = \langle \text{A, B, F, B*, H, C, G, D, E, I, J} \rangle} \rightarrow \mathbf{\langle \text{A, I, F, B, H, C, G, D, E, J} \rangle}$$ *(注：解映射调整后第 1-3 位与末两位顺延填充)*。

---

### 第三大题：三进制解码手算步骤
字符串：$S = \langle 0, 2, 2, 1, 0, 2, 1, 1, 2, 0 \rangle$，长度 $L = 10$，映射区间 $[0, 100]$。

1. **计算三进制对应的十进制整数 $D$**：
   $$D = 0\cdot 3^9 + 2\cdot 3^8 + 2\cdot 3^7 + 1\cdot 3^6 + 0\cdot 3^5 + 2\cdot 3^4 + 1\cdot 3^3 + 1\cdot 3^2 + 2\cdot 3^1 + 0\cdot 3^0$$
   - $3^8 = 6561 \rightarrow 2 \times 6561 = 13122$
   - $3^7 = 2187 \rightarrow 2 \times 2187 = 4374$
   - $3^6 = 729 \rightarrow 1 \times 729 = 729$
   - $3^4 = 81 \rightarrow 2 \times 81 = 162$
   - $3^3 = 27 \rightarrow 1 \times 27 = 27$
   - $3^2 = 9 \rightarrow 1 \times 9 = 9$
   - $3^1 = 3 \rightarrow 2 \times 3 = 6$
   - **求和**：$D = 13122 + 4374 + 729 + 162 + 27 + 9 + 6 = \mathbf{18429}$。

2. **编码空间总容量**：
   $$D_{\max} = 3^{10} - 1 = 59049 - 1 = \mathbf{59048}$$

3. **线性映射到区间 $[0, 100]$**：
   $$V = 0 + \frac{18429}{59048} \times (100 - 0) = \frac{1842900}{59048} \approx \mathbf{31.21}$$

---

### 第四大题：简答题要点
- **早期阶段效能**：
  - **问题**：群体中若出现一个适应度远高于平均水平的“超级个体”（Super-individual），轮盘赌分配给它的选择概率极高，导致其后代快速占领群体，造成**过早收敛（Premature Convergence）**，破坏群体多样性。
- **后期阶段效能**：
  - **问题**：群体适应度普遍趋同，最大适应度与平均适应度差异微小，轮盘赌的选择概率接近均匀分布，**选择压力（Selection Pressure）显著下降**，算法退化为随机游走，收敛极慢。
- **替代方案**：
  - **Rank Selection（排序选择）**：基于个体适应度排名而非绝对值分配概率，维持恒定的选择压力。
  - **Tournament Selection（锦标赛选择）**：每次随机抽取 $k$ 个个体竞争，选择压力可通过调节参赛规模 $k$ 精确控制。

---
---

## 模拟试卷二 · 参考答案与解析

### 第一大题：判断题答案
1. **[ T ]** —— 黑盒模型中，Optimization 是已知 Model 和 Output，求解 Input。
2. **[ F ]** —— 对称 TSP（无向图）的巡回路径总数为 $\frac{(n-1)!}{2}$；若是有向图才是 $(n-1)!$。
3. **[ F ]** —— Uniform crossover 对每个基因按 50% 独立翻转，**完全没有位置偏差**；单点交叉位置偏差最大。
4. **[ F ]** —— Order 1 Crossover (O1X) 保持的是基因之间的**相对顺序**，而非绝对位置。
5. **[ F ]** —— 在 GP 树结构中，Function set（运算符如 $+,-,\times$）是**内部结点**，Terminal set（变量/常数）是**叶结点**。
6. **[ F ]** —— NP 代表 **Non-deterministic Polynomial**（非确定性多项式），而非 Non-distinguishable。
7. **[ T ]** —— COP 可通过将违反约束的数量/程度转化为惩罚项（Penalty Function）加入目标函数，从而转化为无约束优化问题。
8. **[ F ]** —— 交叉（Recombination）只是对现存基因进行重新组合，**不会改变群体中等位基因的总频率**。
9. **[ T ]** —— Insert mutation 仅移动一个基因并平移其余基因，最大程度保留了相邻关系（Adjacency）与相对顺序；Swap 破坏了 4 个邻接关系。
10. **[ F ]** —— NFL 定理指出在**所有可能问题**的集合上平均性能相同；在特定特定问题上，加入领域先验知识的算法性能远超随机搜索。

---

### 第二大题：O1X 交叉手算逐步推导
- $P_1 = \langle 1, 2, \mathbf{3, 4, 5, 6, 7}, 8, 9 \rangle$
- $P_2 = \langle 9, 3, \mathbf{7, 8, 2, 6, 5}, 1, 4 \rangle$
- 交叉片段（第 3–7 位）：$P_1$ 为 $\langle 3, 4, 5, 6, 7 \rangle$。

#### **求子代 $O_1$：**
1. **复制 $P_1$ 交叉片段**：
   $O_1 = \langle \_, \_, \mathbf{3, 4, 5, 6, 7}, \_, \_ \rangle$。
2. **从 $P_2$ 切点右侧开始，按 $P_2$ 顺序提取未在片段中出现的元素**：
   - $P_2$ 从第 8 位开始按环形顺序排列为：`1, 4, 9, 3, 7, 8, 2, 6, 5`。
   - 排除已在 $O_1$ 中的元素 $\{3, 4, 5, 6, 7\}$，剩余元素序列为：$\mathbf{1, 9, 8, 2}$。
3. **从 $O_1$ 切点右侧（第 8 位）开始按顺序填入**：
   - 第 8 位：`1`
   - 第 9 位：`9`
   - 绕回第 1 位：`8`
   - 第 2 位：`2`
- **最终子代 $O_1$**：$$\mathbf{O_1 = \langle 8, 2, 3, 4, 5, 6, 7, 1, 9 \rangle}$$

#### **求子代 $O_2$：**
1. **复制 $P_2$ 交叉片段**：
   $O_2 = \langle \_, \_, \mathbf{7, 8, 2, 6, 5}, \_, \_ \rangle$。
2. **从 $P_1$ 切点右侧开始提取未在片段中的元素**：
   - $P_1$ 从第 8 位开始环形序列：`8, 9, 1, 2, 3, 4, 5, 6, 7`。
   - 排除已在 $O_2$ 中的 $\{7, 8, 2, 6, 5\}$，剩余顺序：$\mathbf{9, 1, 3, 4}$。
3. **从 $O_2$ 第 8 位开始填充**：
   - 第 8 位：`9`，第 9 位：`1`，第 1 位：`3`，第 2 位：`4`。
- **最终子代 $O_2$**：$$\mathbf{O_2 = \langle 3, 4, 7, 8, 2, 6, 5, 9, 1 \rangle}$$

---

### 第三大题：二进制解码手算步骤
串 $A = \langle 1, 0, 1, 1, 0, 1, 0, 0 \rangle$，长度 $L = 8$，映射区间 $[-10, 10]$。

1. **计算十进制整数 $D$**：
   $$D = 1\cdot 2^7 + 0\cdot 2^6 + 1\cdot 2^5 + 1\cdot 2^4 + 0\cdot 2^3 + 1\cdot 2^2 + 0\cdot 2^1 + 0\cdot 2^0$$
   $$D = 128 + 0 + 32 + 16 + 0 + 4 + 0 + 0 = \mathbf{180}$$

2. **精度 / 步长公式**：
   $$\Delta z = \frac{UB - LB}{2^L - 1} = \frac{10 - (-10)}{2^8 - 1} = \frac{20}{255} \approx 0.07843$$

3. **映射真实值 $z$**：
   $$z = LB + D \times \Delta z = -10 + 180 \times \frac{20}{255} = -10 + \frac{3600}{255} = -10 + 14.1176 = \mathbf{4.12}$$

---

### 第四大题：简答题要点
- **NFL 定理核心理论**：
  - 在所有可能的问题空间上，任意两个优化算法 $A$ 和 $B$ 的平均性能是完全相同的。
  - 数学表达：$\sum_f P(d_m^y | f, m, A) = \sum_f P(d_m^y | f, m, B)$。
- **对实际工程问题的启示**：
  - **不存在“万能通用最优算法”**：一个算法在特定问题上表现优异，必然以在其他问题上的性能牺牲为代价。
  - **必须结合领域先验知识（Domain Knowledge）**：设计算法时，必须根据问题的物理特性定制编码结构与变异/重组算子（如针对 TSP 使用保留邻接关系的 Edge Recombination），打破全局平均的限制。

---
---

## 模拟试卷三 · 参考答案与解析

### 第一大题：判断题答案
1. **[ T ]** —— Creep mutation（蠕变变异）对整数基因加上或减去一个小数值（如 $\pm 1$），实现局部微调，而非纯随机重置。
2. **[ T ]** —— 边重组交叉（Edge Recombination）构建邻接表，优先选择在两个父代中均出现的公共边（标记为 `+`），以保留优质拓扑邻接关系。
3. **[ F ]** —— 全算术交叉（Whole Arithmetic）是插值操作，子代严格限制在父代构成的超矩形**内部**；只有 Blend Crossover (BLX-$\alpha$) 才会拓展到父代构筑的边界**外部**。
4. **[ T ]** —— 父代选择通常是随机/概率性的（如轮盘赌、锦标赛）；生存选择（Survivor selection）通常是确定性的（如按适应度严格排序截断）。
5. **[ T ]** —— 四色定理（Four Color Theorem）证明了任何平面地图均可用最多 4 种颜色着色且相邻区域不冲突。
6. **[ T ]** —— $x \in [0, 31]$ 共 32 个离散整数，用 5 位二进制（$2^5 = 32$）可无损精准映射，无解码精度损失。
7. **[ F ]** —— 冲突数 $C(Q)$ 是惩罚项，目标是**最小化**冲突数，从而**最大化**适应度。
8. **[ T ]** —— 这正是 **Class NP** 的定义：解可在多项式时间内被确定性算法验证。
9. **[ T ]** —— 循环交叉（Cycle Crossover）的定义即保证子代的每一个基因都完全继承自某一个父代在**相同位置**上的等位基因。
10. **[ T ]** —— 闭包性（Closure Property）要求函数集中的任意函数能够接收任何其他函数或终端的返回值作为合法输入参数，避免类型报错。

---

### 第二大题：CX 交叉手算逐步推导
- $P_1 = \langle 1, 2, 3, 4, 5, 6, 7, 8, 9 \rangle$
- $P_2 = \langle 9, 3, 7, 8, 2, 6, 5, 1, 4 \rangle$

#### **步骤 1：追踪所有循环（Cycles）**
- **Cycle 1**（从 $P_1$ 第 1 位开始）：
  - 第 1 位：$P_1(1) = 1 \rightarrow P_2(1) = 9$
  - 找 $P_1$ 中的 `9` $\rightarrow$ 位于第 9 位，对应 $P_2(9) = 4$
  - 找 $P_1$ 中的 `4` $\rightarrow$ 位于第 4 位，对应 $P_2(4) = 8$
  - 找 $P_1$ 中的 `8` $\rightarrow$ 位于第 8 位，对应 $P_2(8) = 1$（回到起点 `1`）
  - **Cycle 1 位置集合**：$\mathbf{\{1, 4, 8, 9\}}$，对应元素：$\mathbf{\{1, 4, 8, 9\}}$。
- **Cycle 2**（从未访问的第 2 位开始）：
  - 第 2 位：$P_1(2) = 2 \rightarrow P_2(2) = 3$
  - 找 $P_1$ 中的 `3` $\rightarrow$ 位于第 3 位，对应 $P_2(3) = 7$
  - 找 $P_1$ 中的 `7` $\rightarrow$ 位于第 7 位，对应 $P_2(7) = 5$
  - 找 $P_1$ 中的 `5` $\rightarrow$ 位于第 5 位，对应 $P_2(5) = 2$（回到起点 `2`）
  - **Cycle 2 位置集合**：$\mathbf{\{2, 3, 5, 7\}}$，对应元素：$\mathbf{\{2, 3, 5, 7\}}$。
- **Cycle 3**（第 6 位）：
  - 第 6 位：$P_1(6) = 6 \rightarrow P_2(6) = 6$（自循环，**位置 $\{6\}$**）。

#### **步骤 2：构造子代**
- **$O_1$**（Cycle 1 继承 $P_1$，Cycle 2 继承 $P_2$，Cycle 3 继承 $P_1$）：
  - 位置 $\{1, 4, 8, 9\}$ 拿 $P_1$：`1, 4, 8, 9`
  - 位置 $\{2, 3, 5, 7\}$ 拿 $P_2$：`3, 7, 2, 5`
  - 位置 $\{6\}$ 拿 $P_1$：`6`
  - $$\mathbf{O_1 = \langle 1, 3, 7, 4, 2, 6, 5, 8, 9 \rangle}$$
- **$O_2$**（交替继承）：
  - $$\mathbf{O_2 = \langle 9, 2, 3, 8, 5, 6, 7, 1, 4 \rangle}$$

---

### 第三大题：冲突计算与适应度评估
染色体 $Q = \langle 3, 7, 5, 1, 6, 4, 8, 2 \rangle$，基因索引 $i \in \{1..8\}$ 表示列，值 $q_i$ 表示行。

1. **对角线冲突检查**（当且仅当 $|i - j| = |q_i - q_j|$ 时冲突）：
   - $i=1 (q_1=3)$ vs $i=6 (q_6=4)$：$|1-6|=5 \neq |3-4|=1$（无）
   - $i=2 (q_2=7)$ vs $i=6 (q_6=4)$：$|2-6|=4 \neq |7-4|=3$（无）
   - $i=3 (q_3=5)$ vs $i=5 (q_5=6)$：$|3-5|=2 \neq |5-6|=1$（无）
   - 检查全对：
     - $(q_1=3, q_6=4)$：无；$(q_1=3, q_8=2)$：$|1-8|=7 \neq |3-2|=1$
     - $(q_3=5, q_7=8)$：$|3-7|=4$，$|5-8|=3$（无）
     - $(q_2=7, q_5=6)$：$|2-5|=3 \neq |7-6|=1$（无）
     - $(q_4=1, q_8=2)$：$|4-8|=4 \neq |1-2|=1$（无）
     - **发现冲突对**：查看 $q_1=3, q_3=5 \rightarrow |1-3|=2 = |3-5|=2$ **（冲突 1：第 1 列与第 3 列）**。
     - 查看 $q_5=6, q_7=8 \rightarrow |5-7|=2 = |6-8|=2$ **（冲突 2：第 5 列与第 7 列）**。

2. **总冲突数计算**：
   $$C(Q) = \mathbf{2}$$

3. **适应度计算**：
   $$F(Q) = 1 - \frac{C(Q)}{C_{\max}} = 1 - \frac{2}{28} = \frac{26}{28} = \mathbf{\frac{13}{14}} \approx \mathbf{0.9286}$$

---

### 第四大题：简答题要点
- **概念定义**：
  - **Exploration（探索/全局搜索）**：在大范围搜索空间中跳跃，寻找可能包含全局最优解的新区域（增加/维持多样性）。
  - **Exploitation（开发/局部搜索）**：利用已知的高适应度区域信息，在其附近进行精细化微调与深度搜索（减少多样性，收敛）。
- **驱动算子**：
  - **探索的驱动力**：重组算子（Crossover）在不同解之间做大跳跃；大步长变异（Mutation）。
  - **开发的驱动力**：选择算子（Selection）将资源倾斜给优质个体；小步长局部变异。
- **平衡机制与重要性**：
  - 过度偏向 Exploitation 会导致群体迅速收敛到局部极值（Premature Convergence）；过度偏向 Exploration 则会导致算法退化为无效率的纯随机游走。
  - GA 通过选择压力调节与自适应变异步长（如在搜索早期加大探索，后期加强开发）来实现两者的动态平衡。
