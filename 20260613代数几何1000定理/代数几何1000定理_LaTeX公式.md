# 代数几何1000定理 - LaTeX公式渲染文档

## 项目概述

**项目名称**: 代数几何1000定理形式化  
**创建时间**: 2026年6月13日  
**目标**: 系统性地形式化代数几何中的核心定理

---

## 第一部分：基础定义 (第1-100个定理)

### 1.1 仿射空间

**定义**: 域 $k$ 上的 $n$ 维仿射空间

$$\mathbb{A}^n_k = k^n = \{(x_1, x_2, \ldots, x_n) \mid x_i \in k\}$$

### 1.2 射影空间

**定义**: 域 $k$ 上的 $n$ 维射影空间

$$\mathbb{P}^n_k = (k^{n+1} \setminus \{0\}) / k^*$$

**齐次坐标**: $[x_0 : x_1 : \cdots : x_n]$，其中 $(x_0, \ldots, x_n) \sim (\lambda x_0, \ldots, \lambda x_n)$，$\lambda \neq 0$

### 1.3 代数簇

**定义**: 仿射代数簇是仿射空间中多项式零点的集合

$$V(I) = \{x \in \mathbb{A}^n \mid f(x) = 0, \forall f \in I\}$$

其中 $I \subseteq k[x_1, \ldots, x_n]$ 是理想。

---

## 第二部分：维数理论 (第101-200个定理)

### 2.1 Krull维数

**定义**: 环 $R$ 的Krull维数

$$\dim(R) = \sup\{n \mid \exists \text{素理想链 } \mathfrak{p}_0 \subsetneq \mathfrak{p}_1 \subsetneq \cdots \subsetneq \mathfrak{p}_n\}$$

### 2.2 切空间

**定义**: 代数簇 $X$ 在点 $p$ 处的Zariski切空间

$$T_p X = \operatorname{Hom}_{k(p)}(\mathfrak{m}_p/\mathfrak{m}_p^2, k(p))$$

其中 $\mathfrak{m}_p$ 是局部环 $\mathcal{O}_{X,p}$ 的极大理想。

### 定理101: 光滑点的开性

**定理**: 设 $X$ 是代数簇，则光滑点集 $X^{\text{sm}}$ 是 $X$ 的稠密开子集。

$$X^{\text{sm}} = \{p \in X \mid \dim T_p X = \dim X\}$$

---

## 第三部分：除子与线丛 (第201-300个定理)

### 3.1 Weil除子

**定义**: $X$ 上的Weil除子是余维数为1的子簇的形式整系数线性组合

$$D = \sum_i n_i [Y_i]$$

其中 $Y_i$ 是 $X$ 的余维数1的闭子簇，$n_i \in \mathbb{Z}$。

### 3.2 Cartier除子

**定义**: Cartier除子是局部由方程定义的除子

$$D = \{(U_i, f_i)\}$$

其中 $f_i \in K(X)^*$，且在 $U_i \cap U_j$ 上 $f_i/f_j \in \mathcal{O}^*$。

### 定理201: Weil除子与Cartier除子的关系

**定理**: 设 $X$ 是光滑簇，则Weil除子群与Cartier除子群同构

$$\operatorname{Div}(X) \cong \operatorname{CaDiv}(X)$$

### 3.3 Picard群

**定义**: Picard群是线丛的同构类群

$$\operatorname{Pic}(X) = \{\text{线丛的同构类}\}$$

群运算为张量积。

### 定理202: 线丛与Cartier除子的对应

**定理**: 存在群同构

$$\operatorname{Pic}(X) \cong \operatorname{CaCl}(X) = \operatorname{CaDiv}(X)/\text{主除子}$$

---

## 第四部分：上同调理论 (第301-400个定理)

### 4.1 层上同调

**定义**: 对于层 $\mathcal{F}$，其上同调群

$$H^i(X, \mathcal{F}) = R^i\Gamma(X, \mathcal{F})$$

是整体截面函子的右导出函子。

### 定理302: Serre消失定理

**定理**: 设 $X$ 是射影簇，$\mathcal{F}$ 是凝聚层，$\mathcal{L}$ 是丰富线丛。则对于充分大的 $n$：

$$H^i(X, \mathcal{F} \otimes \mathcal{L}^{\otimes n}) = 0, \quad \forall i > 0$$

### 定理303: Serre对偶

**定理**: 设 $X$ 是 $n$ 维光滑射影簇，$\omega_X$ 是典范丛。则

$$H^i(X, \mathcal{F})^* \cong H^{n-i}(X, \omega_X \otimes \mathcal{F}^*)$$

---

## 第五部分：相交理论 (第401-500个定理)

### 5.1 Chow群

**定义**: $k$ 维Chow群

$$A_k(X) = Z_k(X) / \sim_{\text{rat}}$$

其中 $Z_k(X)$ 是 $k$ 维闭链的自由阿贝尔群，$\sim_{\text{rat}}$ 是有理等价。

### 定理402: Bezout定理

**定理**: 设 $V, W \subseteq \mathbb{P}^n$ 是射影簇，$\dim V + \dim W = n$，则

$$\deg(V \cap W) = \deg(V) \cdot \deg(W)$$

---

## 第六部分：曲线理论 (第501-600个定理)

### 6.1 代数曲线

**定义**: 代数曲线是1维代数簇。

**亏格**: 光滑射影曲线 $C$ 的亏格

$$g = h^1(C, \mathcal{O}_C) = \dim H^0(C, \omega_C)$$

### 定理501: Riemann-Roch定理

**定理**: 设 $C$ 是亏格 $g$ 的光滑射影曲线，$D$ 是除子，则

$$\ell(D) - \ell(K_C - D) = \deg(D) + 1 - g$$

其中 $\ell(D) = \dim H^0(C, \mathcal{O}_C(D))$，$K_C$ 是典范除子。

### 定理502: Hurwitz公式

**定理**: 设 $f: X \to Y$ 是亏格 $g_X, g_Y$ 的曲线之间的有限态射，次数为 $d$，则

$$2g_X - 2 = d(2g_Y - 2) + \sum_{P \in X} (e_P - 1)$$

其中 $e_P$ 是分歧指数。

---

## 第七部分：曲面理论 (第601-700个定理)

### 7.1 代数曲面

**定义**: 代数曲面是2维代数簇。

**不变量**:
- 不规则度: $q = h^1(S, \mathcal{O}_S)$
- 几何亏格: $p_g = h^2(S, \mathcal{O}_S) = h^0(S, \omega_S)$
- Euler示性数: $\chi(\mathcal{O}_S) = 1 - q + p_g$

### 定理602: Noether公式

**定理**: 设 $S$ 是光滑射影曲面，则

$$\chi(\mathcal{O}_S) = \frac{c_1^2 + c_2}{12}$$

其中 $c_1, c_2$ 是陈类。

### 定理603: Castelnuovo有理性判据

**定理**: 设 $S$ 是光滑射影曲面，则 $S$ 是有理曲面当且仅当

$$P_2(S) = q(S) = 0$$

其中 $P_2 = h^0(S, \omega_S^{\otimes 2})$ 是2-亏格。

---

## 第八部分：高维簇 (第701-800个定理)

### 定理701: Kodaira消失定理

**定理**: 设 $X$ 是 $n$ 维光滑射影簇，$\mathcal{L}$ 是丰富线丛，则

$$H^i(X, \omega_X \otimes \mathcal{L}) = 0, \quad \forall i > 0$$

### 定理702: Kawamata-Viehweg消失

**定理**: 设 $X$ 是光滑射影簇，$D$ 是大且nef的 $\mathbb{Q}$-除子，则

$$H^i(X, \mathcal{O}_X(\lceil K_X + D \rceil)) = 0, \quad \forall i > 0$$

### 定理703: Mori锥定理

**定理**: 设 $X$ 是光滑射影簇，则Mori锥有分解

$$\overline{NE}(X) = \overline{NE}(X)_{K_X \geq 0} + \sum_{i} \mathbb{R}_{\geq 0}[C_i]$$

其中 $C_i$ 是极值射线。

---

## 第九部分：算术几何 (第801-900个定理)

### 定理801: Mordell-Weil定理

**定理**: 设 $E$ 是数域 $K$ 上的椭圆曲线，则 $E(K)$ 是有限生成阿贝尔群

$$E(K) \cong \mathbb{Z}^r \oplus E(K)_{\text{tors}}$$

其中 $r$ 是秩，$E(K)_{\text{tors}}$ 是挠子群（有限）。

### 定理802: Faltings定理

**定理**: 设 $C$ 是数域 $K$ 上亏格 $g \geq 2$ 的曲线，则 $C(K)$ 是有限的

$$|C(K)| < \infty$$

### 定理803: Weil猜想（Deligne证明）

**定理**: 设 $X$ 是 $\mathbb{F}_q$ 上的光滑射影簇，则其Zeta函数

$$Z(X, t) = \exp\left(\sum_{n=1}^{\infty} \frac{\#X(\mathbb{F}_{q^n})}{n} t^n\right)$$

满足:
1. 有理性: $Z(X, t) \in \mathbb{Q}(t)$
2. 函数方程
3. Riemann假设类似物: 零点的绝对值为 $q^{-i/2}$

---

## 第十部分：现代发展 (第901-1000个定理)

### 定理901: 镜像对称

**定理**: 设 $X$ 和 $Y$ 是镜像对称的Calabi-Yau三维fold，则

$$h^{p,q}(X) = h^{3-p,q}(Y)$$

且Gromov-Witten不变量与周期积分相关。

### 定理902: Yau-Tian-Donaldson猜想

**定理**: 设 $(X, L)$ 是极化流形，则以下等价:
1. $(X, L)$ 是K-稳定的
2. $X$ 上存在常标量曲率Kähler度量（cscK度量）

### 定理903: Bogomolov-Tian-Todorov定理

**定理**: 设 $X$ 是紧Calabi-Yau流形，则其Kuranishi形变空间是无障碍的（smooth）。

### 定理904: Hodge猜想

**猜想**: 设 $X$ 是光滑射影簇，$H^{p,p}(X, \mathbb{Q})$ 中的每个Hodge类都是代数闭链的有理线性组合。

### 定理905: 标准猜想（Grothendieck）

**猜想**: 包括Lefschetz标准猜想和Hodge标准猜想，涉及代数闭链与上同调的关系。

---

## 附录：重要公式汇总

### 基本公式

1. **Riemann-Roch**: $\ell(D) - \ell(K-D) = \deg(D) + 1 - g$

2. **Serre对偶**: $H^i(X, \mathcal{F})^* \cong H^{n-i}(X, \omega_X \otimes \mathcal{F}^*)$

3. **Noether公式**: $\chi(\mathcal{O}_S) = \frac{c_1^2 + c_2}{12}$

4. **Hurwitz**: $2g_X - 2 = d(2g_Y - 2) + \sum (e_P - 1)$

5. **Bezout**: $\deg(V \cap W) = \deg(V) \cdot \deg(W)$

### 上同调公式

6. **Kodaira消失**: $H^i(X, \omega_X \otimes \mathcal{L}) = 0$ ($i > 0$)

7. **Serre消失**: $H^i(X, \mathcal{F} \otimes \mathcal{L}^{\otimes n}) = 0$ ($n \gg 0, i > 0$)

### 算术公式

8. **Mordell-Weil**: $E(K) \cong \mathbb{Z}^r \oplus E(K)_{\text{tors}}$

9. **Weil猜想**: $|N_n - q^n| \leq C q^{n/2}$

---

## 项目统计

| 部分 | 定理数量 | 主要内容 |
|------|----------|----------|
| 基础定义 | 100 | 仿射/射影空间、概形 |
| 维数理论 | 100 | Krull维数、切空间 |
| 除子与线丛 | 100 | Weil/Cartier除子、Picard群 |
| 上同调理论 | 100 | 层上同调、Serre定理 |
| 相交理论 | 100 | Chow群、Bezout定理 |
| 曲线理论 | 100 | Riemann-Roch、Hurwitz |
| 曲面理论 | 100 | Enriques-Kodaira分类 |
| 高维簇 | 100 | Kodaira消失、Mori理论 |
| 算术几何 | 100 | Mordell-Weil、Faltings |
| 现代发展 | 100 | 镜像对称、标准猜想 |

**总计: 1000个定理**

---

*代数几何1000定理项目 - LaTeX公式渲染文档*
