Collected and noted by : JingShing

# Probability theory note 機率論筆記

## 機率論(一)

* 在尋找掌控自然界現象的法則中，科學上常會面臨一件事是否發生
  * 1)有確定性
  * 2)無確定性
* 在任何實驗中一個件事可能發生或可能不發生稱為隨機
* 機率: 描述隨機(random)事件發生可能性大小

註：降雨機率80%是什麼意思？

#### 降雨機率80%是什麼意思？

* 在相同天氣條件下，平均每100天會有幾天發生降雨，這個定義除了適用於針對某個「區域」做預報，也可以用在某個「特定地點」的天氣預報。
* 覆蓋率:該區域只有80%的地方會出現降雨

* 由於發生或不發生是難於決定，因此希望用一數字(量化)去表示一隨機事件發生機會是多少，機率論就是處理這類問題
* 科學或工程上，經過一連串試驗某事件發生的比例常會趨近一常數，而此常數就是機率論要估計的量，如投擲一公正銅板出現正面的機率=1/2

### 學習目的

1. 討論如何解釋事件的機率以及機率運算所遵循的一些法則, 藉此可對不確定的事件做出適切的決策
2. 機率論為統計學基礎而後者為分析資料的重要工具
3. 巨量資量(Big Data)盛行

### E-Promotion案例

### Healthcare monitoring案例

* Google Flu Trends (流感預測趨勢)透過分析無數筆匿名的流感關鍵字數據，像是「咳嗽」、「發燒」和「疼痛」等字眼，比聯邦疾病控制與預防中心提前7到14天準確預測流感的爆發

### 隨機實驗

* 隨機(random)實驗的意義
* 隨機實驗是一種過程(process)，是一種不能確定預知會發生何種結果的實驗方式。在實驗前已知所有可能出現的結果，而實驗後的結果為所有可能的結果之一，但實驗前並未能正確的、肯定的預知它是何種結果。隨機實驗可重複進行，而經過長期重複實驗，出現的結果會遵循某一些統計規則。

### 機率理論

* 大數法則  (Law of Large Numbers)若某事件有既定的機率，而我們不斷的進行相同的實驗，則該事件發生的次數比例會越來越接近這個既定的機率。
* 統計中的「大數法則」是指一實驗或觀測能重複地進行且次數夠多時，實際觀測到的現象(如樣本的平均值), 會和母群體的現象一致。

#### 大數法則的應用(1)

* 假設有一個賭局，賭一賠一，你的勝率為55%。若你有100元，想在這個賭局中獲利，請問你那一種操作策略勝算最大？

A. 一次200元(再向人借100元)

B. 一次100元

C. 每次十元

D. 每次一元

E. 以上皆非

ANS : D -> 基於大數法則，D可以進行更多次博弈，亦更接近於期望值勝率。

#### 大數法則的應用(2)

* 大數法則運用在保險上面最常見的就是死亡率。
* 壽險業利用“臺灣壽險業第五回經驗生命表”來計算保費的基準(以一千萬人為基準)。
* 人壽保險公司的運作很像賭場─賭被保險人會不會死亡:依據死亡率,預測出必須給付的理賠金期望值,然後訂出保費來保障其公司之利潤。

## 機率論(二) 

* 課程大綱
  1. 機率公設
  2. 組合方法
  3. 條件機率及獨立事件
  4. 分佈函數及隨機變數(包括離散型, 連續型)
  5. 聯合分佈函數
  6. 期望值與變異數
  7. 中央極限定理

## 機率論(四)

* 後續相關課程:
  1. 影像處理(image processing), 資料壓縮(data compression), 圖像識別(pattern recognition), 機器學習(machine learning), 統計與資料分析(statistics and data analysis)
  2. 資管: 統計學

## Chap 1: Axioms of Probability

* 1.1: Introduction
 * (a) Classical probability
 * (b) Relative frequency probability
 * (c) Subjective probability

* 以上三種機率理論不論採用那一個都必需滿足一些前提, 才能進行機率演算
* 拋開這三種機率理論解釋, 完全由機率的性質及演算方法來定義機率,一般稱為公設的(axiomatic)機率理論
* 公設的選取需具備簡單,無爭議性,及不需驗證的特性

## 1.2 Sample Space and Events

* If the outcome of an experiment is not certain but all of its possible outcomes are predictable in advance, then the set of all these possible outcomes is called the sample spaceof the experiment and is usually denoted by S.Therefore, the sample space of an experiment consists of all possible outcomes of the experiment. These outcomes are sometimes called sample points, or simply points, of the sample space. In the language of probability, certain subsets of S are referred to as events. So events are sets of points of the sample space.
* See examples 1.1~1.6

## References

* 林惠玲、陳正蒼:應用統計學四版
* S. Ghahramani: Fundamentals of Probability (with stochastic processes),3th Edition, Pearson Education Limited(滄海書局)

date:22/9/12

## 1-3 Axioms of Probability

1933 soviet Andrei Kolmogorov 提出

Certain simple, indisputable and consistent statement without justification.

Note: the classical definition is a simple result of axiometic approach.

## Definitions(Probability Axioms)

S: Sample Space
A: event
P(A): Probability of A

* Axiom 1
  * $P(A) \geq 0$
* Axiom 2
  * $P(S) = 1$
* Axiom 3
  * if { $A_1$, $A_2$, $A_3$ .. $A_n$ } is a sequence of mutually exclusive(互斥) events(i.e. the joint occurence of every pair of them is impossible : $A_iA_j = \phi$ when ( $ i \neq j $ ) then $P(\bigcup_{i=1}^{\infty}A_i)=\sum_{i=1}^\infty P(A_i)$

**Equally likely** -> if A and B are equally likely means that $P(A) = P(B)$

## Theorem 1.1

the probability of the empty set $\phi$ is 0. Thus $P(\phi) = 0$

Let $A_1 = S$ and $A_i = \phi$ for $i \geq 2$ then $A_1, A_2, .., A_n$ is a sequence of mutually exclusive event set.

$P(S) = P(\bigcup_{i=1}^{\infty}A_i) = \sum_{i=1}^\infty P(A_i) = P(S) + \sum_{i=2}^\infty P(A_i) = P(S) + \sum_{i=1}^\infty P(\phi)$

implying that $\sum_{i=1}^\infty P(\phi) = 0$. That is possible only if $P(\phi)=0$

* Axiom 1 -> $P(S) = 1$
* Axiom 2 -> $P(A)\geq0$

$P(A_1 \bigcup A_2)=P(A_1)+P(A_2)$

### Note

(1) example:roll the dice

(2) relation to axiom 3

(3) example:the sample points are infinite

以投骰子為例：

令 $A_n$ 表示扔骰子一直到第 n 次才出現6的事件

$P(\bigcup_{i=1}^{\infty}A_i)=$ 扔骰子直到出現 6 的機率

$\bigcup_{i=1}^{\infty}A_i=$ 扔骰子直到出現 6 的事件

$P(A_i) = (\frac{5}{6}^{i-1})(\frac{1}{6}) = \frac{1}{6} \frac{1 - (\frac{5}{6}^{i-1})}{1 - \frac{5}{6}}$ (等比公式)

等比公式：$a^{n+1} = a_1 . \frac{1-r^n}{1-r}$

$\frac{5}{6}^{i-1} = $ (前 $i-1$ 次沒出現 6)沒有扔到 6 的事件

$\frac{1}{6} = $ 扔到 6 的事件



$P(A\bigcup A^c) = P(A) + P(A^c) = P(S) = 1$

## Example 1.9

A coin is called unbiased or fair.

The sample space $S = \{T, H\}$ (T means tail, H means head)

$P(S) = P(\{T, H\}) = P(\{T\}+P(\{H\})$

$\{T\},\{H\}$ are equally likely, so $P(\{T\}=P(\{H\})$

$1 = P(S) = P(\{T, H\})=P(\{T\}+P(\{H\})=2P({H})$

$P({H})=\frac{1}{2}$

using Axiom 2 and Axiom 3

date:22/9/13
