# EE6407 Quiz 1 模拟题 + 参考答案（3 套）

> 依据 EE6407 Lecture 1、Lecture 2、课堂录音及 `QUIZ REVIEW 1.md` 的范围和题型整理。  
> 建议：每套 **15 分钟、closed book、no calculator** 完成，然后再看答案。  
> 题型仿照原 Quiz Review：**10 道 T/F + O1 + PMX + CX + 简答题**。

---

# Mock Quiz 1 — Set 1

## Q1. True / False

判断下列陈述为 **True [T]** 或 **False [F]**。

1. Under the black-box characterization, if the model and desired output are known while the input is unknown, the problem is an optimisation problem.
2. A modelling problem can be transformed into an optimisation problem by defining an objective function measuring model error.
3. A constraint assigns a continuous quality score to every candidate solution.
4. Every Class P problem is also a Class NP problem.
5. Every NP-hard problem must be verifiable in polynomial time.
6. Evolutionary Algorithms are stochastic, population-based generate-and-test algorithms.
7. Parent selection normally acts as a force that increases population diversity.
8. Mutation-only evolutionary algorithms can work, while crossover-only evolutionary algorithms generally cannot.
9. One-point crossover can suffer from positional bias.
10. A normal one-gene random-reset mutation is generally unsuitable for permutation representation.

---

## Q2. Order One Crossover (O1)

For the permutation chromosomes

```text
Position:  1 2  3 4 5 6 7  8 9 10

P1 =       1 2 [3 4 5 6 7] 8 9 A
P2 =       9 1 [8 2 7 4 6] 3 5 A
```

perform **Order One Crossover** using positions **3–7**.

Write the two offspring.

---

## Q3. Partially Matched Crossover (PMX)

Using the same parents and crossover positions **3–7**,

```text
P1 = 1 2 [3 4 5 6 7] 8 9 A
P2 = 9 1 [8 2 7 4 6] 3 5 A
```

perform **PMX** and write the two offspring.

---

## Q4. Cycle Crossover (CX)

Using the complete chromosomes

```text
P1 = <1 2 3 4 5 6 7 8 9 A>
P2 = <9 1 8 2 7 4 6 3 5 A>
```

identify all cycles and construct two offspring by alternating cycles.

---

## Q5. Short Discussion

Explain why **fitness proportional selection** may be problematic at:

1. the **early stage** of a GA search; and
2. the **late stage** of a GA search.

Your answer should discuss **fitness difference, selection pressure, population diversity, and convergence**.

---

# Set 1 — Reference Answers

## A1. T/F

```text
1 T
2 T
3 F
4 T
5 F
6 T
7 F
8 T
9 T
10 T
```

### 简要解释

1. **T** — Black box 中 input 未知、model 和 output 已知，对应 optimisation。
2. **T** — 可以将 modelling 转成最小化预测误差等 optimisation。
3. **F** — Constraint 是是否满足要求的判断；连续质量评分属于 objective function。
4. **T** — 课程定义中 P 是 NP 的子集。
5. **F** — NP-hard 不一定属于 NP，也不保证解能在 polynomial time 内验证。
6. **T** — EA 属于 stochastic、population-based、generate-and-test 方法。
7. **F** — Selection 通常降低 diversity、推动 quality。
8. **T** — Lecture 2 明确强调 mutation-only EA 可行，而 crossover-only EA 不行。
9. **T** — 1-point crossover 更容易保留邻近 genes，因此存在 positional bias。
10. **T** — permutation 中单独重置一个 allele 容易产生重复元素和缺失元素。

---

## A2. O1

```text
P1 = 1 2 [3 4 5 6 7] 8 9 A
P2 = 9 1 [8 2 7 4 6] 3 5 A
```

### Child 1

复制 P1 的 segment：

```text
_ _ [3 4 5 6 7] _ _ _
```

从 P2 的 position 8 后开始循环读取：

```text
3, 5, A, 9, 1, 8, 2, 7, 4, 6
```

去掉 `{3,4,5,6,7}` 后：

```text
A, 9, 1, 8, 2
```

从 position 8 开始填：

```text
O1 = <8 2 3 4 5 6 7 A 9 1>
```

### Child 2

复制 P2 的 segment：

```text
_ _ [8 2 7 4 6] _ _ _
```

扫描 P1：

```text
8, 9, A, 1, 2, 3, 4, 5, 6, 7
```

去掉 `{8,2,7,4,6}` 后：

```text
9, A, 1, 3, 5
```

得到：

```text
O2 = <3 5 8 2 7 4 6 9 A 1>
```

### Final

```text
O1 = <8 2 3 4 5 6 7 A 9 1>
O2 = <3 5 8 2 7 4 6 9 A 1>
```

---

## A3. PMX

Segment mapping：

```text
3 ↔ 8
4 ↔ 2
5 ↔ 7
6 ↔ 4
7 ↔ 6
```

最终：

```text
O1 = <9 1 3 4 5 6 7 8 2 A>
O2 = <1 5 8 2 7 4 6 3 9 A>
```

检查：每个 allele 恰好出现一次，因此都是合法 permutation。

---

## A4. CX

```text
P1 = 1 2 3 4 5 6 7 8 9 A
P2 = 9 1 8 2 7 4 6 3 5 A
```

Cycles（positions）：

```text
C1 = {1, 2, 4, 5, 6, 7, 9}
C2 = {3, 8}
C3 = {10}
```

交替取 cycle：

```text
O1 = <1 2 8 4 5 6 7 3 9 A>
O2 = <9 1 3 2 7 4 6 8 5 A>
```

---

## A5. Fitness Proportional Selection

**Early stage:** 如果少数个体的 fitness 明显高于其他个体，它们会获得非常高的 selection probability，形成过强的 selection pressure。结果是这些个体快速占据 population，diversity 迅速下降，容易发生 **premature convergence**。

**Late stage:** 搜索后期个体 fitness 通常非常接近，因此 roulette-wheel probability 也很接近，selection pressure 变得很弱。Selection 接近 random selection，导致改进速度下降、convergence 变慢。

一句话记忆：

```text
Early: fitness gap large → pressure too strong → premature convergence
Late:  fitness gap small → pressure too weak   → slow convergence
```

---

# Mock Quiz 1 — Set 2

## Q1. True / False

1. Simulation corresponds to the case where the input and model are known but the output is unknown.
2. The search space contains all candidate objects of interest, including the desired solution.
3. An objective function is a binary yes/no test of feasibility.
4. NP stands for nondeterministic polynomial.
5. It is currently known that P is different from NP.
6. Recombination can combine information from multiple parents.
7. Crossover alone can create a new allele that is absent from the population.
8. Uniform crossover removes dependence of inheritance on chromosome position.
9. In integer representation, creep mutation tends to make a relatively small numerical change.
10. In a real-valued self-adaptive mutation scheme, the step size should be mutated before the decision variable.

---

## Q2. O1

```text
Position:  1 2 3  4 5 6 7 8  9 10

P1 =       A B C [D E F G H] I J
P2 =       B C A [E F D I H] J G
```

Use positions **4–8** for Order One Crossover.

---

## Q3. PMX

Using the same parents,

```text
P1 = A B C [D E F G H] I J
P2 = B C A [E F D I H] J G
```

perform PMX.

---

## Q4. CX

For

```text
P1 = <A B C D E F G H I J>
P2 = <B C A E F D I H J G>
```

find the cycles and produce two offspring.

---

## Q5. Exploration vs Exploitation

Define:

- **Exploration**
- **Exploitation**

Then explain the roles of **crossover** and **mutation** according to the lecture, and explain why an EA normally benefits from using both.

---

# Set 2 — Reference Answers

## A1. T/F

```text
1 T
2 T
3 F
4 T
5 F
6 T
7 F
8 T
9 T
10 T
```

### 简要解释

1. **T** — output 未知就是 simulation，用于回答 what-if。
2. **T** — 这是 lecture 对 search space 的定义。
3. **F** — objective function 给质量评分；constraint 才是是否满足要求。
4. **T** — NP = nondeterministic polynomial。
5. **F** — `P = NP ?` 仍未解决。
6. **T** — recombination 的主要作用之一就是组合 parent information。
7. **F** — crossover 只能重组已有 allele；新 allele 需要 mutation。
8. **T** — uniform crossover 中每一位独立决定来源，因此 inheritance independent of position。
9. **T** — creep 是对数值做小幅正/负变化。
10. **T** — self-adaptive mutation 中先 `σ → σ'`，再用 `σ'` 变异 `x`。

---

## A2. O1

```text
P1 = A B C [D E F G H] I J
P2 = B C A [E F D I H] J G
```

复制 P1 的 segment `{D,E,F,G,H}`，再从 P2 的 position 9 后开始循环读取并跳过已出现元素：

```text
J, G, B, C, A, E, F, D, I, H
→ J, B, C, A, I
```

从 position 9 开始填入：

```text
O1 = <C A I D E F G H J B>
```

反向操作：

```text
O2 = <B C G E F D I H J A>
```

### Final

```text
O1 = <C A I D E F G H J B>
O2 = <B C G E F D I H J A>
```

---

## A3. PMX

对应 segment mapping：

```text
D ↔ E
E ↔ F
F ↔ D
G ↔ I
H ↔ H
```

最终：

```text
O1 = <B C A D E F G H J I>
O2 = <A B C E F D I H G J>
```

---

## A4. CX

Cycles：

```text
C1 = {1,2,3}
C2 = {4,5,6}
C3 = {7,9,10}
C4 = {8}
```

交替 cycle：

```text
O1 = <A B C E F D G H I J>
O2 = <B C A D E F I H J G>
```

---

## A5. Exploration vs Exploitation

**Exploration**：寻找 search space 中新的、有潜力的区域，获取新的 problem information。

**Exploitation**：在一个已经发现的 promising region 附近继续优化，利用已有 information。

按 Lecture 2 的讲法：

- **Crossover → more explorative**：把两个 parents 的 information 结合起来，可进行较大的 jump。
- **Mutation → more exploitative**：通常产生 parent 附近的小型随机变化。

但两者还有互补作用：

- crossover 可以 **combine information from two parents**；
- mutation 可以 **introduce new alleles / new information**。

因此一般两者都保留最好。

---

# Mock Quiz 1 — Set 3

## Q1. True / False

1. A GA is a deterministic optimisation algorithm.
2. Selection pushes the population toward quality but tends to reduce diversity.
3. Mutation and recombination are variation operators.
4. Random initialisation usually aims to create a broad and diverse initial population.
5. Starting exclusively from known good solutions must always make a GA perform better.
6. The No Free Lunch idea implies that no single optimisation algorithm is best over all possible problems.
7. A finite L-bit chromosome can represent infinitely many real numbers exactly.
8. Increasing L in binary encoding can increase numerical precision.
9. Swap mutation preserves validity of a permutation.
10. In Cycle Crossover, offspring alleles are inherited at positions occupied by that allele in one of the parents.

---

## Q2. O1

```text
Position:  1 2  3 4 5 6 7  8 9 10

P1 =       A B [C D E F G] H I J
P2 =       B A [D C F E H] G J I
```

Use positions **3–7**.

---

## Q3. PMX

Use the same parents and crossover positions.

---

## Q4. CX

Using

```text
P1 = <A B C D E F G H I J>
P2 = <B A D C F E H G J I>
```

find all cycles and generate offspring by alternating cycles.

---

## Q5. Applied GA Design

You want to use a GA to solve a **graph colouring** problem.

Assume there are \(n\) regions and exactly **4 colours** are available.

Answer:

1. Give a suitable chromosome representation.
2. State what each gene and allele mean.
3. Define a suitable objective/fitness function.
4. State the condition for an optimum feasible solution.

---

# Set 3 — Reference Answers

## A1. T/F

```text
1 F
2 T
3 T
4 T
5 F
6 T
7 F
8 T
9 T
10 T
```

### 简要解释

1. **F** — GA 是 stochastic metaheuristic，不是 deterministic algorithm。
2. **T** — selection 减少 diversity、推动 quality。
3. **T** — mutation 和 recombination 都产生 variation。
4. **T** — random initialization 通常追求 broad spread / diversity。
5. **F** — 过强的 seed 可能限制搜索区域，甚至增加 premature convergence 风险。
6. **T** — NFL 的核心就是不存在对所有问题都最优的 universal optimiser。
7. **F** — L-bit 只能表示 \(2^L\) 个不同离散编码。
8. **T** — L 越长通常 precision 越高，但 chromosome 也更长。
9. **T** — swap 只交换两个位置，不产生重复/缺失 allele。
10. **T** — CX 的核心正是 position-preserving inheritance。

---

## A2. O1

```text
P1 = A B [C D E F G] H I J
P2 = B A [D C F E H] G J I
```

O1：

```text
O1 = <A H C D E F G J I B>
O2 = <B G D C F E H I J A>
```

---

## A3. PMX

Mapping：

```text
C ↔ D
D ↔ C
E ↔ F
F ↔ E
G ↔ H
```

PMX：

```text
O1 = <B A C D E F G H J I>
O2 = <A B D C F E H G I J>
```

---

## A4. CX

```text
P1 = A B C D E F G H I J
P2 = B A D C F E H G J I
```

Cycles：

```text
C1 = {1,2}
C2 = {3,4}
C3 = {5,6}
C4 = {7,8}
C5 = {9,10}
```

交替 cycles：

```text
O1 = <A B D C E F H G I J>
O2 = <B A C D F E G H J I>
```

---

## A5. Graph Colouring

### 1. Representation

使用 **integer representation**：

\[
Q=\langle q_1,q_2,\ldots,q_n\rangle
\]

其中：

```text
qi ∈ {1,2,3,4}
```

### 2. Gene / Allele

- gene position \(i\)：表示第 \(i\) 个 region；
- allele \(q_i\)：表示该 region 被赋予的 colour。

例如：

```text
<1, 3, 2, 4, 1, ...>
```

表示不同区域分别采用 colour 1、3、2、4、1……

### 3. Objective / Fitness Function

一种简单定义是：

\[
F(Q)=\text{number of adjacent region pairs having different colours}
\]

即对每条 adjacency edge：

\[
f(i,j)=
\begin{cases}
1,&q_i\neq q_j\\
0,&q_i=q_j
\end{cases}
\]

然后：

\[
F(Q)=\sum_{(i,j)\in E}f(i,j)
\]

目标：

```text
maximize F(Q)
```

也可以反过来定义冲突数：

\[
C(Q)=\sum_{(i,j)\in E} [q_i=q_j]
\]

然后：

```text
minimize C(Q)
```

### 4. Optimum condition

如果使用 conflict formulation：

```text
C(Q) = 0
```

意味着所有相邻 region 都使用不同 colour，即得到 feasible 4-colouring。

如果使用 fitness formulation：

```text
F(Q) = |E|
```

其中 \(|E|\) 是所有 adjacency pairs 的数量。

---

# 考前速查

## Black Box

```text
unknown input  → optimisation
unknown model  → modelling
unknown output → simulation
```

## EA 两股力量

```text
mutation + recombination → diversity / novelty ↑
selection                → diversity ↓, quality ↑
```

## Crossover vs Mutation

```text
crossover → combine parent information
mutation  → introduce new allele / information

Lecture framing:
crossover → exploration
mutation  → exploitation / local random diversion
```

## Binary crossover

```text
1-point → positional bias
n-point → still positional bias
uniform → independent of position
```

## Permutation

```text
valid chromosome: every element occurs exactly once

mutation:
swap
insert
scramble
inversion

crossover:
O1
PMX
CX
edge recombination
```

## Fitness proportional selection

```text
Early:
large fitness difference
→ excessive selection pressure
→ diversity loss
→ premature convergence

Late:
small fitness difference
→ weak selection pressure
→ almost random selection
→ slow convergence
```

## NP

```text
P ⊆ NP
P vs NP: unknown

NP-complete:
belongs to NP
+ every NP problem polynomially reducible to it

NP-hard:
at least as hard as NP-complete
but need not belong to NP
```

---

# 建议使用方法

1. 第一次只看题目，**15 分钟计时**。
2. 做完再展开答案。
3. O1 / PMX / CX 一定手写过程，不要只背最终 offspring。
4. T/F 遇到绝对词尤其警惕：
   - always
   - must
   - only
   - guaranteed
5. Quiz 前优先确保以下知识没有混淆：
   - optimisation / modelling / simulation
   - objective function / constraint
   - P / NP / NP-complete / NP-hard
   - selection / recombination / mutation
   - exploration / exploitation
   - O1 / PMX / CX
   - fitness proportional selection 在 early / late stage 的问题
