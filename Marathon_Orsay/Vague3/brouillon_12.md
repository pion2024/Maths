假设存在满足要求的等边三角形，其边长为$d\geqslant1$，顶点分别为$A,B,C$

- 设$J=(m_1,n_1),K=(m_2,n_2),M=(m_3,n_3)$分别为到$A,B,C$距离小于$\frac{1}{2025}$的三个整数点，也就是说 $0 \leqslant |A-J|,|B-K|,|C-M| \leqslant \frac{1}{2025}$ 且 $|A-B|=|B-C|=|C-A|=d$. 

由三角不等式得：

	- $d-\frac{2}{2025} \leqslant -|J-A|+|A-B|-|B-K|\leqslant \left|-|J-A|+|A-B|-|B-K|\right|$ $ \leqslant|J-K|=|J-A+A-B+B-K| $ 
$\leqslant|J-A|+|A-B|+|B-K|\leqslant d+\frac{2}{2025}$ 

- 即 $d-\frac{2}{2025}\leqslant |J-K|\leqslant d+\frac{2}{2025}$

同理有

- $d-\frac{2}{2025}\leqslant |K-M|\leqslant d+\frac{2}{2025}$

- $d-\frac{2}{2025}\leqslant |M-J|\leqslant d+\frac{2}{2025}$

于是

- $(d-\frac{2}{2025})^2\leqslant (m_i-m_j)^2+(n_i-n_j)^2\leqslant (d+\frac{2}{2025})^2,\quad \forall (i,j)\in\{1,2,3\}^2 \and i\neq j$

先用反证法证明不存在顶点全为整数点的等边三角形：

- 设等边三角形三个顶点$A,B,C$全为整数点，则补全该等边三角形为矩形$DEFG$，矩形的边分别与两条坐标轴平行。由于三角形有3个顶点，故$\triangle ABC$交矩形$DEFG$于4条边上的3点，故三个顶点中必有一个同时交矩形的两条边，即与矩形的某个顶点重合。设$C$与$F$重合。如图
- 三角形三个顶点$A,B,C$全为整数点，故$a=|AD|,b=|DB|,c=|BE|,d=|EF|,e=|FG|,f=|GA|$均为正整数。
- 于是矩形$DEFG$的边长为整数，故$S_{DEFG}$为整数。且$S_{ADB},S_{BEF},S_{AGF}$为整数。
- 故$S_{ABF}=S_{DEFG}-S_{ADB}-S_{BEF}-S_{AGF}\in\mathbb{N}^*$
- 然而三角形$ABC$边长为$l=\sqrt{a^2+b^2}$，则$S_{ABF}=\frac{\sqrt3}{4}l^2=\frac{\sqrt3}{4}(a^2+b^2)$,$(a^2+b^2)\in\mathbb{N}^*,\sqrt3\notin\mathbb{Q}\implies S_{ABF}\notin \mathbb{N}^*$， 矛盾

故不存在顶点全为整数点的等边三角形

下面证明，若符合要求的等边三角形存在，则其边长$d>253$.

- $(d+\frac{2}{2025})^2-(d-\frac{2}{2025})^2<1 \iff \frac{8d}{2025}<1 \iff d<\frac{2025}{8}=253.125$

- 假设 $d\leqslant 253\implies (d+\frac{2}{2025})^2-(d-\frac{2}{2025})^2<1$
- $(d-\frac{2}{2025})^2\leqslant (m_i-m_j)^2+(n_i-n_j)^2\leqslant (d+\frac{2}{2025})^2,\quad \forall (i,j)\in\{1,2,3\}^2 \and i\neq j$  且 $(m_i-m_j)^2+(n_i-n_j)^2 \in\mathbb{N}^*$， 故 $\exists k\in\mathbb{N}^*,(d-\frac{2}{2025})^2\leqslant k \leqslant (d+\frac{2}{2025})^2,\quad \forall (i,j)\in\{1,2,3\}^2 \and i\neq j$.

- 当$(d+\frac{2}{2025})^2-(d-\frac{2}{2025})^2<1$时，$\left[(d+\frac{2}{2025})^2,(d-\frac{2}{2025})^2\right[$区间上有且仅有1个整数，即$k$。于是 $(m_i-m_j)^2+(n_i-n_j)^2 = k,\quad \forall (i,j)\in\{1,2,3\}^2 \and i\neq j$，而这意味着$|J-K|=|K-M|=|M-J|=\sqrt{k}$ 即 三角形$JKM$为整数顶点等边三角形（这是提出并证明上面那个引理的动机），矛盾。

**我们于是证明了$d$的下界：若符合条件的三角形存在，则其边长 $d>253$。**

现在，我们只需要说明当$d$足够大时，确实存在符合要求的等边三角形。

令顶点$B=(-m,0),C(m,0),A=(0,\sqrt3m)$。 只需证明 $\exists m\in\mathbb{Z}$,使得$\sqrt3m$的小数部分$\{\sqrt3m\}\leqslant\frac{1}{2025}$。

只需证明，存在整数数列$\forall n\in\mathbb{N}^*,b_n\in\mathbb{N}^*,(b_n)_n \underset{n\to\infty}{\to} 0$，使得$\forall k\in\mathbb{N}^*,\{\sqrt3b_n\} \underset{k\to\infty}{\to} 0$

- 定义$\alpha_n \coloneqq \{\sqrt3n\}$,于是$\forall n \in\mathbb{N}^*, 0\leqslant \{\sqrt3n\} <1 \implies \exists l\in[0,1],\alpha_{n_k}\to l$ 即实数域上的有界数列$(\alpha_n)_n$存在收敛子列$(\alpha_{n_k})_k$。

- $\forall \varepsilon>0, \exists N,\forall k>N,\left|\{\sqrt3n_{k+1}\}-\{\sqrt3n_{k}\}\right|<\varepsilon$

- $(c_k) \coloneqq \{\sqrt3n_{k}\}$有界，故存在单调收敛子序列$(d_{m})$ 

- $\forall m\in\mathbb{N}^*, a_m \coloneqq n_{k_m} \in\mathbb{N}^*,a_{m+1}-a_m\geqslant1, d_m \coloneqq \{\sqrt3a{_m}\}$	

- $\forall \varepsilon>0,\exists M,\forall m>M, |d_{m+1}-d_m|<\varepsilon $

$(d_m)$单调递增或单调递减。

引理：$\forall \alpha,\beta\in\mathbb{R},\{\alpha\} \geqslant \{\beta\} \implies \lfloor \alpha-\beta\rfloor \geqslant \lfloor\alpha\rfloor - \lfloor\beta\rfloor$。证明如下：

- 设$\alpha = p_1+r_1, \beta = p_2+r_2,\quad p_1,p_2\in\mathbb{Z},r_1,r_2\in[0,1[,r_1=\{\alpha\} \geqslant r_2=\{\beta\}$ 
- 所以 $r_1\geqslant r_2 \implies \lfloor  p_1-p_2+(r_1-r_2) \rfloor \geqslant \lfloor p_1-p_2\rfloor = p_1-p_2$
- 即 $\lfloor \alpha-\beta\rfloor \geqslant \lfloor\alpha\rfloor - \lfloor\beta\rfloor$

推论

- $\forall \alpha,\beta\in\mathbb{R},\{\alpha\} \geqslant \{\beta\} \implies \{\alpha-\beta\} \leqslant \{\alpha\}-\{\beta\}=|\{\alpha\}-\{\beta\}|$

若 $(d_m)$ 单调递增，则$\forall m\in\mathbb{N}^*,d_{m+1}-d_{m}=\{\sqrt3a_{m+1}\}-\{\sqrt3a_{m}\}\geqslant0$, 下证$\forall m\in\mathbb{N}^*,\{\sqrt3(a_{m+1}-a_m)\} \leqslant |\{\sqrt3a_{m+1}\}-\{\sqrt3a_{m}\}|$

- 令$\alpha \coloneqq \sqrt3a_{m+1}, \beta \coloneqq \sqrt3a_{m},\quad \{\alpha\} \geqslant \{\beta\}$ 因为$(d_m)$递增。于是由引理推论知上式成立

令 $b_n \coloneqq a_{n+1}-a_{n} \in\mathbb{N}^*$ 于是 $\forall m\in\mathbb{N}^*,\{\sqrt3(a_{m+1}-a_m)\} \leqslant |\{\sqrt3a_{m+1}\}-\{\sqrt3a_{m}\}| $
$\implies \forall \varepsilon>0, \exists N,\forall n>N, \{\sqrt3b_n\}<\varepsilon \implies \exists m\in\mathbb{N}^*,\{\sqrt3b_m\}<\frac{1}{2025}$

若 $(d_m)$ 单调递减，则$d_{m+1}-d_{m}=\{\sqrt3a_{m+1}\}-\{\sqrt3a_{m}\} = \{\alpha\}-\{\beta\}\leqslant0$, 下证$\forall m\in\mathbb{N}^*,\{\sqrt3(a_{m}-a_{m+1})\} \leqslant |\{\sqrt3a_{m+1}\}-\{\sqrt3a_{m}\}|$; 注意第一项中对下标做了颠倒。

- 沿用之前的记号，令$\alpha \coloneqq \sqrt3a_{m+1}, \beta \coloneqq \sqrt3a_{m},\quad \{\alpha\} \leqslant \{\beta\}$ 因为$(d_m)$递减。

- $\{\alpha\} \leqslant \{\beta\} \iff \{-\alpha\} =1-\{\alpha\} \geqslant 1-\{\beta\} = \{-\beta\}$
- $\alpha' \coloneqq -\alpha,\beta'\coloneqq -\beta, \quad \{\alpha'\} \geqslant \{\beta'\}$
- 于是 $\forall m, \{\sqrt3(a_{m}-a_{m+1})\} = \{\alpha'-\beta'\} \leqslant |\{\alpha'\}-\{\beta'\}|=|1-\{\alpha\}-1+\{\beta\}| $
  $
  =|\{\beta\}-\{\alpha\}|=|\{\sqrt3a_{m}\}-\{\sqrt3a_{m+1}\}|=|d_{m}-d_{m+1}|=|d_{m+1}-d_m|<\varepsilon$ 

令 $b_n' \coloneqq a_{n}-a_{n+1} \in\mathbb{N}^*$ 故 $\forall m\in\mathbb{N}^*,\{\sqrt3(a_{m}-a_{m+1})\} \leqslant |\{\sqrt3a_{m+1}\}-\{\sqrt3a_{m}\}| $
$\implies \forall \varepsilon>0, \exists N,\forall n>N, \{\sqrt3b_n'\}<\varepsilon \implies \exists m\in\mathbb{N}^*,\{\sqrt3b_m'\}<\frac{1}{2025}$

**于是我们终于证明了存在性**：$\exists d\in\mathbb{N}^*,\{\sqrt3d\}<\frac{1}{2025}$。令$A=(-d,0),B=(d,0),C=(0,\sqrt3d)$,$ABC$构成符合题意的等边三角形。

Problem12证毕。





```latex
\documentclass[11pt]{article}
\usepackage[utf8]{inputenc}
\usepackage[T1]{fontenc}
\usepackage{amsmath, amssymb, amsthm}
\usepackage{fancyhdr}
\usepackage{mathrsfs}
\usepackage{enumitem}
\usepackage[french]{babel}
\usepackage{hyperref}
\usepackage[a4paper, margin=2.5cm]{geometry}

\pagestyle{fancy}
\fancyhf{}
\lhead{CHEN Pinyuan, L1, Université Paris Cité, Paris, PionChan@outlook.com}
\rhead{14 avril 2025}
\cfoot{\thepage}

\begin{document}
	
	\section*{Problème 12}
	
	On va d'abord retirer des informations des conditions nécessaires de l'existence d'un tel triangle demandé.  
	
	Supposons qu'il existe un triangle \emph{équilatéral} satisfaisant les conditions, de côté $d \geqslant 1$, dont les sommets sont $A$, $B$ et $C$.
	
	Soient $J=(m_1,n_1), K=(m_2,n_2), M=(m_3,n_3)$ trois points à coordonnées entières, situés respectivement à une distance inférieure à $\frac{1}{2025}$ de $A$, $B$, $C$, c'est-à-dire :
		\[ 0 \leqslant |A-J|, |B-K|, |C-M| \leqslant \frac{1}{2025}, \quad \text{et } |A-B|=|B-C|=|C-A|=d \]
	
	Par inégalité triangulaire, on a :
	\[
	d - \frac{2}{2025} \leqslant |J-K| \leqslant d + \frac{2}{2025}.
	\]
	De même,
	\[
	d - \frac{2}{2025} \leqslant |K-M| \leqslant d + \frac{2}{2025}, \quad
	d - \frac{2}{2025} \leqslant |M-J| \leqslant d + \frac{2}{2025}.
	\]
	D'où :
	\begin{equation}\label{eq:bornes}
		(d - \frac{2}{2025})^2 \leqslant (m_i - m_j)^2 + (n_i - n_j)^2 \leqslant (d + \frac{2}{2025})^2, \quad \forall (i,j) \in \{1,2,3\}^2, i \neq j.
	\end{equation}
	
	\subsection*{Preuve qu'il n'existe pas de triangle équilatéral dont tous les sommets sont des points entiers}
	
	Supposons que les trois sommets $A, B, C$ soient à coordonnées entières. Complétons ce triangle équilatéral en un rectangle $DEFG$ dont les côtés sont parallèles aux axes. Comme le triangle a 3 sommets et que le rectangle a 4 côtés, il existe un sommet du triangle qui coïncide avec un sommet du rectangle. Supposons que $C = F$.
	
	Comme $A,B,C$ sont entiers, alors les longueurs $a=|AD|, b=|DB|, c=|BE|, d=|EF|, e=|FG|, f=|GA|$ sont des entiers strictement positifs.
	
	Ainsi l'aire du rectangle $S_{DEFG} \in \mathbb{N}$, et les aires $S_{ADB}, S_{BEF}, S_{AGF}$ aussi.
	
	Donc $S_{ABF} = S_{DEFG} - S_{ADB} - S_{BEF} - S_{AGF} \in \mathbb{N}^*$.
	
	Mais la longueur $l = |AB| = \sqrt{a^2 + b^2}$ donne :
	\[S_{ABF} = \frac{\sqrt{3}}{4}l^2 = \frac{\sqrt{3}}{4}(a^2 + b^2), \quad a^2 + b^2 \in \mathbb{N}^*, \quad \sqrt{3} \notin \mathbb{Q} \implies  S_{ABF} \notin \mathbb{N}^*,\]
	ce qui est une contradiction.
	
	Donc, il n'existe pas de triangle à sommets tous entiers.
	
	\subsection*{Minoration de $d$}
	
	Montrons maintenant que si un triangle satisfaisant les conditions existe, alors $d > 253$.
	
	\[(d + \frac{2}{2025})^2 - (d - \frac{2}{2025})^2 < 1 \iff \frac{8d}{2025} < 1 \iff d < 253{,}125.
	\]
	
	Supposons $d \leqslant 253$, alors :
	\[(d + \frac{2}{2025})^2 - (d - \frac{2}{2025})^2 < 1, \implies \exists ! k \in \mathbb{N}^* \text{ tel que } k \in [(d - \frac{2}{2025})^2, (d + \frac{2}{2025})^2]\]
	 
	L'existence de $k$ est du à \eqref{eq:bornes} où $(m_i - m_j)^2 + (n_i - n_j)^2 \in \mathbb{N}^*$. L'unicité est due à l'étroitesse de cette intervalle car si elle comprenait deux entiers différents alors sa longueur serait au moins 1.  
	
	Donc $(m_i - m_j)^2 + (n_i - n_j)^2 = k,\ \forall i \neq j$.
	
	Cela implique que $JKM$ est un triangle équilatéral à sommets entiers (d'où la motivation de la preuve précédente) $\implies$ contradiction.
	
	\textbf{Donc, si un tel triangle existe, alors $d > 253$.}
	
	\subsection*{Existence d'un tel triangle}
	
	Maintenant, nous allons montrer que si $d$ est suffisamment grand, un tel triangle existe réellement.
	
	Soient$A = (-\delta, 0)$, $B = (\delta, 0)$, $C = (0, \sqrt{3}\delta)$. $ABC$ forme un triangle équilatéral. Donc il suffit de montrer qu'il existe $\delta \in \mathbb{Z}$ tel que $\{ \sqrt{3}\delta \} \leqslant \frac{1}{2025}$
	
	Il suffit de prouver l'existence d'une suite d'entiers $(b_n)_{n \in \mathbb{N}^*}$ telle que $\{ \sqrt{3}b_n \} \to 0$.
	
	Définissons $\alpha_n := \{\sqrt{3}n\}$. Alors $\alpha_n$ est une suite bornée dans $[0,1]$, donc il existe une sous-suite convergente $(\alpha_{n_k})$.
	
	Comme toute suite réelle bornée convergente admet une sous-suite monotone convergente, donc $\alpha_n$ admet une telle sous-suite \[d_m := \{\sqrt{3}a_m\} \text{ où } a_m := n_{k_m} \text{ croissante }\]  
	
	Dans la démonstration suivante, n'oublions pas que $(d_n)$ est monotone et convergente.  
	
	\textbf{Notation :} On note \[\lfloor x \rfloor \in\mathbb{Z} \text{ la partie entière (arrondi vers } -\infty \text{) d'un réel } x\]
	\[ \text{ et } 0\leqslant\{x\}<1 \text{ la partie décimale de } x\] 
	
	On a donc $x = \lfloor x \rfloor + \{x\}$, et $\lfloor x \rfloor $ croissante. 
	
	\textbf{Lemme :} \[\forall \alpha, \beta \in \mathbb{R}, \{\alpha\} \geqslant \{\beta\} \implies \lfloor \alpha - \beta \rfloor \geqslant \lfloor \alpha \rfloor - \lfloor \beta \rfloor\] 
	
	\textbf{Preuve: }
	
	Soit $\alpha = p_1 + r_1, \beta = p_2 + r_2, \quad p_1, p_2 \in \mathbb{Z}, r_1, r_2 \in [0, 1[, r_1 = \{\alpha\} \geqslant r_2 = \{\beta\}$.
	
	Ainsi, $r_1 \geqslant r_2 \implies \lfloor p_1 - p_2 + (r_1 - r_2) \rfloor \geqslant \lfloor p_1 - p_2 \rfloor = p_1 - p_2$.
	
	Donc, $\lfloor \alpha - \beta \rfloor \geqslant \lfloor \alpha \rfloor - \lfloor \beta \rfloor$.
	
	\textbf{Corollaire :}$\forall \alpha, \beta \in \mathbb{R}, \{\alpha\} \geqslant \{\beta\} \implies \{\alpha - \beta\} \leqslant \{\alpha\} - \{\beta\} = |\{\alpha\} - \{\beta\}|$. \\
	
	\textbf{Cas croissant} : si $(d_n)$ est croissante, on pose $b_n := a_{n+1} - a_n \in \mathbb{N}^*$, alors on montre que :
	\[\forall n\in\mathbb{N}^*, \{\sqrt{3}b_n\} = \{\sqrt{3}(a_{n+1} - a_n)\} \leqslant | \{\sqrt{3}a_{n+1}\} - \{\sqrt{3}a_n\} | = |d_{n+1}-d_n|.
	\]
	
	Soit $\alpha := \sqrt{3} a_{n+1}, \beta := \sqrt{3} a_n, \quad \{\alpha\} \geqslant \{\beta\}$ car $(d_n)$ est croissante. Par conséquent, d'après le corollaire du lemme, l'assertion est vérifiée. 
	Donc \[(d_n) \text{ est convergente} \implies | \{\sqrt{3}a_{n+1}\} - \{\sqrt{3}a_n\} | \to 0 \implies \{\sqrt{3}b_n\} \to 0,\]
	
	ce qui implique $ \exists m \in \mathbb{N}^* \text{ tel que } \{\sqrt{3}b_m\} < \frac{1}{2025}$ 
	
	\textbf{Cas décroissant} : 
	En reprenant les notations précédentes $\alpha := \sqrt{3} a_{n+1}, \beta := \sqrt{3} a_n,\quad \{\alpha\} \leqslant \{\beta\}$ car $(d_n)$ est décroissante.
	
	On a \[\{\alpha\} \leqslant \{\beta\} \iff \{-\alpha\} = 1 - \{\alpha\} \geqslant 1 - \{\beta\} = \{-\beta\}\]
	
	Soit $\alpha' = -\alpha,\ \beta' = -\beta \implies \{\alpha'\} \geqslant \{\beta'\}$.
	
	Ainsi, pour tout $n$, on a :
	\[
	\{\sqrt{3}(a_n - a_{n+1})\} = \{\alpha' - \beta'\} \leqslant |\{\alpha'\} - \{\beta'\}| = |1 - \{\alpha\} - 1 + \{\beta\}| = |\{\beta\} - \{\alpha\}|
	\]
	\[
	= |\{\sqrt{3} a_n\} - \{\sqrt{3} a_{n+1}\}| = |d_n - d_{n+1}| = |d_{n+1} - d_n| 
	\]
	
	Soit $b_n' := a_n - a_{n+1} \in \mathbb{Z}$. On a donc :
	\[
	\forall n \in \mathbb{N}^*,\ \{\sqrt{3}b_n'\} = \{\sqrt{3}(a_n - a_{n+1})\} \leqslant |\{\sqrt{3} a_{n+1}\} - \{\sqrt{3} a_n\}|
	\]
	
	Ce qui implique comme dans le cas dernier:
	\[
	\forall \varepsilon > 0,\ \exists N,\ \forall n > N,\ \{\sqrt{3} b_n'\} < \varepsilon \implies \exists m \in \mathbb{N}^*,\ \{\sqrt{3} b_m'\} < \frac{1}{2025}
	\]
	
	
	\textbf{Conclusion} :
	\[\exists \delta \in \mathbb{Z} \text{ tel que } \{ \sqrt{3}\delta \} < \frac{1}{2025}.
	\]
	
	On prend alors $A = (-\delta, 0)$, $B = (\delta, 0)$, $C = (0, \sqrt{3}\delta)$ : $ABC$ est un triangle \textit{équilatéral} conforme aux conditions.
	
	Ainsi, les deux idées de Bastien sont vérifiées.  
	
	\textbf{Fin de la preuve.}
	
\end{document}
```

