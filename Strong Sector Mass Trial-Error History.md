# Strong Sector Mass Trial-Error History

**用途**：Resolution β-2 Călugăreanu Lock picture 抵達前的迭代歷史記錄——失敗的 ansätze、否決的 candidate、推演的中間步驟。主要 workdoc [Strong Sector Mass 總結](Strong%20Sector%20Mass%20總結.md) 只 keep final result。

**創建**：2026-05-08

---

## §1. Picture Trajectory 全覽

| Stage | Picture | Status | 失敗 mode |
|---|---|---|---|
| 1 | Simple winding (Tw=$\{0,+1\}$) | ✗ | 結構性無法生指數階梯 |
| 2 | Single-mechanism modular tensor data candidates (II/II-a'/III/IV) | ✗ | 全部 bounded $\le \sqrt{3}$ |
| 3 | Vertical × Horizontal product decomposition | ✓ | Empirical decomposition + top saturation 自洽 |
| 4 | Variant C 1-knot chirality (Jones polynomial) | ✗ | $B_3$-derivable 1-knot family 全部 fail |
| 5 | Hyperbolic volume 1-knot (Upgrade A) | ✗ | $B_3$ 1-knot family 不對齊 |
| 6 | 3-component link (Resolution β) | ✓ | 量級對齊，剩 acceleration detail |
| 7 | **Călugăreanu Lk = Tw + Wr lock (β-2)** | ✓ | Picture conceptual closure |

---

## §2. Single-Mechanism Modular Tensor Candidates（全 fail）

四個 candidate pictures 嘗試直接從 SU(2)_4 modular tensor data 給 Yukawa hierarchy formula。

### 2.1 Candidate II: F-Symbols 主導 Yukawa

**Hypothesis**：$y_q \propto |F^{V_3}_{V_n V_{\rm Tw} V_3}|$，F-symbol 是 6j-symbol 對應。

**Numerical test 結果**：
- 測試 $|w| = (3-n) + (1-\text{Tw})$：預測 $y_b = y_c$（觀測差 3.3×），$y_s = y_u$（觀測差 42×）✗
- 測試 $|w| = 2(3-n) + (1-\text{Tw})$：log ratio self-consistency fail（觀測 0.76 vs 預測 0.5）✗
- 直接反推 $|w|_q$：非整數，且任何 $(n, \text{Tw})$ 雙線性組合無法 reproduce 觀測 6 元組

**Failure mode**：F-symbol bounded $\le 1$，**無 sign**，n=1 反向 vs n≥2 正向 crossover 不對。

### 2.2 Candidate II-a': Phase-Coherent F-Product

**Hypothesis**：$y_q^{(\text{Tw}=+1)} = y_q^{(\text{Tw}=0)} \cdot |1 - f e^{2\pi i h_n}|$，加干涉 phase coherence。

**Numerical**（取 $f = 0.5$）：

| $n$ | $h_n$ | 預測 $\mu_n$ | 觀測 |
|---|---|---|---|
| 1 | $1/8$ | $0.737$ | $0.48$（factor 1.5 ◐）|
| 2 | $1/3$ | $1.323$ | $13.3$（factor 10 ✗）|
| 3 | $5/8$ | $1.398$ | $42$（factor 30 ✗）|

**Failure mode**：干涉因子 $|1 - f e^{i\phi}| \in [1-f, 1+f]$ **絕對 bounded $\le 2$**，c/s, t/b 的 13×, 42× enhancement 永遠無法 reach。

但 n=1 給 factor 1.5 算 in the right ballpark——picture-internal sign-flip 方向對齊（n=1 destructive interference 對齊 u<d）。

### 2.3 Candidate III: Modular S-Matrix

**Hypothesis**：$y_q \propto |S_{V_n V_{\rm sat}}/S_{V_0 V_{\rm sat}}|$。

**Numerical**：

測 1：$V_{\rm sat} = V_3$, $k+2 = 6$（full $SU(2)_4$）：
| $a$ | $|S$-ratio$|$ |
|---|---|
| 0 | $1$ |
| 1 | $1$ |
| 2 | $0$ |
| 3 | $1$ |

n=2 給 zero——**結構性失敗**。

測 2：truncated $SU(2)_3$ ($k+2 = 5$)，$V_{\rm sat} = V_3$：
| $a$ | $|S$-ratio$|$ |
|---|---|
| 0 | $1$ |
| 1 | $\varphi \approx 1.618$ |
| 2 | $\varphi$ |
| 3 | $1$ |

monotonic 失敗 + bounded $\le \varphi$。

**Failure mode**：S-matrix entries 是 $\sin$ 函數，bounded $\in [-1, 1]$，**無法 span 5 orders**。

### 2.4 Candidate IV: Axial Fiber Dual Polarization

**Hypothesis**：axial fiber 帶兩 polarization $|+\rangle, |-\rangle$（Higgs-like doublet）。

**測試**：
- 直接 overlap $\langle V_n | V_3 \rangle$：SU(2) self-conjugate，只 $V_3$ 給非零
- Fusion-to-trivial：$V_n \otimes V_3$ 投影到 trivial 只 $V_3 \otimes V_3 \supset V_0$，給步階函數

**直接 numerical fail，但 picture-level 給 useful 結構觀察**：
1. **Axial fiber ≅ SM Higgs doublet** 拓撲識別
2. **Up/down 不對稱不是 symmetric Tw split**——是兩個 axial polarization 各自的 saturation 行為差異
3. Yukawa decomposition：$y_q = y^H(n) \cdot \mu(n, \text{Tw})$ motivation source

**這個 candidate 雖然 numerical fail，但 motivate 後續的 vertical × horizontal product picture (Stage 3)**。

### 2.5 Common Failure Mode

**所有 4 個 modular tensor data candidates hit 同一 ceiling**：single modular tensor data ratio 量級 $\le O(\varphi)$。要 span 5 orders Yukawa hierarchy **結構性需要 multiplicative product structure** 或 **non-modular invariant**（hyperbolic volume）。

---

## §3. Variant C 1-Knot Picture 迭代

從 §5 product decomposition 升級到 Variant C：strand = knotted arc，不是 simple winding。

### 3.1 Initial Variant C Setup

**Picture upgrade**：每 strand = vertex 內嵌 knotted arc，3 layer winding：
1. Inter-strand mutual (B_3 braid)
2. Axial fiber 環繞
3. Intrinsic knot chirality

**Generation $n$** = knot complexity（不是純 axial winding）。
**u vs d** = mirror knot $K_u = K_d^*$。

### 3.2 C1 Numerical: $V_n$-Colored Jones

**$q_{\rm HFT}$ candidate**：$q = e^{i\pi/3}$ from dual CFT level（$SU(2)_4$ 與 $SU(3)_3$ 共享 $k+2 = k+3 = 6$）。

**Trefoil $3_1$ colored Jones at $q = e^{i\pi/3}$**：

公式：$\langle T(s,t), V_n \rangle = \sum_m S_{nm} \theta_m^{st}/S_{n0}$，$st = 6$。

代入：
| $V_n$ | $\langle 3_1, V_n \rangle$ |
|---|---|
| $V_1$ | $1$ |
| $V_2$ | $0$ |
| $V_3$ | $1$ |

Pattern $\{1, 0, 1\}$——bounded + zero。**結構性 fail**——modular tensor data at finite level 全部 bounded $\le \sqrt{3}$。

### 3.3 1-Knot Family Enumeration（Upgrade A: Hyperbolic Volume）

從 $B_3$ braid generators 直接 generate 1-component knot 序列：

| Sequence | 描述 | Result |
|---|---|---|
| A: $(\sigma_1\sigma_2^{-1})^{2n}$ closure | $4_1, 8_{12}, ...$ | 增量遞減（觀測加速）✗ |
| B: Torus $T(3,m)$ via $(\sigma_1\sigma_2)^m$ | $T(3,2)=3_1, T(3,4)=8_{19}, ...$ | Non-hyperbolic, V=0 ✗ |
| C: Pretzel $P(2n+1, 2n+1, 2n+1)$ | $P(3,3,3), P(5,5,5), ...$ | 增量過大（V $\sim 14, 23$）✗ |
| D: Twist knot $J(2,2n)$ | $4_1, 6_1, 8_1, ...$ | Volumes converge $\sim 4.06$ ✗ |

**所有 single-parameter $B_3$ 1-knot family fail**——沒有 family 能 reproduce 觀測 increment $\{3.00, 3.78\}$（加速比 1.26）。

### 3.4 1-Knot Picture Failure Diagnosis

觀測 Yukawa hierarchy 加速 ratio (20 → 44, factor 1.26 acceleration) 在標準 hyperbolic 1-knot 序列 **rare**——大部分 family volumes converge or grow linearly。

特殊 family 候選（augmented links / iterated cabling / Dehn surgery sequences）都 picture-external，HFT picture 內部沒有 natural 機制 select。

→ **Pivot 到 3-link picture (Resolution β)**：發現 $B_3$ closure 自然形式 ≠ 1-component knot。

---

## §4. 3-Link Picture (Resolution β) 推演

### 4.1 Pivot Motivation

$B_3$ closure 由 permutation 條件決定：
- Permutation = 3-cycle → 1-component knot
- Permutation = identity → **3-component link**

3-component link 對齊：
1. 3 strand 各自自我 close（Z_3 symmetry preserved）
2. Vertex = mesh junction：3 strand 是 separate 拓撲 object
3. **$B_3$ identity-permutation closure 是 picture-natural**

### 4.2 Iterated Borromean Family

**$(\sigma_1\sigma_2^{-1})^{3n}$ closure** for $n \ge 1$：permutation $(123)^{3n} = e$ → 3-component link：

| $n$ | Closure | Volume |
|---|---|---|
| 1 | Borromean rings $L_{6a4}$ | $7.32772$ |
| 2 | Iterated Borromean (n=2, 12 crossings) | $\sim 14$-$15$（待 calc）|
| 3 | Iterated Borromean (n=3, 18 crossings) | $\sim 22$（待 calc）|

**Volume 量級對齊**：
- $V_2 - V_1 \approx 7$ → $V_* \approx 2.33$
- $V_3 - V_2 \approx 7$ → $V_* \approx 1.85$

**量級數量正確**——3-link picture 比 1-knot 候選（全 fail）大幅 closer。$V_*$ 在 picture-natural 範圍 $\sim 2$。

### 4.3 Increment Acceleration Open Detail

觀測加速 ratio $1.26$（$\ln 44 / \ln 20 = 1.26$），iterated Borromean 線性增加（增量 $\approx$ constant per generation）——**acceleration 未自動 emerge**。

Two candidates（後被 β-2 取代）：

**β-1: Finite-$N$ correction**：
$$y^H(n) = C \cdot \exp(V(L_n)/V_*) \cdot [1 + a/N + b/N^2 + ...]$$

**β-2 (preliminary): CS-Volume Composite**：
$$y^H(n) \propto \exp(V(L_n)/V_*) \cdot e^{i\alpha \cdot CS(L_n)}$$

→ User 後續直覺 (Călugăreanu lock) 升級 β-2 為 picture-internal **Tw + Wr trade-off**，不需 CS invariant separate term，這是最終 Resolution β-2（見主 workdoc）。

---

## §5. Resolution β-2 Conceptual Lock 達成

User 直覺 lock：「strand 一邊 twist 一邊 writhe」+ Călugăreanu $Lk = Tw + Wr$ 守恆是 picture 真正 missing piece。

**Lk = n picture-internal lock**——把 (n, Tw) 兩量子數 reframe 為 (Lk, Tw partition)：down-type 全部 Wr complexity，up-type 帶一單位 Tw。

**Picture 完整 reduce**：
- Yukawa 5-order hierarchy ← Wr hyperbolic volume (volume conjecture)
- Increment acceleration ← satellite construction 內在 property
- Up/down asymmetry ← Tw vs Wr trade-off + alignment factor $\mathcal{T}$
- Top quark $y_t = 1$ ← $(n=3, Tw=+1)$ saturation lock
- 3 generations ← Lk ≤ 3 from $B_3$ closure ceiling

**詳細 final formula 與結論見** [Strong Sector Mass 總結 §6](Strong%20Sector%20Mass%20總結.md)。

---

## §5b. β-2 Numerical Lock Trial（2026-05-08）

C2β-2/C3β-2/C4β-2 numerical exploration——final results（sub-percent locks）寫進主 workdoc §6.7-6.10，這裡記嘗試的 candidate sequences。

### 5b.1 $V_*$ Candidates 嘗試

| Candidate | 值 | Test result |
|---|---|---|
| $V_{\rm cusp}$ | $1.0149$ | Increments 大（3.06, 3.83），but 對齊 1-knot 不成 |
| $V_{\rm cusp}/2 = \Lambda(\pi/3)$ | $0.5074$ | 接近 fit but 6% off |
| **$\pi/6$** | $0.5236$ | ✓ **0.6% match for $V_B - V_M$**——LOCK |
| $\pi/3$ | $1.0472$ | 過大 |
| $\Lambda(\pi/4)$ | $0.9160$ | 13% off |

最終 lock：$V_* = \pi/6$ from $SU(2)_4$ q-parameter $q = e^{i\pi/3}$ 半角度。

### 5b.2 $V_*^{\rm Tw}$ Candidates

從 $\mathcal{T}(+1, 3)/\mathcal{T}(+1, 2)$ ratio:

| Candidate | $V_*^{\rm Tw}$ | Predicted ratio | Off |
|---|---|---|---|
| $V_*$ | $0.524$ | $\exp(3) = 20$ | 200% off |
| $2 V_* = \pi/3$ | $1.047$ | $\exp(1.5) = 4.48$ | 35% off |
| $V_*\sqrt{2}$ | $0.741$ | $\exp(2.12) = 8.3$ | 21% off |
| **$\pi^2/12$** | $0.8225$ | $\exp(1.91) = 6.78$ | **1.3% off** ✓ |

Picture-natural lock：$V_*^{\rm Tw} = \pi^2/12 = (\pi/2) V_*$，dual CFT perpendicularity factor。

### 5b.3 Knot Family Identification Candidates

從 picture-corrected volumes（fitted $V_* = \pi/6$, anchored $V_{Wr=3} = V_{Borr}$）：
- $V_{Wr=2} = 5.350$（Magic 5.333, 0.3% match ✓）
- $V_{Wr=1} = 3.779$（Whitehead 3.664, 3.1% off）
- $V_{Wr=0} = ?$（unknot, V=0 hyperbolic）

**Whitehead → Magic → Borromean** 是 picture-natural identification:
- 結構：2-component → 3-component → 3-component
- Volumes 都是 $\Lambda(\pi/4)$ 與 $\Lambda(\pi/3)$ 倍數
- Gen 1 (Whitehead) 5% 偏離反映 2→3 component topology transition

### 5b.4 $\mathcal{T}_0$ Candidates

$\mathcal{T}_0 \approx 2.77$ from n=2,3 average:

| Candidate | 值 | Off |
|---|---|---|
| $e$ | $2.718$ | 2% |
| $\sqrt{2\pi}$ | $2.507$ | 11% |
| $\pi - 0.34$ | $2.80$ | 1% (no clean source) |
| $V_{Wr=1}/V_*$ | $7.21$ (no, off) | - |
| $\sqrt{V_*^{\rm Tw}/V_*} \cdot \pi/2$ | $1.97$ | off |

最佳 candidate $\mathcal{T}_0 = e$，picture interpretation 待。

### 5b.5 n=1 Anomaly Resolution Attempts

Wr=0 boundary 對齊 picture's natural pure-Tw mechanism：

| 嘗試 | Result |
|---|---|
| $\mathcal{T}(+1, 1) = \mathcal{T}_0 \exp(0/V_*^{\rm Tw}) = e$ | 240× off (vs 651) ✗ |
| $\mathcal{T}(+1, 1) = $ fitting parameter | bypasses picture |
| u quark in pure-Tw regime $y_u = e^{-\Delta E_{\rm Tw}/E_*}$ | picture 候選，待 derive |

n=1 留作 picture refinement——boundary regime structurally distinct。

---

## §5c. C6β-2 CKM Hopf Link Trial（2026-05-08）

C6β-2 numerical exploration——final results 寫進主 workdoc §7。

### 5c.1 $V_{\rm step}$ Candidates 嘗試

從 $|V_{us}| = \lambda$ 反推 $V_{\rm step}$：

| Candidate | $V_{\rm step}$ | Predicted $\lambda$ | Off |
|---|---|---|---|
| $\Lambda(\pi/3)$ | $0.507$ | $0.378$ | 68% off |
| $V_*$ | $0.524$ | $0.368$ | 64% off |
| **$\pi/4$** | $0.785$ | $0.223$ | **0.83% match** ✓ |
| $\pi/3$ | $1.047$ | $0.135$ | 40% off |

最終 lock：$V_{\rm step} = \pi/4$ = Whitehead/Borromean cusp angle，picture-natural identification。

### 5c.2 Wolfenstein $A$ Identification

$A = 0.826$。Picture candidates：

| Candidate | Value | Off |
|---|---|---|
| $\sqrt{\pi/4} = 0.886$ | $0.886$ | 7% off |
| **$\pi^2/12 = V_*^{\rm Tw}$** | $0.8225$ | **0.4% match** ✓ |
| $\sqrt{V_*^{\rm Tw}} = 0.907$ | $0.907$ | 10% off |
| $V_{\rm sat}^{\rm eff}/V_{Borr} \cdot 1/\ldots$ | various | none clean |

**Critical finding**：$A = V_*^{\rm Tw}$ 來自 **dual-source picture self-consistency**（C4β-2 ratio + C6β-2 CKM）。

### 5c.3 CP Violation $\bar\rho, \bar\eta$ 嘗試（C9β-2）

**$\bar\rho$ candidates**：

| Candidate | Value | Off |
|---|---|---|
| $\pi/20$ | $0.1571$ | 0.07% |
| **$1/(2\pi)$** | $0.1592$ | **1.4%** ✓ picture-natural |
| $1/6 = V_*/\pi$ | $0.1667$ | 6% |

選 $\bar\rho = 1/(2\pi)$（picture interpretation = inverse complete revolution）。$\pi/20$ 雖 sub-percent 但 picture interpretation 不清。

**$\bar\eta$ candidates**：

| Candidate | Value | Off |
|---|---|---|
| **$(\pi/2)\lambda$** | $0.3505$ | **0.4%** ✓ |
| $V_*^{\rm Tw} \lambda \cdot 2$ | $0.367$ | 5% |
| $\sin(\pi/9)$ | $0.342$ | 2% |

最終 lock：$\bar\eta = (\pi/2)\lambda$，$\pi/2$ 第三次出現（dual-CFT perpendicularity factor），triple-source verification with C4β-2 + C6β-2。

### 5c.4 Picture-Internal Hopf Link Identification

$d^{\rm pic}(i, j)$ 候選 form 嘗試：

| Form | Prediction | Issue |
|---|---|---|
| $(i-j)V_{\rm step}$ pure additive | works for 1↔2 | 2↔3 jump introduces $A$ |
| $V_{Wr}(\max) - V_{Wr}(\min)$ | gives some matches | 不對 t-d 等 |
| Hopf-link complement volume | conceptually correct | specific link 待 |

最終接受：$\lambda = e^{-3/2}$ + $A = \pi^2/12$ 兩 picture-internal lock 已 derive Wolfenstein 主 hierarchy，CP phase $\rho, \eta$ open。

---

## §5d. F5 $B_3$ Braid Word Algorithm Attempt（2026-05-08）

charm/bottom vertex coupling 從 picture-internal $B_3$ minimum braid word 嘗試 derive。

### 5d.1 Setup

Vertex configuration = $B_3$ braid word closure。Minimum braid word $|w|_{\rm min}$ 對應「3 strand 在 vertex 中的 minimum crossing 數」。

$$E_{B_3} = E_*^{\rm braid} \cdot |w|_{\rm min}$$

### 5d.2 候選 $|w|$ Formula 嘗試

**Ansatz A：Pair-wise additive (homochiral n-mismatch + Tw cross)**：

$$|w|_{ij} = |n_i - n_j| + \text{Tw}_i n_j + \text{Tw}_j n_i$$

| Baryon | $(n_i, Tw_i)$ | $|w|_{\rm min}$ |
|---|---|---|
| Λ | (1,+1), (1,0), (2,0) | $5$ |
| Λ_c | (1,+1), (1,0), (2,+1) | $7$ |
| Λ_b | (1,+1), (1,0), (3,0) | $8$ |

從 $\Delta E^{\rm phen}$ 反推 $E_*^{\rm braid}$：

| Transition | Δ\|w\| | $\Delta E^{\rm phen}$ (MeV) | $E_*^{\rm braid}$ |
|---|---|---|---|
| Λ → Λ_c | 2 | $+302$ | $151$ |
| Λ → Λ_b | 3 | $+396$ | $132$ |
| Λ_c → Λ_b | 1 | $+94$ | $94$ |

**$E_*^{\rm braid}$ 不一致**（94-151 MeV），ansatz A fails consistency check。

**Ansatz B (multiplicative)** $|w| = (n_i + n_j - 2)(1 + Tw_i + Tw_j)$：複雜度爆炸，未 fit。

### 5d.3 候選 $E_*^{\rm braid}$ Picture Identification

平均 ~125 MeV 的 candidates：

| Candidate | Value | Off |
|---|---|---|
| $\Lambda_{\rm QCD}/\pi$ | $142$ | 13% |
| $\sqrt{2CT_0}/4$ | $125$ | match avg |
| $\Lambda_{\rm QCD}\cdot 5/16$ | $139$ | 11% |

**沒有清楚 picture-natural 識別**。

### 5d.4 Failure Mode 診斷

Pair-wise additive $|w|$ 結構性不足以 capture：
1. **Triplet Yang-Baxter constraint** 引入 collective term（不只 pair-wise sum）
2. **Tw scaling 與 n scaling 不對稱**——Tw 走 sub-fiber 方向，n 走 axial，cross-coupling 應有 metric tensor 而非 simple multiplicative
3. **Constituent mass 已含部分 vertex effect**——phenomenological residue 不純是 $E_{B_3}$

### 5d.5 Picture Building Block Status

✓ $B_3$ braid 結構在 vertex 存在（from anyon framework §2.1）
✓ Minimum word concept + energy form $E_{B_3} = E_*^{\rm braid} |w|$
✗ 具體 $|w|$ formula：**non-trivial Yang-Baxter solving 待**
✗ $E_*^{\rm braid}$ identification：picture-natural candidates 13% off

**結論**：$B_3$ braid algorithm 比預想複雜——pair-wise ansatz 不夠，需完整 representation theory + Yang-Baxter solving。**Framework 仍 valid，但 sub-percent lock 待後續 picture-internal work**。

對 strong sector，charm/bottom vertex coupling 在當前 picture 留作 framework-level 而非 numerical lock。

---

## §5e. $E_*$ Scaling with $\{n_i\}$ Verification（2026-05-08）

從 §9a vertical channel formula $\Delta E = (h_3 - h_1) E_* = E_*/2$ 反推，驗證 $E_*$ 隨 $\{n_i\}$ 是否符合 picture-internal scaling 猜想。

### 5e.1 Observed $E_*$ from Spin Splits

| Family | $(n_1, n_2, n_3)$ | $\Delta E$ obs | $E_*$ implied |
|---|---|---|---|
| Δ - p | (1,1,1) | 294 | 588 |
| Σ* - Σ | (1,1,2) | 191 | 382 |
| Ξ* - Ξ | (1,2,2) | 215 | 430 |

**$E_*$ 非單調 Δ → Σ → Ξ**：588 → 382 → 430。

### 5e.2 Simple Scaling Ansätze 全部 fail

| Ansatz | Σ match | Ξ match |
|---|---|---|
| $1/\langle m\rangle$ | 28% off | 4% |
| $1/\langle m\rangle^2$ | 5% | 32% off |
| $1/\sum m^2$ | **1%** ⭐ | 35% off |
| $1/(m_u m_s)$ pair-wise | 6% | 16% off |
| $1/m_{\rm singular}$ | 6% | 37% off |
| $1/\sum m$ | 26% off | 4% |

**Pattern**：fits Σ* 的 ansatz 不 fit Ξ*，反之亦然。沒有 single simple scaling 同時 work。

### 5e.3 Verdict

✓ **Direction confirmed**：heavier strand → smaller spin split
✓ **Δ-p anchor lock**：$E_*(1,1,1) = (4/3)\Lambda_{\rm QCD}$（1.2% match）
✗ **Specific functional form**：no clean picture-internal $f(\{n_i\})$ 同時 reproduce 三個 splits

### 5e.4 與 §5d 的 Coupling Insight

User 觀察：$B_3$ braid coupling (§5d) 與 $E_*$ scaling 是 **picture-internally coupled**——共享同一 modular tensor category data。

**Picture-internal source**：

$$\Delta E_{\rm vertex}(\{n_i, Tw_i\}, J) = E_*^{(0)} \cdot \mathcal{F}_{B_3}(\{V_{n_i}\}, h_m, F\text{-symbols}, R\text{-matrix})$$

| Picture-internal data | 來源 |
|---|---|
| $V_n$ reps + $h_n$ | §2.1, §2.2 既有 |
| R-matrix phases | §2.3 既有 |
| F-symbols（associator）| 需 explicit derive from $SU(2)_4$ at $j_{\rm max}=3/2$ truncation |

**統一機制**：
- $E_*$ scaling = F-symbol pathway 從 $V_1$ ground 到 $V_3$ excited 在 mixed-rep fusion space
- $B_3$ braid coupling = $\sigma_1, \sigma_2$ 矩陣元 在同一 fusion space
- 兩者 **same data, different manifestations**

**Status**：framework articulated，explicit F-symbol calculation 為下層 picture work。一旦 F-symbol explicit derive，$B_3$ braid 與 $E_*$ scaling **simultaneously locked**——picture-internal sub-mechanism unification。

### 5e.5 Why F-Symbol Calculation 是 Hard

$SU(2)_4$ at $j_{\rm max}=3/2$ truncation 的 F-symbols 是 6j-symbols 的 quantum 變種。Closed-form 表達式 known，但 evaluation at root-of-unity $q = e^{i\pi/3}$ 需要 careful regularization。

完整計算 ≈ modular tensor category 數值表 generation。Picture-internal but **non-trivial sub-mechanism**——超出當前 strong sector 階段。

留作後續 picture work（possibly Paper 2 or follow-up paper material）。

---

## §5f. F-Symbol Calculation 揭示 §9a Vertical Channel 的 Conceptual Gap（2026-05-08）

嘗試 F-symbol explicit calculation 為 $B_3$ braid + $E_*$ scaling 統一 lock，過程中揭示 §9a 「vertical channel = baryon J」identification 的 conceptual gap。

### 5f.1 F-Matrix Setup

對 $SU(2)_4$ at $j_{\rm max}=3/2$，$q = e^{i\pi/6}$，q-integers $[2]_q = \sqrt{3}, [3]_q = 2$。

**Δ-p baseline F-matrix** ($V_1^3 \to V_1$)：

$$F^{1/2,1/2,1/2}_{1/2} = \frac{1}{\sqrt{3}}\begin{pmatrix} 1 & \sqrt{2} \\ \sqrt{2} & -1 \end{pmatrix}$$

eigenvalues $\pm 1$。Structure OK for all-n=1。

### 5f.2 Mixed-n Inconsistency

對 Σ-type baryon (uds with sym ud, J=1/2) vertical fusion $V_1 \otimes V_1 \otimes V_2$：

$$V_1^2 V_2 = V_0 \oplus 2 V_2$$

**Decomposition 不含 $V_1$ 或 $V_3$**——但物理 Σ (J=1/2) 與 Σ* (J=3/2) 對應 V_1 與 V_3 in §9a identification。

**矛盾**：fusion 結果中沒有 V_1 或 V_3 channel，無法直接 identify Σ/Σ* 與 vertical channel。

### 5f.3 Picture Conceptual Issue

**For all-n=1**：strand topological winding $V_n=1$ 與物理 spin $j=1/2$ **巧合相同**（$V_1$ rep 的 spin = 1/2）。$V_1^3 = 2V_1 \oplus V_3$ trivially 對應 octet J=1/2 + decuplet J=3/2。

**For mixed-n**：$V_2$ 在 SU(2)_4 vertical 對應 $j_{\rm topology} = 1$（spin-1 rep），但 s quark 物理 spin = 1/2。**Vertical $j_{\rm topology}$ ≠ 物理 spin**——「V_n vertical = baryon J」identification break down。

### 5f.4 §9a #15 Lock Status Reassessment

| Lock | Original claim | Revised status |
|---|---|---|
| #15 p-Δ split via vertical channel | Picture-internal lock (1.2%) | ⚠ All-n=1 special case；mixed-n 不適用 |

Formula $\Delta E = (h_3 - h_1) E_*$ with $E_* = (4/3)\Lambda_{\rm QCD}$ 在 Δ-p 給 1.2% match，但這是因 V_n=1 = j=1/2 的特殊巧合——**不是 general picture-internal vertex coupling 機制**。

Mixed-n baryons 的 spin 來源需要 picture refinement：spin 可能來自 horizontal SU(3)_3 + spin-flavor SU(6) emergence，而非 vertical SU(2)_4 fusion。

### 5f.5 Picture Refinement Direction

兩個 candidate refinements：

**Option A**：$V_n$ vertical = 純 topology label (strand winding)，不直接 carry spin。物理 baryon spin from 獨立 spin-flavor wavefunction。
→ §9a 的 Δ-p formula 是 emergent coincidence，需另構機制 explain Σ*-Σ, Ξ*-Ξ。

**Option B**：$V_n$ vertical 含 effective spin 信息但 mixed-n 有 non-trivial cross-coupling。需要 picture-level upgrade articulate「mixed-rep spin emergence」。

### 5f.6 5-Source Verification 不受影響

重要：**$V_* = \pi/6$ 的 5-source verification 仍 holds**——因為 5 sources 都不依賴 vertical channel formula：
- $y_b/y_s$ (C3β-2): Yukawa hierarchy from Wr volume
- $V_*^{\rm Tw}/V_* = \pi/2$ (C4β-2): Tw alignment
- CKM A (C6β-2): Hopf link evaluation
- CP $\bar\eta$ (C9β-2): perpendicular phase
- Λ/Σ split (C10β-2): horizontal SU(3)_3 fusion

只有 #15 (vertical channel for spin split) 受影響。

### 5f.7 F-Symbol Calculation 暫停

繼續 F-symbol explicit calculation 需要先 picture refine spin-V_n 關係，否則計算得到的 F-matrix 物理意義不清楚。**留作後續 picture work**。

---

## §5g. Wr-Tw Rebalance Dynamics（Picture Refinement, DeepThinker Mode B Output, 2026-05-08）

§5f F-symbol exploration 揭示「V_n vertical = baryon J」identification break for mixed-n。DeepThinker mode B 收斂 picture refinement：

### 5g.1 Picture Refinement

| Element | 角色 |
|---|---|
| $V_n$ vertical | Pure topological label（NOT physical spin）|
| Strand spin | Independent spin-1/2 quantum number (kinematic) |
| Spin axis | Strand 主要 winding direction：Wr for Tw=0 strands; Tw for Tw=+1 strands |
| Spin coupling | Vertex 內 strand spin orientations 之間的 elastic energy |

每 strand 攜 spin-1/2 explicit，與 $V_n$ topology 分離。Baryon spin from standard SU(2)⊗SU(2)⊗SU(2) coupling。

### 5g.2 Spin Promotion Mechanism: Wr-Tw Rebalance

Spin promotion (J=1/2 → J=3/2) → 1+ strand spin reorientation → strand 經歷 Wr-Tw rebalance under Călugăreanu $Lk = Tw + Wr$ constraint。

**Per-strand vertex Hamiltonian**：

$$H_i = \frac{1}{2} A \omega_{Wr,i}^2 + \frac{1}{2} C \omega_{Tw,i}^2$$

with $\omega_{Tw,i} + \omega_{Wr,i} = 0$（Lk constraint per strand）。

Reorientation 經 vertex elastic constants $A, C$ propagation。

### 5g.3 Leading-Order Result: CQM-Equivalent

從 V1 lock $E_i^* = n_i\sqrt{2CT_0}$ + $\bar L_{ij}^2 \propto m_i m_j$（strand extent 從 mass scaling）：

$$\Delta E_{\rm spin\,promotion} \propto \sum_{i<j} \frac{\Delta\langle S_i \cdot S_j \rangle}{m_i m_j}$$

**Picture-internal derive CQM hyperfine pair-wise structure**——不是經驗 input。

### 5g.4 Test on Spin Splits

CQM-equivalent ratios:
- $\Delta E_{\Sigma^*-\Sigma}/\Delta E_{\Delta-p} = m_u/m_s = 0.612$
- $\Delta E_{\Xi^*-\Xi}/\Delta E_{\Delta-p} = m_u/m_s = 0.612$ (same as Σ at leading order)

Predicted: Δ-p = 294, Σ*-Σ = 180, Ξ*-Ξ = 180.
Observed: 294, 191, 215.

**6% match Σ, 16% off Ξ**——leading-order picture-internal 預測 Σ ≈ Ξ，與觀測 12% 差異不一致。

### 5g.5 Sub-Leading Corrections（Open）

觀測 Σ*-Σ ≠ Ξ*-Ξ 來自：
- SU(3) flavor breaking
- Wr distribution heterogeneity (Σ has Wr=(0,0,2); Ξ has Wr=(0,2,2))
- Z_3 vertex symmetry breaking under mixed-flavor configuration
- Sub-fiber alignment differences

Picture-internal sub-leading correction 公式待 explicit calc with Wr distribution + Călugăreanu propagation。

### 5g.6 Specific Coefficient $c$ Identification

$\Delta E_{\Delta-p} = c \cdot 3/(2 m_u^2) = 294$ MeV → $c = 1.91 \times 10^7$ MeV³

Picture-natural candidates not obviously clean. Possibly involves $\Lambda_{\rm QCD}$, $\sqrt{2CT_0}$, $V_*, V_*^{\rm Tw}$ combination 待 detailed dimensional analysis from Wr-Tw rebalance dynamics。

### 5g.7 Status

✓ **Framework articulated**: Wr-Tw rebalance mechanism clear, V_n = topology only confirmed
✓ **Leading-order picture-internal result**: CQM hyperfine pair-wise structure $\propto 1/(m_i m_j)$ derive from picture (not empirical)
✗ **Specific coefficient $c$ identification**: picture-natural value 待
✗ **SU(3) breaking** (Σ vs Ξ split difference): sub-leading picture-internal calc 待

Picture refinement key point: $V_n$ vertical 與 strand spin **decoupled**——這是 DeepThinker mode B 解決 §5f conceptual gap 的核心 insight。

---

## §6. 學到的 Picture-Level Lessons

1. **Single modular tensor data candidates 結構性 bounded**——任何 SU(2)_k at finite level 給的 invariant 都 $\le O(\varphi)$，無法 span 5 orders Yukawa
2. **Multiplicative product structure 必要**——vertical × horizontal CFT decomposition 是 picture-level breakthrough
3. **1-knot picture 不夠 picture-symmetric**——強迫 3 strand fuse 成 single knot 違反 vertex Z_3 symmetry
4. **Hyperbolic volume 是真正的 multiplicative source**——via volume conjecture，picture-internal motivated
5. **$B_3$ braid algorithm 比 simple ansatz 複雜**——pair-wise additive 失敗，需要 Yang-Baxter constrained collective formula
6. **Phenomenological regularities ≠ picture lock**——$\Delta E_{\rm vertex}$ 反推的 linear pattern 是「湊數字」不該寫進主 workdoc
7. **$B_3$ braid + $E_*$ scaling 是 coupled sub-mechanisms**——共享 same modular tensor category data；F-symbol explicit derivation 會 simultaneously lock 兩者；picture-internal 統一機制存在但需要 non-trivial 計算
8. **F-symbol explicit calculation 揭示 §9a vertical channel identification 是 all-n=1 巧合**——「V_n vertical = baryon J」對 mixed-n 不成立；mixed-n baryon 的 spin 來源需要 picture refinement
9. **DeepThinker Mode B 解決 §5f conceptual gap**：$V_n$ vertical = pure topology 與 strand spin (independent quantum number) decouple；spin promotion energy 從 Wr-Tw rebalance under Călugăreanu $Lk$ constraint 給 leading-order CQM-equivalent $1/(m_i m_j)$ pair-wise（picture-internal derive 而非經驗）；sub-leading SU(3) breaking 待 detailed elastic + Călugăreanu calc
5. **Călugăreanu 守恆是統一 lock**——把分散的 quantum number、charge、mass 機制 reduce 到單一拓撲守恆
