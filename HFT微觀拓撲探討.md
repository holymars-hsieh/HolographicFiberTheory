# HFT 微觀拓撲探討

**用途**：HFT 微觀拓撲層的完整 picture——整合 EWSB 動力學、四力幾何起源、SM 粒子完整 sector、暗物質與宇宙學 cascade 於同一 mesh + Hopf bundle 結構
**對應**：v13 主論文已上 Zenodo（2026-05-05）、Candidate Y 已投 FoP（2026-05-03），兩者皆不依賴本文件 micro picture——本文件是 macro 預測下的 deeper instantiation
**關聯**：
- Macro/micro Gauss-Bonnet duality 見 [`工作文件_作用量vs能量_macro_micro.md`](工作文件_作用量vs能量_macro_micro.md)
- Baryon mass 量化變分框架見 [`從拓撲結構變分求解重子質量.md`](從拓撲結構變分求解重子質量.md)（F4/F5/F6 量化任務具體執行入口）

---

## §0. 概述

HFT 的微觀拓撲層在 trivalent $S^2$ mesh + Hopf $S^1$ bundle 結構下統合**整個 SM + 暗物質 + 重力**：

**核心結構**：
- 每 edge 上**兩條 identical fiber strands**穿越 vertex（不在 vertex 終止）
- Vertex 是 6-strand re-pairing $B_3$ braid，中心 $Z_3 \equiv C_3$
- 每 vertex 有一根**垂直穿過 $S^2$ 的 $S^1$ axial fiber**（中心旋轉軸，攜 lepton sector）
- Vertex Wr **雙重量子化**：accumulation $360°$（vertex-level），dispersion $120°$/fiber（fiber-level，$Z_3$ 配額）
- 全空間 chirality 鎖在 **vertex W(1) Wr 旋轉方向**（CW/CCW），edge 本身無 chirality 自由度

**四 cohomology 對應四力**：

| Cohomology | 力 | 性質 |
|---|---|---|
| $H^0$ Vacuum | Gravity | substrate 橫波 |
| $H^1$ Twist | EM | vertex 垂直軸 fiber holonomy |
| $H^1 \to H^2$ boundary | Weak | $\text{Tw} \to Wr$ 轉換阻力 |
| $H^3$ Link | Strong | $B_3$ vertex braid 離散構型 gauge description（HFT 不需 gluons）|

**SM 粒子各 sector 拓撲位置完全分離**：

| 粒子 | 拓撲位置 | Charge | Mass |
|---|---|---|---|
| ν | sub-fiber Tw_L 殘餘（無垂直軸 winding）| $0$ | meV |
| ℓ | vertex 垂直軸 full fiber | $\pm 1$（integer winding）| MeV–GeV（Higgs-like）|
| q | edge 上單一 strand | $\pm 1/3, \pm 2/3$（sub-fiber + $Z_3$ 配額）| MeV–GeV（current + constituent）|
| Baryon | 3 strands at vertex 形成 $B_3$ closed braid | integer | $\sum T_{\rm strand}$（$B_3$ braid elastic）|
| Meson | 單 strand 連 2 vertices | q + q̄ | strand 兩端 elastic tension |
| W/Z | $\text{Tw} \to Wr$ boundary process | W± charged | 2 Nyquist slots cost |
| W(1) DM | vertex 360° Wr + 3-fiber 120° dressing | $0$ | 5.08 GeV |

**EWSB 真空殘餘三框架同構**：

$$\boxed{\;\delta S_E \;=\; N_{\rm rep} \times \frac{N_{\mathbb{Z}_2\text{-cost}}}{N_{\rm Ny}} \;=\; 10 \times \frac{2}{128} \;=\; \frac{10}{64} \;=\; 0.15625\;}$$

對 v13 macro $8/S_E = 0.15573$：0.34% 內，差距由 $D(t_0)$ stretch 完全吸收（sin² 空間僅 +0.023% dressing）。三框架（A: sin²-space rational, B: Gauss-Bonnet, C: macro $Z_2$）獨立 derive 收斂同一恆等式。

**EWSB = 全域 chirality lock + 張力連通激活**——pre-EWSB vertex W(1) handedness + edge Tw sign 各自 50/50 隨機；bubble nucleation 透過**單一全域 chirality choice 同時鎖定**兩者為 coherent baseline，並激活 mesh-wide 張力連通——這個張力連通**就是** HFT 「Higgs vev」具體身分。

---

## §1. v13 既定拓撲輸入

| 量 | 來源 | 數值 |
|---|---|---|
| 全息 Nyquist 預算 $N_{\rm Ny}$ | $2^3 (T^1S^2) \times 2^2 (\text{Tension/Phase}) \times 4 (\text{Cohomology})$ | $128$ |
| 整體骨架 $N_{\rm skel}$ | $N_{\rm Ny} + N_v^2 = 128 + 9$ | $137$ |
| Frozen knot classes $N_v^2$ | $\binom{k+2}{2} - 1$（$SU(3)_3$ 非真空可積表示）| $9$ |
| 整 $SU(3)_3$ 可積表示 $N_{\rm rep}$ | $\binom{k+2}{2}$（含真空 $(0,0)$）| $10$ |
| $\sin^2\theta_W\big|_{\rm GUT}$ | $N_w/N_{\rm Ny} = 30/128$ | $15/64$ |
| 手性投影 $\sin^2\theta_W\big|_{\rm GUT}$（投影因子）| $3/8$（v13 §4.2）| $0.375$ |
| EWSB 動作預算 $S_E$ | $N_{\rm skel} \times 3/8 = 137 \times 3/8$ | $51.375$ |
| $S^2$ structural substrate（W(0)）| $N_{\rm skel} \times 5/8 = 137 \times 5/8$ | $85.625$ |
| 4 上同調類 | $H^0$ Vacuum, $H^1$ Twist, $H^2$ Writhe, $H^3$ Link | 拓撲嚴格正交 |

**Action partition**：$N_{\rm skel} = 137 = S_E + (N_{\rm skel} - S_E) = 51.375 + 85.625$。前者是 EWSB-active budget（visible 8 + dark 43.375），後者是 W(0) $S^2$ structural substrate（不參與 EWSB redistribution）。

---

## §2. 兩個本體論承諾

### 2.1 Action-Information Equivalence

$$N_{\rm nodes,eff} \;\equiv\; S_E$$

$S_E$ 精確等於「參與 EWSB 手性鎖定的有效網格節點數」，不是 ad hoc 歸一化。**廣義承諾**：所有 HFT 量最終 reducible 到節點計數——這是 HFT 與標準 QFT 連續積分本體論的根本差異。

具體 implication：mesh 多繞一圈所需的「額外 action」就是它在 128 Nyquist slots 中佔用的額外資訊空間——直接決定 W(2) mass scale = $128 \times M_{W^{(1)}}$（§9.5）。

### 2.2 真空態 $(0,0)$ 的 Dual Role

| 過程 | 物理性質 | 真空態角色 | Counting |
|---|---|---|---|
| $\delta S_E$ accounting | 全域相變 | 基態配置；網格傾斜時也承受偏離 | $N_{\rm rep} = 10$（含真空）|
| $\alpha^{-1}$ running | 局部拓撲激發（knot melting）| 背景 Nyquist 海洋本身；無法融化回背景 | $N_v^2 = 9$（不含真空）|

> 全域形變中真空是參與者；局部激發中真空是背景。

### 2.3 Fiber 自由度修正：$\rho$ = Tension Scalar，非徑向振幅（2026-05-07）

**v13 早期定義誤導**：把 $S^1$ fiber 的「振幅自由度」$\rho$ 描述為**徑向延伸**（fiber 像有截面寬度的 tube），這個 visual analogy 與 picture 後期發展不一致。

**修正版 ontology**：$\rho$ 是 **fiber 沿軸 tension scalar**（局部張力密度），與 $T_0 = \Lambda_{\rm QCD}^2$ vacuum baseline 同 entity。$S^1$ fiber 是純圓拓撲，**沒有徑向自由度**——所有 DOFs 都是縱向的：

| Wave / DOF | 載體 | HFT manifestation |
|---|---|---|
| Phase 縱波 $\partial_s\theta$ | $S^1$ fiber phase 沿軸梯度 | 光子（$H^1$ Tw）|
| Tension 縱波 $\partial_s\rho$ | $S^1$ fiber tension 沿軸梯度 | 局部質量 / inertia 密度變化 |
| Stress 縱波 $\partial_x T$ | $S^2$ mesh tension 沿基底梯度 | 引力波 / Higgs 呼吸（$H^0$ stress）|

**Q5 Nyquist counting 不變**：5D 相空間 = 2 ($S^2$ base) + 1 ($S^1$ phase $\theta$) + 1 ($S^1$ tension $\rho$) + 1 (時間 / 沿軸位置)；$128 = 2^3 \times 2^2 \times 4$ binarization 結構保留，只是「Amp/Phase」factor 重命名為「Tension/Phase」。

**「橫波」是 emergent**：標準觀測中光子横波偏振 + 引力波 TT mode 是 fiber/mesh **在 3D 空間中方向投影**的衍生性質，非 fundamental 徑向振動。

→ 與 §3.0.8 discrete slot picture 完全自洽：$\theta$ 量子化為 integer winding $n$，$\rho$ 量子化為 integer Wr quantum + $T_0$ baseline，兩者都離散都縱向。

---

## §3. Mesh 微觀結構

### 3.0 Vacuum 基態 + 手性鎖定（lock 2026-05-07）

#### 3.0.1 為什麼 vacuum 必有 Tw/Wr 分布（非 Lk=0 trivial）

Hopf bundle 非平凡性 $\pi_3(S^2) = \mathbb{Z}$ 強制全域 fiber linking 非零。Lk=0 平行 vacuum 與 Hopf 全域拓撲不相容——「結構作用量」必須有微觀 anchor。系統最低能態：把全域拓撲必要的 $N_{\rm Hopf}$ winding **按彈性平衡分散到 edges 與 vertices**。

#### 3.0.2 Vacuum Baseline 變分鎖定

設 $V$ 個 vertices, $E = 3V/2$ 個 edges（trivalent）。Vacuum 每 edge 攜 Tw $t_0$，每 vertex 攜 Wr $w_0$。

**約束 + 變分平衡**：

$$\frac{3V}{2} t_0 + V w_0 = N_{\rm Hopf}, \quad \frac{Ct_0}{L_e} = \frac{Aw_0}{L_v} \;\Rightarrow\; \frac{t_0}{w_0} = \frac{A}{C} \cdot \frac{L_e}{L_v}$$

**$N_{\rm Hopf} = V$（per-vertex Hopf invariant）**：每 vertex 攜垂直軸 $S^1$ fiber → 一個 Hopf base point → 1 unit Hopf invariant。排除 $N_{\rm Hopf} = 1$（無微觀 anchor）、$E = 3V/2$（edge 無 Hopf base point 結構）、$\{10, 128, 137\}$（non-extensive 違反 mesh scaling）。

**$L_e/L_v = 2/3$（discrete slot exclusion）**：strand 在 vertex 內 6-strand $B_3$ re-pairing 受**離散 slot 計數約束**——兩 strand 不能同時佔用同一最小 spatial slot（等同 §3.11 anyonic statistics）。Vertex 由 $Z_3$ 分 3 sectors，每 sector minimum braid step = half-edge slot $a/2$ → $\ell_{\rm braid} = 3 \times (a/2) = 3a/2$。代入 $L_e^{\rm strand} = a$, $L_v^{\rm strand} = 3a/2$ 得 $L_e/L_v = 2/3$（4-segment partition 推導見 §3.0.4）。

**Lock 結果**（$A:C = 5:3$ × $L_e/L_v = 2/3$）：

$$\boxed{w_0 = \frac{3}{8}, \quad t_0 = \frac{5}{12}, \quad \frac{3}{2}t_0 = \frac{5}{8} = \cos^2\theta_W, \quad w_0 = \frac{3}{8} = \sin^2\theta_W}$$

**Per-vertex region shares 精準對齊 EWSB tilt 分數**——sharp lock 強驗證整套 derivation。

#### 3.0.3 $A:C = 5:3$ 在 Picture 中雙層 Carry

| 層級 | 角色 |
|---|---|
| **Elastic constants $A:C$** | 控制所有激發態能量（K meson, W(1), proton, baryon zoo）；V1 雙重 1% 驗證（W(1) 0.7%, K meson 0.2%）anchor |
| **Vacuum baseline shares** $\{(3/2)t_0, w_0\} = \{5/8, 3/8\}$ | 由 $A:C \times L_e/L_v$ 共同 lock，控制 vacuum 拓撲分布 |

兩層級 sharp 對齊**非 redundancy 而是 self-consistency check**——EWSB tilt 結構在 elastic 動力學 + vacuum 拓撲分布雙重 manifest。

#### 3.0.4 $L_e, L_v$ 幾何定義 + 4-Segment Partition

每 edge 物理長度 $a$，strand 沿弧長分區（連續性原則：strand 是穿過 vertex 連到每 edge 的整條不可分曲線）：

$$\underbrace{\ell_{\rm app}}_{\to L_v} \;-\; \underbrace{\ell_{\rm twist}}_{\to L_e} \;-\; \underbrace{\ell_{\rm twist}}_{\to L_e} \;-\; \underbrace{\ell_{\rm app}}_{\to L_v}$$

每 strand 通過 vertex 只進兩條 edges（in + out），單次 transit：

$$L_e^{\rm strand} = 2\ell_{\rm twist}, \quad L_v^{\rm strand} = 2\ell_{\rm app} + \ell_{\rm braid}$$

$\ell_{\rm app} \to 0$（discrete picture：strand 從 edge twist mode 直接進入 vertex braid mode，無連續 approach 過渡）→ $L_e = a$, $L_v = \ell_{\rm braid} = 3a/2$。

#### 3.0.5 全域 Chirality Lock + 激發態公式

**Pre-EWSB**：vertex W(1) handedness + edge Tw sign 各自 50/50 隨機，**未相關聯**。

**EWSB chirality lock = 全域 complexity 簡化**：單一 chirality choice 同時鎖 vertex W(1) Wr 方向 (CW/CCW) + edge Tw 符號 ($\pm$) 為 coherent baseline。「左手性 $S^2$ 網路」= 兩者 alignment 的同一 choice 雙重表現。

**激發態（粒子）= vacuum baseline 上整數偏離**：

$$M_{\rm hadron} = \sqrt{2CT_0} \cdot |\Delta\text{Lk}|$$

vacuum baseline 是 universal subtracted quantity——K meson $|\Delta\text{Lk}|=1$ → 498.6 MeV vs 觀測 497.6 MeV (0.2% match) 保留。

#### 3.0.6 HFT 連續/離散框架同一性

- $L_e, L_v$ 弧長 + Kirchhoff 變分能量 = **連續積分形式**
- 底層 substrate = N_Ny = 128 + Z_3 sub-cell **離散 slots**
- $\ell_{\rm braid} = 3 \times (a/2)$ = 整數 × slot scale，不是任意實數
- **連續工具是離散 substrate 的計算 wrapper**，picture 本體論優先離散

### 3.1 Edge Fiber Pair + $\mathbb{Z}_2$ 手性對稱

每 edge 上**兩條 identical $S^1$ fiber strands**穿越 vertex（不在 vertex 終止）。Vacuum 已是 coherent 雙絞 baseline ($t_0 = 5/12$) — 由 vertex W(1) Wr 全域 alignment 派生 winding direction（§3.0）。

HFT chirality $\mathbb{Z}_2$ 對稱**作用於 vertex W(1) Wr 旋轉方向**（CW $\leftrightarrow$ CCW），edge 本身**無 $\mathbb{Z}_2$ 自由度**——$B_2$ 中心 $\mathbb{Z}_2$ 在激發態對應 winding sign flip ($\text{Lk} \to -\text{Lk}$) 是 vertex W(1) handedness 的派生量。

### 3.3 Vertex $B_3$ Braid 與 Strand Re-pairing

3 條同手性雙股 fibers 進入 vertex → **6 strands 在 vertex 區域 re-pair**：

- 每條入射 fiber 兩股**在 vertex 處分離**：一股沿 $+120°$ 出射、另一股沿 $-120°$
- 每條出射 edge 接收兩股（來自相鄰兩條入射 fiber）
- 出射兩股自然 re-braid 為新的同手性雙股 fiber

| 尺度 | 結構 |
|---|---|
| Fiber 內部（沿 edge）| $B_2$ 同手性雙絞 |
| Vertex 區域 | $B_3$ braid（6 strands spatial braiding）|
| Vertex 中心對稱 | $Z_3 \equiv C_3 \equiv B_3$ 中心 |

### 3.4 Vertex 垂直軸 Fiber

每 vertex 有一根**Hopf bundle 在 vertex base point 上的 $S^1$ fiber**——vertex 中心旋轉軸。這是 Hopf bundle 在 mesh 幾何中的 manifestation。

| Fiber 類型 | Bundle 方向 | 攜帶 |
|---|---|---|
| Edge fiber（horizontal）| 沿 $S^2$ 切線 | sub-fiber 級 Tw（quark sector）|
| Vertex axial fiber（"vertical"）| Hopf-fiber 維度（**非 spatial 第三軸**）| full-fiber 級 Tw（lepton sector）|

**重要 ontological caveat（2026-05-08）**：「垂直」指 Hopf bundle 的 fiber 維度，**不代表 spatial 第三維度**。Anyonic B_3 braid 在 vertex 局部是 2+1D（spatial S² + temporal）而非 3D spatial——「strand 上下關係」是時間 ordering 的 topological class。Picture 與 holographic principle 完全 compatible，詳見 [HFT Anyon Framework §0.7](HFT%20Anyon%20Framework_Vn%20R-Matrix%20與%20Braid%20Word.md)。

3 條 horizontal edges 圍繞 vertex base point 對稱排列——**正是因為 Hopf fiber 提供結構錨點**，anyonic braiding 才能在 vertex 穩定形成 trivalent junction。

**Pre-EWSB / Post-EWSB 差別**：

| 階段 | 垂直軸狀態 | 與 horizontal mesh 耦合 |
|---|---|---|
| Pre-EWSB（低張力）| 存在但獨立 | decoupled——無應力傳遞 |
| Post-EWSB（高張力）| 同樣存在，**mesh 整體被「拉緊」** | coupled——應力互相傳遞 |

EWSB 不只完成 chirality lock，還**激活整個 mesh 的張力連通性**——所有結構元件作為 coupled mechanical system 互相應力傳遞。這個 mesh-wide 張力連通**就是** HFT 的「Higgs vev」具體身分。

### 3.5 Wr 雙重量子化

Vertex Wr 有兩個量子單位在**不同拓撲層級**：

| 過程 | 量子 | 層級 | 物理 |
|---|---|---|---|
| **Accumulation**（vertex localized excess Wr）| $360°$（1 整圈）| Vertex-level | 多繞 1 整圈 sub-fiber routing 守恆 |
| **Dispersion**（unwind 釋放到 fiber）| $120°$/fiber | Fiber-level | $Z_3$ 強迫 3 fiber 等量分擔 |

**為什麼 vertex Wr 必須整 turn**：

- $120°$ / $240°$ rotation 改變 sub-fiber 出射方向 → 與其他 vertex 的 strand connectivity 不一致 → 局部 elastic 應力立刻扭回 W(0)（不穩定）
- $360°$ rotation 每條 sub-fiber 回到原本出射方向 → routing 守恆（拓撲穩定）

→ $360°$ 是「能加 winding 又不破壞 sub-fiber routing」的最小量子。

**$120°$ 與 $360°$ 各司其職**：

| Quantum | 位置 | 角色 |
|---|---|---|
| $360°$ | Vertex localized | W(1)/W(2)/W(3) 階梯的最小量子 |
| $120°$ | Fiber-level | Dispersion 配額（衰變 GW 量子、夸克分數電荷量子、W(1) 的 3-fiber dressing）|

---

## §4. EWSB Representation Selection

### 4.1 Edge Tw ↔ Vertex Wr Călugăreanu 等價

**核心 equivalence**：

$$\text{edge with Tw} = +1 \;\equiv\; \text{edge with Tw} = -1 \;+\; (+1\text{ Wr at each endpoint vertex})$$

**Călugăreanu 驗證**：unwinding then reverse-winding 把 edge Tw 從 $+1$ 變到 $-1$（$\Delta\text{Tw} = -2$）；Lk 守恆 → $\Delta Wr = +2$；vertex 對稱平分 → 每端 $+1$ Wr。

**Vertex 局部等價**（per vertex 周圍 3 edges 與 final lock 方向 aligned/reversed 計數）：

| 組合 | Vertex Wr inherit |
|---|---|
| 3 aligned, 0 reversed | $0$ |
| 2 aligned, 1 reversed | $+1$ |
| 1 aligned, 2 reversed | $+2$ |
| 0 aligned, 3 reversed | $+3$ |

低張力下兩種 representation 自由轉換、能量簡併。

### 4.2 EWSB 一階相變：Spontaneous Representation Selection

| 階段 | Mesh 描述 |
|---|---|
| Pre-EWSB（低張力）| Vertex W(1) handedness + edge Tw sign 各自 50/50 隨機；Călugăreanu 自由轉換 degenerate |
| EWSB trigger | Cosmic stretch 達臨界值 $T_c = M_Z$ |
| Bubble nucleation | 第一 nucleation bubble 的 chirality choice spontaneously 決定，**同時鎖** vertex W(1) 旋轉方向 + edge Tw 符號 |
| Post-EWSB | 全空間 coherent vacuum baseline $(t_0 = 5/12, w_0 = 3/8)$；reversed edges 的拓撲 footprint 透過 §4.1 機制轉移為 vertex Wr |

### 4.3 Post-EWSB Initial Vertex Wr Distribution

Pre-EWSB 50/50 隨機在 EWSB 鎖定後，每 vertex 周圍 3 edges 的 aligned/reversed 形成 binomial $\{1/8, 3/8, 3/8, 1/8\}$（§4.1 vertex Wr inherit table）。這是 EWSB phase transition **initial geometric distribution**——須再經 thermal Boltzmann selection 才得 final crystallized state（§10）。

### 4.4 Identification：Gauge Mixing = 幾何正交性損失

| SM gauge | HFT 幾何對應 |
|---|---|
| $U(1)_Y$ | $S^1$ 纖維 |
| $SU(2)_L$ | $S^2$ 基底網格切向旋轉 |

兩者**不在抽象 $SU(2)_L \times U(1)_Y$ 空間**，而是有具體 Hopf bundle 幾何載體。

**機制三步**：

1. Pre-EWSB 理想正交：$S^1 \perp S^2$；4 cohomology 等概率分配 → $\sin^2_{\rm ideal} = 1/4$
2. Representation selection 拒絕一個 chirality → $S^1$ 失去與 $S^2$ 完美正交
3. Gauge mixing：傾斜投影因子精準等於 $\sin^2\theta_W$；$1/4 \to 15/64$ 跌落 $\Delta\sin^2 = 1/64$

> **Gauge mixing 是 $S^1$ 與 $S^2$ 在 representation selection 中為釋放 $N_{\rm rep} = 10$ 個拓撲態必須支付的幾何正交性損失。**

副效應：消解兩個 paradox：
- 「兩個角不在同一平面」：$\sin^2\theta_W$ 直接是正交損失量度，無需跨空間 angle identification
- 「vertex $C_3$ 對稱破壞」：正交損失是 global Hopf bundle event，不依賴 local vertex 方向

---

## §5. EWSB 真空殘餘三框架同構

### 5.1 Framework A：sin²-space Rational Projection

從**全息資訊論**進入：$\sin^2\theta_W$ 是 native 128-slot 網格上的資訊佔空比。

**理想基準**（最大熵 equipartition）：4 個拓撲嚴格正交的上同調類等概率分配 → $\sin^2_{\rm ideal} = 32/128 = 1/4$。

**$\mathbb{Z}_2$ 鎖定的拓撲代價**：representation selection 拒絕一個 chirality → 凍結 2 Nyquist slots：

$$\Delta\sin^2 = \frac{32}{128} - \frac{30}{128} = \frac{2}{128}$$

**全域積分**（10 個可積表示一同承受偏移）：

$$\delta S_E = N_{\rm rep} \times \frac{N_{\mathbb{Z}_2\text{-cost}}}{N_{\rm Ny}} = 10 \times \frac{2}{128} = \frac{10}{64}$$

> Native 128-slot form $2/128$ 比約分後的 $1/64$ 更 transparent——避免掩蓋結構。

### 5.2 Framework B：Local Strain Gauss-Bonnet Integration

**macro = $\int$ micro** 廣義 Gauss-Bonnet：每節點正交性損失產生局部應變 $\epsilon = 2/128$，承載 $N_{\rm rep} = 10$ 個可積表示通道。歸一化用 Action-Information equivalence $N_{\rm nodes,eff} \equiv S_E$：

$$\delta S_E = \frac{1}{N_{\rm nodes,eff}} \sum_i N_{\rm rep} \cdot \epsilon = \frac{10}{64}$$

### 5.3 Framework C：Macro $Z_2$ Action Accounting（v13 §8）

$Z_2$ 強制事件在兩手性分支等量分配：

| 分支 | 沉積對象 | 拓撲電荷 |
|---|---|---|
| 左手分支（visible）| 可見物質質量基礎 | $\sum Q_f^2 = 8$ |
| 右手分支（vacuum stator）| $W^{(3)}$ 定子 | 等量 $8$（反作用）|

$$\delta S_E = \frac{\sum Q_f^2}{S_E} = \frac{8}{51.375} \approx 0.15573$$

### 5.4 三框架收斂

**A ≡ B**：寫出同一公式 $\delta S_E = 10/64$。

**A/B ≡ C**（透過絕對沉積量恆等式）：

$$\delta s_i \times N_{\rm nodes,eff} = \frac{10}{64} \times S_E = \sum Q_f^2 = 8 \;\Rightarrow\; \frac{8}{S_E} = \frac{10}{64}$$

**0.34% 殘差 = $D(t)$ 動態拉伸**：

- Static identity：$10/64 = 0.15625$
- Dynamic 觀測：$8/S_E = 0.15573$
- 差距 = $W^{(3)}$ 縱向拉伸 $D(t_0) = (L(t_0) - L_0)/L_0$（§11）

### 5.5 Reverse Derivation：sin² 空間的精確 dressing

把 $\delta S_E = 8/S_E$ 鎖定為絕對物理約束反推：

$$\sin^2\theta_W^{\rm exact} = \frac{1927}{8220} \approx 0.234428$$

對比 v13 leading $15/64 = 0.234375$：

$$\frac{1927/8220}{15/64} \approx 1.000227 \;\Rightarrow\; +0.023\% \text{ Dynamic Dressing}$$

巨觀 0.34% 在 sin² 空間僅 +0.023%，差距源於 leverage 因子 $N_{\rm rep} = 10$。**巨觀能量守恆與微觀幾何投影完美閉合**。

---

## §6. 四力的幾何起源

SM 三 gauge group $U(1) \times SU(2) \times SU(3)$ + Gravity 對應 fiber bundle 結構複雜度的四個層次，恰好匹配 4 個上同調類。

### 6.1 EM = $U(1)$ Fiber Holonomy（$H^1$ Twist）

**幾何本體**：vertex 垂直軸 $S^1$ fiber 的 holonomy。

帶電粒子互動透過垂直軸 fiber 內部相位波動進行**長程通信**。不形變 $S^2$ 基底 → 無拓撲 cost → **massless 長程**。

**光子**：vertex 垂直軸 fiber network 的 collective 縱向波——沿各 vertex 垂直軸之間 linkage 傳播。「正交於手性鎖定」就是垂直於 $S^2$ 的 axial fiber 方向。

### 6.2 Weak = $\text{Tw} \to Wr$ Boundary Map（$H^1 \to H^2$ interface）

**幾何本體**：$S^1$ fiber 強行「歪斜」進入 $S^2$ 網格的結構性阻力。

W/Z = $H^1 \to H^2$ boundary map 的 quantized propagating mode——既不純粹 $H^1$ 也不純粹 $H^2$，而是兩者振盪的 quantum：

```
Edge          Vertex          Edge          Vertex
 Tw    ─→     Wr     ─→      Tw     ─→     Wr   ...
(H^1)        (H^2)          (H^1)         (H^2)
       ↑              ↑              ↑
     boundary      boundary       boundary
     cost          cost           cost
     (Z_2)         (Z_2)          (Z_2)
```

每次 $\text{Tw} \leftrightarrow Wr$ 轉換支付 2 Nyquist slots 拓撲 cost——這 cost 就是 W/Z 質量。短程性來自 cost 累積的 Yukawa-like 衰減。

**EWSB tilt 量化**：$M_W/M_Z = \cos\theta_W = 7/8$。多繞一圈的 action cost：

$$\Delta M / T_c = 8 \times \cos\theta_W = 8 \times \tfrac{7}{8} = 7$$

其中 $8 = \sum Q_f^2$ visible charge tensor，$7/8$ 傾斜後正交保留——$\Delta M/T_c = 7$ 是**結構性 lock**，不是 fit 參數。

**W± vs Z⁰ 帶電不對稱性的 Strand-level 機制**：

兩者皆為 $H^1 \leftrightarrow H^2$ boundary map quantum，差別在「**$H^1 \leftrightarrow H^2$ 振盪是否伴隨整數 Tw winding 在 sector 之間正交轉移**」：

| Boson | 振盪性質 | $H^1$ winding | Sector 關係 |
|---|---|---|---|
| **Z⁰** | 封閉彈性振盪——strand 在 vertex 從 $\text{Tw}$ 擠壓為 $Wr$ 再釋放回 $\text{Tw}$ | 整體守恆 | 可在單一 sector 內封閉（如 $Z \to e^+e^-$ 或 $Z \to q\bar{q}$ 同 sector）|
| **W±** | 開放非彈性振盪——伴隨 1 unit integer Tw winding 在 horizontal 與 vertical sector 之間正交轉移 | 局部變化 $\pm 1$（charge transfer）| **必橋接 quark vertex（horizontal sub-fiber）與 lepton vertex（vertical axial fiber）** |

**Beta decay $d \to u + W^- \to u + e^- + \bar{\nu}_e$ 的 slow-motion**：

1. **初始態**：$d$ quark = sub-fiber strand Tw $= 0$（charge $0 - 1/3 = -1/3$）
2. **Vertex $B_3$ braid 觸發**：mass-energy 差驅動 vertex 構型重組，strand 拓撲路徑改變導致整數 Tw 躍遷 $0 \to +1$（支付 2 Nyquist slots boundary cost = $M_W$ 質量來源）
3. **終態 quark sector**：$u$ quark = sub-fiber strand Tw $= +1$（charge $+1 - 1/3 = +2/3$）；quark sector $H^1$ winding 增加 $+1$
4. **拓撲守恆強制**：horizontal sub-fiber 系統憑空增加 $+1$ winding 必須對應 $-1$ winding 在他處出現——**透過 $H^1 \to H^2 \to H^1$ boundary map 正交轉移**至 vertical axial fiber sector
5. **W⁻ 的真實身分**：被強行從 horizontal strand 系統正交扭轉進入 vertical axial fiber 的 $-1$ Tw winding 動態過程
6. **Settling**：$-1$ winding 在另一 vertex 垂直軸上 settle 為 $e^-$（vertical axis Tw $= -1$）+ 殘餘 sub-fiber Tw_L wave 為 $\bar{\nu}_e$（無 winding）

**整體 charge conservation 還原為 mesh $H^1$ winding 守恆**：

$$\underbrace{-\tfrac{1}{3}}_{d} = \underbrace{+\tfrac{2}{3}}_{u} + \underbrace{-1}_{e^-} + \underbrace{0}_{\bar{\nu}_e} \;\Leftrightarrow\; H^1 \text{ winding 全域守恆}$$

**為什麼 W± 必橋接 quark 與 lepton sector**：W± 本質上**就是** horizontal sub-fiber 與 vertical axial fiber 之間的整數 winding 轉移過程，所以必然連接兩個 sector（不可在單一 sector 內封閉）。Z⁰ 不轉移 winding，可以在單一 sector 內封閉振盪。

**為什麼 weak 是唯一 massive gauge boson**：weak 是唯一 cohomology boundary map quantum；其他三力對應 cohomology degree direct physics（無 boundary cost）。

**對 P7 quark flavor mapping 的鋪路**：flavor change（$d \leftrightarrow u$, $s \leftrightarrow c$, $b \leftrightarrow t$ 等）= strand 上 integer Tw winding 的離散躍遷。Quark flavor mapping reduce 為「allowed strand topology paths under vertex $B_3$ braid」的離散枚舉。

### 6.3 Strong = $B_3$ Vertex Braid（$H^3$ Link，Gauge Description 非 Stress Mode）

Strong 與其他三力**結構性錯位**：它**不是**另一種 propagating stress mode，而是**vertex 上 $B_3$ braid 離散構型空間的 elastic potential 結構**——SU(3) 規範描述是這個離散構型在連續 Lie algebra 上的 over-parameterized embedding。

**幾何本體**：$B_3$ vertex 編織，$Z_3$ 中心 = SU(3) color label。

- 3 條 horizontal fibers at vertex = 3 fundamental color labels
- 6 strands 在 vertex 內部 re-pair → $B_3$ braid 構型
- Color confinement = $B_3$ closure 拓撲必然（拉走 1 strand = 破壞整個 6-strand braid）

**HFT 不需要 Gluons**：

| QCD（連續）| HFT（離散）|
|---|---|
| 8 gluons 為 force carriers | 構型躍遷 + Nyquist 信息槽位枚舉 |
| α_s 連續 running | 離散 configuration transitions |
| Confinement 動力學待證明 | Confinement 是拓撲必然（$B_3$ closure）|
| Asymptotic freedom from β-function | 短距離 = 較少 strand crossings = 較低 elastic potential |
| Baryon 譜系 = SU(3) × spin reps | Baryon 譜系 = $B_3$ 構型 × Nyquist 槽位有限枚舉 |

**「強作用力」的真實意義**：

> Strong force = vertex $B_3$ braid 構型的 elastic potential 在離散躍遷中重新分配的 bookkeeping。

具體流程：構型 A → 構型 B + 能量差透過 EM/Weak/Gravity stress modes 釋放（photons、neutrinos、outgoing kinetic）。**所有可觀測能量釋放通道都走 EM/Weak/Gravity**——這三個是 real propagating stress modes；strong 是構型 bookkeeping。

**Lattice QCD 對應**：lattice QCD 必須離散化才能算 confinement——因為物理本來就是離散的，連續 SU(3) 是 non-native 選擇。HFT 直接以離散本體論為起點。

### 6.4 Gravity = $H^0$ Substrate Transverse Wave

**幾何本體**：$S^2$ mesh 的橫向張力波（W(0) substrate 形變）。

W(0) = 全 mesh $S^2$ structural action（85.625 units），所有 vertices 坐落其上。Substrate 形變透過 $H^0$ transverse wave 自由傳播——這個 wave 攜載 mass-energy 之間的 long-range coupling，等同於 GR 的 gravitational wave。

**Graviton-like collective mode**：substrate 上的 quantized transverse oscillation；所有攜能量的拓撲 excitation 都耦合此 mode → universal gravitational coupling。

### 6.5 四力對應總表

| 力 | Cohomology | 性質 | Mesh 對應 | Boson |
|---|---|---|---|---|
| **EM** | $H^1$ Twist（vertical）| Real propagating stress mode | Vertex 垂直軸 Tw fiber network | Photon |
| **Weak** | $H^1 \to H^2$ boundary | Real propagating stress mode（boundary quantum）| $\text{Tw} \to Wr$ 轉換阻力 | W/Z |
| **Gravity** | $H^0$ Vacuum | Real propagating stress mode | $S^2$ mesh 橫向張力波 | Graviton-like collective |
| **Strong** | $H^3$ Link | **離散構型 gauge description**（非 stress mode）| $B_3$ vertex braid | **無**（gluon 是 QCD 連續近似 artifact）|

**4 上同調類精確對應 4 種力**——其中 3 個是 propagating stress modes，1 個是離散構型 gauge description。這個 asymmetry 解釋為什麼 weak 是唯一 massive gauge boson、為什麼 strong 沒有可觀測的「force carrier」。

---

## §7. 電荷的微觀幾何

電荷 = **$S^1$ fiber 在 Hopf 叢中的 holonomy**：

$$Q = \oint_\gamma A \cdot dx$$

電荷種類由 fiber bundle topology + 拓撲層次（full-fiber vs sub-fiber）決定。

### 7.1 Lepton 整數電荷 = Vertex 垂直軸 Tw

帶電輕子 Tw 攜帶在 **vertex 垂直軸 fiber**（§3.4）。垂直軸上 1 unit Tw winding = 1 charge quantum。

當垂直軸 Tw 透過 mesh 張力連通傳到 horizontal $S^2$ 結構時，$Z_3$ 對稱強迫應力等量分擔給 3 條 horizontal edges（每 edge 1/3 份）；但 lepton 是 **source 觀測者**——測量的是垂直軸本體的 integer Tw winding，所以電荷是整數 $\pm 1$。

### 7.2 Quark 分數電荷 = Sub-Fiber Strand 斷裂重組釋放

**Quark 拓撲身分**：

- Baryon vertex 是穩定 $B_3$ braid（6 strands = 3 fibers × 2 strands homochiral）
- **Quark = 該 braid 中單一 strand 攜帶的 sub-fiber Tw 應力**
- 每 strand 在 vertex re-pairing 中跨越**兩條相鄰 edges**
- Strand 應力釋放（局部斷裂重組）→ 沿該 strand 路徑往兩端 edges 傳出

**Color = strand 所屬 fiber label**（3 fibers at vertex → 3 colors）。

**1/3 量子來源**：strand 局部斷裂重組釋放的應力 = 1/3 vertex Wr dispersion 配額（$Z_3$ 強迫等量分擔到 3 fibers，每 fiber 領 $120°$ = $1/3$ turn）。

$$Q_{\rm quark} = (\text{strand 上 integer Tw}) + (-\tfrac{1}{3} \text{ dispersion 配額})$$

| 夸克 | strand Tw | dispersion | 總電荷 |
|---|---|---|---|
| d | 0 | $-1/3$ | $-1/3$ |
| u | $+1$ | $-1/3$ | $+2/3$ |
| d̄ | 0 | $+1/3$ | $+1/3$ |
| ū | $-1$ | $+1/3$ | $-2/3$ |

**Confinement 自動滿足**：strand 必須兩端 anchored 到 vertex $B_3$ braid，pulling out 1 strand = 破壞 6-strand braid 結構。

**Flavor 雙量子數結構**：完整 quark flavor 由**兩個獨立量子數**決定：

| 量子數 | 範圍 | 決定 |
|---|---|---|
| **$n$**（strand 在 vertex 內 winding number）| $\{1, 2, 3\}$ | Mass tier / generation |
| **Integer Tw on strand** | $\{0, +1\}$（antiquark $\{-1, 0\}$）| Charge type（down-type / up-type）|

| $n$ \ Tw | 0（down-type）| +1（up-type）|
|---|---|---|
| 1 | d | u |
| 2 | s | c |
| 3 | b | t |

兩量子數獨立組合 → 6 quark flavors + 6 antiquarks。具體 mapping 詳見 §8.3。

### 7.3 Baryon 整數電荷的 Emergent Consistency

3 個夸克 confined 在同一 vertex 時，3 個 1/3 vertex offset **填滿一個完整 Wr 量子**：

$$3 \times \tfrac{1}{3} = 1$$

| 重子 | 夸克 | sub-fiber Tw 和 | vertex Wr | 總電荷 |
|---|---|---|---|---|
| $\Delta^{++}$ | uuu | $+3$ | $-1$ | $+2$ |
| p | uud | $+2$ | $-1$ | $+1$ |
| n | udd | $+1$ | $-1$ | $0$ |
| $\Delta^-$ | ddd | $0$ | $-1$ | $-1$ |

> 重子電荷必為整數 $\Leftrightarrow$ vertex Wr 量子必須整數填滿 $\Leftrightarrow$ 3 quark 必須一起出現

把 **color confinement、baryon number、整數電荷** 統合到同一 vertex 拓撲約束。

### 7.4 中微子 $Q = 0$（Tw Wave 非 Tw Winding）

關鍵 distinction：**Tw winding（holonomy，$H^1$ non-trivial）vs Tw wave（local oscillation，$H^1$ trivial）**——兩者數學上不同 cohomology class。

電荷 = $\oint_\gamma A \cdot dx$ 只測量 **closed 不 exact 的 1-forms**——即繞 base loop 的 winding。

| 性質 | 拓撲身分 | 電荷？ |
|---|---|---|
| Tw winding（繞 base loop 不可收縮）| $H^1$ non-trivial | ✓ 帶電 |
| Tw wave（局部 torsional 振盪）| $H^1$ trivial（exact）| ✗ 不帶電 |

中微子 = vertex 垂直軸 Tw = 0（無 winding）+ horizontal sub-fiber Tw_L 殘餘 wave（提供 meV mass）。光子也是 Tw wave（沿垂直軸 network 傳播）——兩者在 $H^1$ trivial class 同類，差別在傳播 channel + chirality。

**中微子只走 weak + gravity**：sub-fiber Tw wave 在 vertex 仍可激發 $H^1 \to H^2$ boundary map（弱作用），且攜能量耦合 $H^0$ substrate（重力）；無 $H^1$ winding 故無 EM；不參與 $B_3$ braid 故無 strong。

---

## §8. SM 質量階梯

### 8.1 Lepton Mass = Vertex 垂直軸 Tw × Mesh 張力連通耦合

$$m_\ell \;\propto\; T_{\rm vertical}(n) \;\times\; k_{\rm vertex\text{-}edge\,coupling}$$

**SM 對應**：

| SM 概念 | HFT mesh 對應 |
|---|---|
| Higgs vev | post-EWSB mesh-wide 張力連通本身（不是某 scalar field expectation）|
| Yukawa coupling | $k_{\rm vertex\text{-}edge}$（每 lepton flavor 不同的 specific coupling profile）|
| Lepton charge | 垂直軸 Tw winding（integer）|
| Lepton mass | charge × coupling × mesh tension |

**為什麼沒有 EWSB 就沒有 lepton mass**：pre-EWSB mesh 鬆散，垂直軸與 horizontal edges 解耦，垂直軸 Tw 不被「拉」成 inertia。Post-EWSB 張力連通激活，垂直軸 Tw 透過耦合 transmit 為 lepton mass。

### 8.2 Lepton Generation = Winding Density 階梯

垂直軸 winding density $n$ 決定 generation：

| Lepton | $n$ | 物理 |
|---|---|---|
| e | 1 | 最低 generation, stable |
| μ | 2 | 第 2 階, 半穩定 |
| τ | 3 | 第 3 階, 半穩定 |
| (4+) | — | **不存在**（超過 vertex 信息容量極限）|

**3 是 information capacity ceiling**——同一極限在多個 sector 的 manifestation：

| Sector | Generation 載體 | $n=1, 2, 3$ 對應 |
|---|---|---|
| **Lepton** | 垂直軸 fiber 的 winding density per unit length | e / μ / τ |
| **Quark** | 單一 strand 在 vertex 內 winding number | (u,d) / (c,s) / (t,b) |
| **W(n) Writhon** | Vertex Wr quantum 數 | W(1) DM / W(2) GW / W(3) instant disperse |
| **CS truncation** | $SU(3)_3$ integrable reps | $\binom{3+2}{2} = 10$（含真空）|

→ **$k=3$ 是同一個 information capacity 上限的多重 manifestation**。為什麼宇宙剛好 3 generations、為什麼 W(3) 不穩定、為什麼 quark flavor 階梯也終止在第 3 階——全部 reduce 到 vertex 的離散信息容量上限這個單一拓撲事實。

具體比例（v13: $m_\mu/m_e = 137 \times 3/2 \approx 205.5$、$m_\tau/m_\mu = 137/8 \approx 17.125$）來自 mesh elastic structure 與 $N_{\rm skel}$ 耦合，是 follow-up Paper 3 量化任務。

### 8.3 Quark Mass：雙來源

**Current mass（Higgs-like, ~MeV）**：strand 上小量 Tw winding × post-EWSB mesh 張力連通——與 lepton 同機制的小貢獻。

**Constituent mass（QCD-like, ~300 MeV）**：strand 在 vertex $B_3$ braid 中佔據的張力比例：

$$m_q^{\rm constituent} \;=\; \tfrac{1}{3} E_{\rm vertex}^{B_3\text{-config}}$$

**Generation = Strand Winding Number $n$**：quark generation 對應 strand 在單一 vertex 內部的 winding number $n \in \{1, 2, 3\}$：

| $n$ | Quark | 拓撲描述 | Mass scale |
|---|---|---|---|
| 1 | (u, d) | 最簡穿越路徑，無額外打結，順利完成 re-pairing | 最輕（MeV 級）|
| 2 | (c, s) | Strand 在 vertex 內多繞 1 圈 | 中等（GeV 級）|
| 3 | (t, b) | Strand 在 vertex 內繞 3 圈，達到 $k=3$ CS 信息極限 | 最重（GeV–百 GeV 級）|

更高 $n$ → strand 累積更高拓撲應力 + 更大 elastic tension → 更重 mass。$n=4$ 不存在因為超過 $k=3$ Chern-Simons information ceiling——這也是為什麼 SM 剛好 3 個夸克 generation。

### 8.4 Baryon Mass = Vertex $B_3$ Braid 彈性位能

$$m_{\rm baryon} \;=\; E_{\rm vertex}^{B_3\text{-config}} \;=\; \sum_{\rm strands} T_{\rm strand}^{\rm braid\,config}$$

整個重子質量 = 該 $B_3$ 構型中 3 條 quark strand tensions 的總和。每 strand 的 tension 由其 winding number $n$ 決定（§8.3）。編織越緊、內部 winding 數越高，整個重子越重。

**重子譜系 = 離散構型枚舉**：

1. Nyquist 信息容量極限下列出所有 allowed $B_3$ braid configurations
2. 每構型 strand tension 總和 = mass eigenvalue
3. 對應 v13：$SU(3)_3$ 10 個 integrable reps = 10 個基礎 vertex 構型 class；$N_v^2 = 9$ 非真空 frozen knot classes = 9 種最低構型
4. 重子 octet（8 baryons，spin-1/2）可能對應 9 - 1 = 8 ground configurations；decuplet（10 baryons，spin-3/2）對應第 1 階激發層

**Baryon Zoo 範例**（P7 + P10 綜合應用）：

| 重子 | 夸克組成 | $B_3$ braid 結構 | Mass scale |
|---|---|---|---|
| **質子 $p$** | $uud$ | 3 條 $n=1$ strands 交織成最低張力 $B_3$ 穩態——所有 strand 無額外打結 | $938$ MeV（最輕穩定 baryon）|
| **$\Delta^{++}$** | $uuu$ | 3 條 $n=1$ strands 但 spin-3/2 對稱配置 → 第 1 階激發 | ~$1232$ MeV |
| **奇異 $\Lambda$** | $uds$ | 2 條 $n=1$（u,d）+ 1 條 $n=2$（s）；s strand 多繞 1 圈撐高內部張力 | ~$1116$ MeV |
| **底重子 $\Lambda_b$** | $udb$ | 2 條 $n=1$（u,d）+ 1 條 $n=3$（b）；b strand 在 vertex 內繞 3 圈，極高拓撲張力 | ~$5619$ MeV（質子的 $\sim 6$ 倍）|

→ 重子 zoo 直接從 $\{n_1, n_2, n_3\}$ + flavor 組合枚舉，每個構型對應特定 strand tension 總和。

**Allowed Transitions**（衰變動力學）：構型 A 何時可衰變到構型 B？

- B_3 braid 從高張力構型「鬆脫」成低張力構型 = strand 上 winding number $n$ 降階（如 $b$ → $c$ 是 $n=3 \to n=2$，或 $b$ → $u$ 是 $n=3 \to n=1$）
- 此躍遷的 micro 機制 = strand integer Tw 改變（charge type 變化）+ 透過 W± 把 1 unit Tw winding 正交轉移到 vertical axis（產生 lepton + neutrino，§6.2 P8 機制）
- 釋放的彈性位能差透過 EM/Weak/Gravity stress modes 帶走——**無 gluon mediation**

→ P10 「allowed B_3 transitions」reduce 為 strand 量子數 $\{n, \text{Tw}\}$ 的 allowed jumps + 對應 stress mode 觸發條件——與 P8 W± 機制完全橋接。

### 8.5 Meson = 兩 Vertices 間 Single-Strand Tension

**最自然構型**：單一 strand 連接兩 vertices——一端 q，另一端 q̄。

- Strand 攜 net Tw winding + 兩端 vertex Wr dispersion 配額
- 兩端 anchored 到 2 個 vertex 的 $B_3$ braid → 不能 pull out → confinement 自動
- $m_{\rm meson}$ = strand 整體 elastic tension + vertex contribution

### 8.6 W/Z Mass = Boundary Map Cost

W/Z 沒有靜態 mass term——mass 來自每次跨越 $H^1 \to H^2$ boundary map 支付的 $\mathbb{Z}_2$ 拓撲 cost（2 Nyquist slots）累積為 Yukawa-like 衰減：

$$M_W = \text{boundary cost per cycle}$$

$$M_Z = M_W / \cos\theta_W \approx M_W \times 8/7$$

Z 走「正向」boundary（完整 round-trip 守恆 winding），W± 走「斜向」boundary（直接 charge transfer）——Z 多支付一個 $1/\cos\theta_W$ 因子。

### 8.7 Asymptotic Freedom（無 Gluon 機制）

- 短距離 = strand 在 vertex 內部簡單路徑段 = 較少 tension
- 長距離 = strand 須繞過 mesh 較多 vertex = 累積 tension 線性增加
- 與 QCD linear confinement potential 結構一致，但機制是 **strand elastic tension** 而非 gluon flux tube

### 8.8 統合對應表

| | Lepton | Baryon |
|---|---|---|
| Mass 來源 | 垂直軸 Tw × mesh 張力連通（$H^1$ + Higgs-like）| Vertex $B_3$ braid elastic potential（$H^3$ Link）|
| EWSB 依賴 | **依賴**（無 EWSB 無 mesh 張力連通）| **不依賴 EWSB Higgs**（純 vertex 構型 elastic）|
| 對應 SM 觀測 | Yukawa coupling 給 lepton mass | QCD 結合能給 baryon mass（chiral symmetry breaking）|

→ HFT 兩 mass 來源**結構分離**——精確 match SM mass 來源分工。

**重子衰變**：構型 A → 構型 B + 能量差透過 EM/Weak/Gravity stress modes 釋放（emit photons、neutrinos、outgoing kinetic）。**無 gluon mediation**——所有可觀測能量釋放通道都走 real stress modes。

---

## §9. W(n) Writhon Hierarchy + Dark Sector

### 9.1 W(0) 是 $S^2$ Substrate

W(0) **不是** vertex 子集，而是全 mesh $S^2$ 結構性 action：

$$\text{W(0) substrate} = N_{\rm skel} \times \cos^2\theta_W\big|_{\rm GUT} = 137 \times \tfrac{5}{8} = 85.625$$

W(0) = 鎖在 $S^2$ 結構的 vacuum geometry（v13「stator 真空幾何」/ 宇宙學常數來源）。

| Action sector | 量 | 角色 |
|---|---|---|
| W(0) substrate | $85.625$ | 鎖在 $S^2$ 結構，不參與 EWSB partition |
| $S_E$（EWSB-active）| $51.375$ | 進入 visible/dark 分配 |
| └ Visible | $8$ | 質子等可見物質 |
| └ Dark | $43.375$ | $\to$ W(1)/W(2)/W(3) excitations |

### 9.2 Vertex 激發階梯

```
Excitation Energy
     ↑
     |  W(3)  ──  3 turn excess Wr（瞬時 disperse）
     |  W(2)  ──  2 turn excess（unstable，shed 1 turn → W(1)）
     |  W(1)  ──  1 turn excess Wr（stable，DM 候選 ~5.08 GeV）
     |  ─── W(0) substrate baseline（vertex 上 0 excess Wr）───
```

> v13 主論文使用 W(1)/W(2)/W(3) 命名，其中 v13 W(3) 是 ground state（對應本文件 W(0) substrate）。本文件採用 W(0) = substrate 慣例。

### 9.3 衰變動力學

**W(2) → W(1)**：unstable，shed 1 turn 透過 $Z_3$ dispersion：

$$W(2) \xrightarrow{\text{shed 1 turn}} W(1) + 3 \times (\tfrac{1}{3}\text{ Tw on outgoing fibers})$$

**W(3) → W(1)**：超出 vertex 信息極限，瞬時 shed 2 turns。

W(1) 是**最低非零拓撲荷穩定 floor**——非零拓撲荷無 annihilation 伴侶，不可衰變到 W(0) substrate。Shed fiber Tw 量子沿 fiber 傳播 dissipate 為 propagating GW。

**衰變 timescale**：

| State | timescale | 機制 |
|---|---|---|
| W(3) | 瞬時（< Hubble at EWSB）| 超過 vertex information 極限 |
| W(2) | EWSB → reheating（~$10^{-12}$ s）| 局部張力 over-threshold |
| W(1) | eternal | 穩定 DM |

**EWSB GW pulse prediction**：W(2)/W(3) 衰變 fiber Tw quanta 集中於 EWSB-reheating window 釋放，為 LISA-band sharp GW background（~$10^{-5}$ Hz today），疊加在 bubble nucleation broadband GW 之上。

### 9.4 W(1) 完整結構

| 元素 | 量 |
|---|---|
| Vertex Wr | 360°（嚴格 localized integer quantum）|
| 3-fiber dressing | 各 120° Tw（$Z_3$ 對稱副產品）|
| Mass | ~5.08 GeV（vertex 處 elastic potential）|

W(1) 的完整 state = vertex 360° Wr **+** 3-fiber 120° dressing 的整合 composite。

### 9.5 W(2) Mass = 128 × W(1) Mass（Action ≡ Information）

從 Action ≡ Information 本體論：

- W(1) 多 1 turn vertex Wr → 占用少量 Nyquist slots（resolved < 128）
- W(2) 多 2 turn + EWSB 傾斜耦合 → 多繞圈與傾斜耦合**佔用全部 128 Nyquist slots**（saturation）

$$M_{W^{(2)}} = M_{W^{(1)}} \times N_{\rm Nyquist} = M_{W^{(1)}} \times 128 \approx 650 \text{ GeV}$$

Mass 不是 turn 數的線性函數，是 **turn × 傾斜耦合的信息容量函數**——v13 既定 Nyquist saturation 的結構結果。

### 9.6 W(1) 為何不耦合 EM/Weak/Strong

| 力 | Cohomology | W(1) 耦合？ | 原因 |
|---|---|---|---|
| EM | $H^1$ vertical | ✗ | W(1) 是 $H^2$（horizontal Wr）class，與 vertical axis $H^1$ 拓撲正交 |
| Weak | $H^1 \to H^2$ boundary | ✗ | W(1) 已是純 $H^2$ 鎖定態，無 free $H^1$ component 可走 boundary map |
| Strong | $H^3$ Link | ✗ | W(1) 單一 vertex localized，無 cross-vertex linking |
| Gravity | $H^0$ | ✓ | 攜能量 → 耦合 substrate |

→ W(1) **只與 gravity 耦合**——這是 cold dark matter 的觀測 signature。

「**winding 不等於 charge**」是 HFT 對 SM 觀測的精細結構解釋：
1. 電荷需要 winding 拓撲（$H^1$ non-trivial）
2. 電荷需要 winding **方向**正確（$S^1$ vertical axis 而非 $S^2$ base）
3. W(1) 滿足 (1) 但不滿足 (2)（在 $H^2$ 不在 $H^1$）→ 不帶電

### 9.7 W(1) 傳播：Substrate Gravity Wave Passive Transport

W(1) 唯一可用 propagation channel 是 gravity（$H^0$ substrate）。

**移動機制**（passive transport via substrate wave）：

```
其他質量 source       Substrate gravity wave        W(1) 所在 vertex
（或宇宙背景）  ──→  on H^0（free propagation  ──→  (360° Wr + 3-fiber dressing)
                       on whole S^2）
                                                          ↓
                                                Wave 修改 W(1) 周圍 fiber dressing
                                                → elastic potential 重心偏移
                                                → W(1) 整體「漂」到相鄰 vertex
```

**類比：海浪推船**——W(1) 是 passive object，移動由 background substrate wave dynamics 驅動。Free W(1) 不移動；cosmological context 永遠 nonzero stress，W(1) 隨流移動。

**與 W(n) 衰變的區分**：

| 過程 | 機制 | Wr 量子 |
|---|---|---|
| W(n) → W(n-1) 衰變 | Vertex 真 unwind 1 turn → 3 fibers 各得 120° Tw 為**獨立 GW pulse** | $\Delta n = -1$ |
| W(1) → W(1) 平移 | **整體 hop 不 unwind**——substrate dragging | $\Delta n = 0$ |

3 fibers × 120° dispersion 只在真衰變時觸發。W(1) propagation 期間 Wr 量子守恆。

**對 DM 觀測的精細解釋**：

| 觀測 | HFT 機制 |
|---|---|
| DM cold（非相對論）| W(1) 攜 finite mass，substrate wave 速度上限 $c$ 但 W(1) 隨流速度 $\ll c$ |
| DM clustering | substrate gravity waves 朝向質量集中區 → 推 W(1) 流向 → halo 形成 |
| DM 不衰變 | propagation Wr quantum 守恆 |
| DM 與 baryon halo offset（子彈星系團）| baryon 壓力波推 substrate wave，W(1) dressing 響應 lag → DM halo 落後 |

---

## §10. Stage-Separated Synthesis with v13

新 picture 的 vertex binomial 統計與 v13 既有 Boltzmann formula 在 EWSB phase transition 不同階段各司其職。

### 10.1 三階段流程

| Stage | 描述 |
|---|---|
| Pre-EWSB（無張力，無傾斜）| 50/50 mixed L/R edges；trivalent vertex (L,R) 組合給 binomial 分布 $\{1/8, 3/8, 3/8, 1/8\}$ |
| EWSB transition（一階相變 + 傾斜 lock）| Bubble nucleation 鎖定 representation；傾斜 lock 引入 $\Delta M/T_c = 7$ Boltzmann selection |
| Crystallization at $T_c = M_Z$ | $x_{W^{(2)}} = (1/9) \cdot 128 \cdot e^{-7.04} \approx 1.25\%$ 倖存為 W(2)；其餘退回 W(1) |
| Reheating 結束 | W(2) 全衰變到 W(1) + GW；W(3) 已早於 reheating 衰變 |

→ 新 picture 給 **initial geometric distribution**；v13 Boltzmann 給 **final crystallized distribution**——兩者描述不同階段，不衝突。

### 10.2 v13 Refined Formula 結構性保留

$$\Omega_c/\Omega_b\big|_{\rm refined} = \frac{43.375 (1 - x_{W^{(2)}} \cdot 127/128)}{8} \approx 5.354$$

- $43.375$：dark budget（macro action partition，與 micro 解耦）
- $x_{W^{(2)}} = 1.25\%$：crystallization 時 Boltzmann-weighted 倖存比例（傾斜網格幾何 lock 結構結果）
- $127/128$：W(2) → W(1) decay 的 mass loss 比例（Nyquist saturation 結構結果）
- $\Delta M/T_c = 8 \times \cos\theta_W = 7$：EWSB 傾斜結構性 lock

新 picture 解釋為什麼**沒有** 12% 級的 binomial-naive 修正：傾斜 lock 把 binomial 中 $3/8$ 的 W(2) candidate 中絕大多數 thermal-fluctuated 回 W(1)，只剩 1.25% Boltzmann tail 倖存為真 W(2) 直到 crystallization frozen。

### 10.3 Candidate Y 的 Scope

| Layer | 內容 | Candidate Y | v13 主論文 |
|---|---|---|---|
| Leading 5.422 | Action budget $43.375/8$，與 micro 解耦 | ✓ 主張，4σ tension 公開承擔 | ✓ |
| Refined 5.354 | W(2) Boltzmann + decay 修正 | ✗ 不主張 | ✓ |

Candidate Y 的 5.422 derivation 純 macro action partition，**不依賴 micro picture**——新 picture 不影響其 claim。

---

## §11. Cosmological Cascade

### 11.1 $D(t)$ Stretch 是 +0.023% Dressing 的物理源頭

§5.5 反向推導確立：v13 結構性 $15/64$ 須產生 +0.023% dressing 才能完美吸收 $\delta S_E$ macro 預算。

**唯一存活候選**：$W^{(3)}$ 網格的縱向拉伸 $D(t) = (L(t) - L_0)/L_0$（v13 §10 item 4）。

排除候選：純數學高階項（違反古典張力場本體論）、球面曲率修正（與 Wyler volume 推導重複計算）。

### 11.2 $D(t)$ 的本體論身分：宇宙膨脹的各向異性分量

$D(t)$ 真正的物理身分是**宇宙膨脹的 anisotropic component**，不是 $S^2$ 的絕對拉伸量。

**分解**：

$$D_{\rm cosmic}(t) = \underbrace{D_{\rm iso}(t)}_{\text{trivial scaling}} + \underbrace{D_{\rm aniso}(t)}_{\text{observable drift source}}$$

| 分量 | 性質 | 物理可觀測？ |
|---|---|---|
| Isotropic（$S^3$ 全空間 synchronous expansion）| 所有 dimensionful 量等比例縮放 | ✗——dimensionless ratios 全部不變 |
| Anisotropic（$S^2$ vs $S^1$ 各向異性差別演化）| 改變幾何 ratio（vertex 配置、orthogonality angle、Nyquist slot 分配）| ✓——drift cascade 的物理 driver |

→ $D(t)$ 的真實意義 = $D_{S^2}(t) - D_{S^1}(t)$ 差量——「$S^2$ 相對 $S^1$ 多出的拉伸」，而非 $S^2$ 的絕對拉伸量。

**為什麼 isotropic 分量不可觀測**：v13 既定結構結果（$\sin^2\theta_W = 15/64$, $\alpha^{-1} = 137$, $N_{\rm rep} = 10$, $\Delta M/T_c = 7$）皆 dimensionless——若 $S^2$ 與 $S^1$ 等比例擴張，所有 ratio 不變、無 drift 可觀測。drift 必然來自結構 ratio 的改變，即各向異性。

### 11.3 $S^1$ Vertical Axis 的本體論立場

$S^1$ vertical fiber **不獨立拉伸**，這個 statement 在 anisotropic framing 下精確意義：

- $S^1$ 跟著 $S^3$ isotropic 部分 trivially scale（無 observable consequence）
- $S^1$ **無獨立 anisotropic component**——不引入額外 free parameter
- 「$D_{S^1}(t)$」實質為零 in anisotropic sense
- Vertical axis 的 effective tension 變化全部透過 vertex coupling，由 $D_{\rm aniso}(t) \approx D_{S^2}(t)$ 單一 source 驅動

這是 HFT 本體論承諾：**$S^2$ 是 base shell（有切線方向，elastic 動力學 well-defined）；$S^1$ 是 phase substrate（無「長度」可言，winding 是拓撲整數量子化）**。兩者 ontologically 不對稱——逼它們「都該有 stretch」是 unwarranted symmetry assumption。

### 11.4 連到 $W^{(3)}$ Stator 雙成分動力學

v13 §10 item 4 既定 $W^{(3)}$ stator 雙成分結構：

- **Planck-cell 不可壓縮**（horizontal $S^2$ direction）：mesh cell 體積守恆 + 拓撲剛性
- **Hopf-fiber 彈性 with $L_0$**（vertical $S^1$ direction）：fiber 軸向 elastic restoring

兩者對 cosmic expansion 響應**結構性不同**：

- $S^2$ direction：透過 cell 重排吸收膨脹（Planck-cell 數量增加，individual cell 結構不變）
- $S^1$ direction：受 $L_0$ 自然長度 restoring force 約束，fiber 不易拉伸

→ 響應差異**自然產生** $D_{\rm aniso}(t) \neq 0$——這就是 anisotropic stretch 的物理 source。

### 11.5 機制：微觀正交性 × 各向異性膨脹的耦合

W(0) substrate 並非絕對剛體：

- 隨宇宙膨脹，$S^2$ 比 $S^1$ 多拉伸 $D_{\rm aniso}(t)$
- 各向異性拉伸使「正交投影」幾何參考系微小形變——$S^1 \perp S^2$ 角度漂移
- $D_{\rm aniso}(t)$ 直接作用於微觀拓撲投影點 → 局部 $\sin^2\theta_W$ 偏離純拓撲基態 $15/64$

$$+0.023\% = D_{\rm aniso}(t_0) \text{ 投影到弱同位旋通道的分量}$$

### 11.6 Cascade 結構係數 First-Principles Derivation（F1c + F1d Lock 2026-05-07）

D(t) 是**單一 scalar 動力學變量**，α 與 θ_W 殘差都從同一場 readout，係數從 cell counting 嚴格 derive。

**Setup**：
$$\alpha^{-1}(t) = N_{\rm skel}(D(t)), \quad \sin^2\theta_W(t) = \frac{N_w(D(t))}{N_{\rm Ny}(D(t))}$$

**$D$ 對 mesh 結構的 differential 影響**：

| 成分 | 物理 | $D$-scaling |
|---|---|---|
| $N_{\rm Ny} = 128$ | $S^2$ Nyquist cell count | $\propto$ area $\sim 1 + 2D$ |
| $N_v^2 = 9$ | $SU(3)_3$ frozen knot classes | **拓撲不變**（$D$-independent）|
| $N_w = 32 - 2$ 中的 $32$（cohomology share）| 一個 cohomology class 的 cell share | $32 \to 32(1 + 2D)$ |
| $N_w$ 中的 $-2$（chirality frozen） | $\mathbb{Z}_2$ 鎖定代價 | **拓撲不變**（$D$-independent）|

#### $k_{\alpha^{-1}}$ derivation

$$\alpha^{-1}(D) = N_{\rm Ny}(1+2D) + N_v^2 = 128(1+2D) + 9 = 137 + 256\, D$$

$$\boxed{k_{\alpha^{-1}} = \frac{\partial \ln \alpha^{-1}}{\partial D}\bigg|_{D=0} = \frac{256}{137} \approx 1.869}$$

結構意義：$256/137 = 2 N_{\rm Ny}/N_{\rm skel}$——area scaling factor 2 × Nyquist 在 skel 中的 share。

#### $k_\theta$ derivation

$$\sin^2\theta_W(D) = \frac{32(1+2D) - 2}{128(1+2D)} = \frac{1}{4} - \frac{2}{128(1+2D)}$$

對 $D$ 微分（at $D=0$）：

$$\frac{d\sin^2}{dD}\bigg|_{D=0} = \frac{4}{128} = \frac{1}{32}, \quad \frac{\Delta\sin^2}{\sin^2}\bigg|_{D=0} = \frac{1/32}{15/64} \cdot D = \frac{2}{15}\, D$$

$$\boxed{k_\theta = \frac{\partial \ln \sin^2\theta_W}{\partial D}\bigg|_{D=0} = \frac{2}{15} \approx 0.133}$$

結構意義：$k_\theta$ 來自 chirality-frozen 2 slots **不隨 $D$ scale** 的不對稱——若 frozen slots 也隨 area scale，$k_\theta = 0$（純比例情況下 sin² 不漂移）。

#### Sharp Ratio Prediction

$$\boxed{\frac{\Delta\alpha^{-1}/\alpha^{-1}}{\Delta\sin^2\theta_W/\sin^2\theta_W} = \frac{k_{\alpha^{-1}}}{k_\theta} = \frac{1920}{137} \approx 14.01}$$

完全離散組合純數，**無 free parameter**。

#### 與 v13 +0.023% Dressing 對齊

從 §5.5 鎖定 $\Delta\sin^2/\sin^2 \big|_{t_0} = +0.023\%$：

$$D(t_0) = \frac{0.023\%}{2/15} \approx 0.173\%, \quad \frac{\Delta\alpha^{-1}}{\alpha^{-1}}\bigg|_{t_0} \approx 0.32\%$$

→ **HFT 預測 $\alpha^{-1}$ cosmic 漂移約 0.32%**，與 sin² 漂移嚴格 14:1 比例。

### 11.7 Falsifiable Cascade Prediction

**重要 framing 釐清**：D(t) 只**直接耦合兩個結構性 channel**（α 與 sin²θ_W 各自從 mesh cell counting 獨立 derive）。其他 SM 觀測量（$G_F, v, m_e, m_p, \mu$）都是 SM cascade derived 函數：

$$D(t) \xrightarrow{\text{直接}} \{\alpha,\, \sin^2\theta_W\} \xrightarrow{\text{SM cascade}} \{G_F, v, m_e, m_p, \mu, \dots\}$$

**Sharp test 只有一個**：14:1 ratio。其他 cascade-derived 觀測量是 **consistency checks**，不是新的 D(t) sharp lock。

| Lock 層級 | 內容 |
|---|---|
| **Primary sharp test**（picture unique structural lock）| $\Delta\alpha^{-1}/\alpha^{-1} : \Delta\sin^2/\sin^2 = 1920/137 \approx 14.0$ |
| **Consistency checks**（cascade-derived，獨立 systematics）| $\Delta\mu/\mu, \Delta v/v$ 等須落在 SM cascade 從 $(\Delta\alpha, \Delta\theta_W)$ derive 的具體數值 |

**Falsifiable channels**：

| 觀測 | 可測量 | HFT 預測 (at $D = 0.173\%$) |
|---|---|---|
| Atomic clock | $\dot\alpha/\alpha$ | 取決於 $\dot{D}(t)$ 動力學 regime（F1a/F1b）|
| Quasar absorption (UVES/HARPS/ESPRESSO) | $\Delta\alpha/\alpha$ at $z \sim 2$–$5$ | $\sim 0.3\%$ 級漂移 |
| ELT 高解析光譜 | $\Delta\sin^2/\sin^2$ at high-z | $\sim 0.023\%$ 級漂移 |
| **Ratio test (primary)** | $\Delta\alpha^{-1}/\alpha^{-1} \div \Delta\sin^2/\sin^2$ | **= 14.0 嚴格 lock** |
| ELT $\Delta\mu/\mu$ | μ drift at high-z | cascade-derived（§11.9）|
| CMB recombination | $\alpha(z=1100)$ | inflation/recombination-era $\alpha$ shift |

**Falsification 標準**：
- 14:1 ratio 違反 → **falsify** HFT cascade picture（primary structural test）
- $\Delta\mu/\mu$ 偏離 SM cascade 預測 → 表示 picture 含 D ↔ $\Lambda_{\rm QCD}$ 直接耦合（HFT-specific 拓撲 signature 可能性，非 SM cascade 抓得到）

### 11.8 F1a + F1b: D(t) 動力學——Phase-Transition Impulse Picture（2026-05-08）

#### 動力學方程與 quasi-static regime

$D(t)$ 是 mesh anisotropic strain，dimensionless scalar field。完整動力學方程：

$$\ddot{D}(t) + \gamma H(t) \dot{D}(t) + \omega_0^2 D(t) = \mathcal{S}(t)$$

其中 $\omega_0$ 是 Hopf-fiber 對 $L_0$ natural length 的 elastic restoring frequency。

**$\omega_0$ 從 $L_0$ 鎖定**（見 §11.8.0）：D(t) 集體模 = W(3) macro Λ-elastic 同一 fiber mode，$L_0 \sim c/H_0$ cosmic-scale natural length → $\omega_0 = c/L_0 \sim H_0$。

過阻尼條件 $\gamma H > 2\omega_0$ 要求 $\gamma \gtrsim 2$（mesh dissipation coupling，O(1)-O(10) 自然量級），此時方程退化為：

$$\boxed{\gamma H(t) \dot{D}(t) + \omega_0^2 [D(t) - D_{\rm eq}(a)] = 0}$$

$D$ 沒有 oscillation，只有 Hubble-paced dissipation-driven relaxation 向 cosmic 即時 equilibrium。

#### 11.8.0 F1a Numerical Lock: $L_0$ as Cosmic-Scale Hopf-Fiber Natural Length（2026-05-08）

**Picture 鎖定**：D(t) anisotropic strain 與 W(3) macro Λ-elastic 是**同一 collective Hopf-fiber mode 的兩個 manifestation**：
- Macro：global fiber 從 cosmic compressed state ($L < L_0$) 向 $L_0$ 鬆弛，表現為加速膨脹（dark energy）
- Micro/anisotropic：$S^2 \times S^1$ 兩成分對 cosmic stretching 響應差異 → $D = D_{S^2} - D_{S^1}$ 各向異性

兩者共享同一 elastic restoring scale。$L_0$ 由 [W(3) cosmology workingdoc](工作文件_W3彈性與暗能量.md) 鎖定為 Hopf-fiber 宇宙級自然長度（today $L < L_0$，damped relaxation 收斂於 $L_0$）。

**$\omega_0$ derivation**：collective fiber elastic mode 在 length-scale $L_0$ 上的 fundamental frequency：

$$\boxed{\omega_0 = \frac{c}{L_0} \sim H_0 \approx 2.2 \times 10^{-18}\,\text{s}^{-1}}$$

**結構意義**：HFT picture 預測 $\omega_0$ 與 $H_0$ **同一量級無 hierarchy**——dark energy scale 即 D(t) elastic restoring scale，兩者本是同一物理。

**Atomic clock bound 轉譯為 $\epsilon/\gamma$ 上界**：代入 $\omega_0^2/(\gamma H_0) = H_0/\gamma$：

$$\left|\frac{\dot\alpha}{\alpha}\right| = k_{\alpha^{-1}} \cdot \frac{H_0}{\gamma} \cdot \epsilon_{\rm imbalance} \cdot D(t_0) = 1.87 \cdot \frac{6.9 \times 10^{-11}}{\gamma} \cdot \epsilon \cdot 1.73 \times 10^{-3}\,\text{yr}^{-1}$$

對齊 Rosenband bound $|\dot\alpha/\alpha| < 10^{-17}$/yr：

$$\boxed{\frac{\epsilon_{\rm imbalance}}{\gamma} \lesssim 4.5 \times 10^{-5}}$$

**Self-consistency check**（β1 picture）：post-EWSB relaxation $\tau_{\rm relax} = \gamma/\omega_0 = \gamma/H_0$。$\gamma \sim O(1)$ → $\tau_{\rm relax} \sim$ Hubble time。Cosmic age $t_0/\tau \sim O(1)$ 給 e-foldings $\sim 1$；natural $\epsilon \sim e^{-t_0/\tau} \sim 0.1$–$0.4$。

但 picture 要求 $\epsilon \lesssim 4.5 \times 10^{-5} \cdot \gamma$——若 $\gamma \sim 1$，需 $\epsilon \sim 10^{-5}$（10+ e-foldings）。

**結論**：$\gamma \gtrsim 10$（強過阻尼，mesh dissipation coupling 偏大）給足夠 e-foldings 使 $\epsilon$ 自然 small。Picture self-consistent 要求 mesh damping 顯著但非極端。

**Regime lock**：
- $\omega_0 \sim H_0$（cosmic Hubble scale，從 $L_0$ first-principles）
- $\gamma \gtrsim 10$（dimensionless mesh damping，picture self-consistency 約束）
- Hubble-paced overdamped relaxation
- β1 near-equilibrium 自然成立

**Falsifiability**：若未來 atomic clock bound tighten 到 $|\dot\alpha/\alpha| < 10^{-19}$/yr 且仍未見 drift → 強迫 $\epsilon/\gamma < 4.5 \times 10^{-7}$，需 $\gamma \gtrsim 100$ 或 $\epsilon$ 極端微小，picture 始壓力但不立即破。

#### F1b lock: Phase-Transition Impulse Source（液態 → 晶態相變）

**HFT 立場**：D(t) 動力學遵從 EWSB phase transition 的 liquid-to-crystal 相變圖景：

| Phase | mesh 狀態 | D 性質 |
|---|---|---|
| **Pre-EWSB（液態）** | 鬆散網格，無 chirality lock，無 rigidity | $D$ ill-defined（無可參考 baseline structure）|
| **EWSB phase transition** | bubble nucleation 結晶化瞬間 | $D$ 從液態 ill-defined 跳變為晶態具體值 $D_*$ |
| **Post-EWSB（晶態）** | mesh 結構鎖定 + 張力連通 | $D$ well-defined，受 cosmic expansion 慢驅動 |

Source term：

$$\mathcal{S}(t) = \underbrace{D_* \cdot \omega_0^2 \cdot \delta(t - t_{\rm EWSB})}_{\text{EWSB impulse}} + \underbrace{\omega_0^2 D_{\rm eq}(a(t))}_{\text{post-EWSB cosmic drive}}$$

**為什麼 phase-transition impulse 對齊 picture**：
- §3.0/§4.2 已建立 EWSB 是**單階段 chirality lock**——鎖定前後是兩個本質不同的 phase
- §10 stage-separated synthesis 已用相同 framing（pre-EWSB 50/50 binomial → EWSB Boltzmann selection → post-EWSB crystallized state）
- Liquid-to-crystal 類比與 SM 觀測對齊：cosmological 觀測無需 pre-EWSB drift（pre-EWSB 在 inflation/reheating 之前，遠超 quasar 觀測 epoch）

#### Post-EWSB Relaxation Profile

過阻尼 solution：

$$D(t) = D_{\rm eq}(a(t)) + [D_* - D_{\rm eq}(a(t))] \cdot e^{-(t - t_{\rm EWSB})/\tau_{\rm relax}}$$

其中 $\tau_{\rm relax} = \gamma H / \omega_0^2$ 是 relaxation timescale。

**今天觀測值 $D(t_0) \approx 0.173\%$**：picture input，等同於 EWSB 鎖定值 + post-EWSB 累積 relaxation 的合計。

#### F1a Atomic Clock Self-Consistency

完整 atomic clock bound 推導見 §11.8.0；β1 near-equilibrium picture 自然 satisfy bound（$\gamma \gtrsim 10$，$\epsilon \lesssim 4.5 \times 10^{-5}$）。

#### 觀測 Signatures + Falsifiable Predictions

**Atomic clock**：$\dot\alpha/\alpha \sim 10^{-17}$ /yr 級或更小（natural compatibility）。

**Quasar absorption (z ~ 2-5)**：$\Delta\alpha/\alpha$ 反映從 z 到今天的 $D$ 變化：

$$\frac{\Delta\alpha}{\alpha}\bigg|_{z} = -k_{\alpha^{-1}} \cdot [D(t_0) - D(t_z)] = -k_{\alpha^{-1}} \cdot \Delta D_{\rm relax}$$

其中 $\Delta D_{\rm relax} = $ post-EWSB relaxation 在 [t_z, t_0] 區間累積。$\Delta D \sim D \cdot \exp(-\Delta t/\tau)$。

對 $\tau \sim$ Hubble timescale: $\Delta D/D \sim O(0.1$–$1)$，$\Delta\alpha/\alpha \sim 0.05$%–$0.3$%。

**Falsifiable signature**：
- Atomic clock 看不到 drift（$\dot\alpha/\alpha < 10^{-17}$）
- Quasar (high-z) **應該**看到 finite drift（$\sim 0.1$%）+ **HFT 14:1 ratio** 對 $\sin^2\theta_W$
- CMB recombination ($z \sim 1100$): drift 接近完整 EWSB 鎖定值

→ **HFT picture 預測**：drift 隨 z 單調漸近 EWSB-lock 值，atomic clock 觀察到的「靜止」是 post-EWSB relaxation 已 saturate 的自然後果，**非缺乏 cosmological drift**。

#### Sub-tasks 完成度

| ID | 內容 | 狀態 |
|---|---|---|
| F1a | $\omega_0$ from $L_0$ | ✓ **Lock**（§11.8.0）：$L_0 \sim c/H_0$ cosmic Hopf-fiber natural length（與 W(3) macro Λ-elastic 同 mode），$\omega_0 = c/L_0 \sim H_0$ |
| F1a' | $\gamma$ dimensionless damping | ✓ Picture-bounded：self-consistency 要求 $\gamma \gtrsim 10$（強過阻尼）使 atomic clock bound 自洽 |
| F1b | $\mathcal{S}(a)$ functional form | ✓ **Phase-transition impulse** lock，對齊 §3.0/§4.2/§10 既有 picture |
| 動力學 regime | Hubble-paced overdamped | ✓ Lock |
| Sub-scenario | β1 near-equilibrium | ✓ Default picture，self-tuned by ~14 Gyr cosmic relaxation |

### 11.9 F1e: $k_\mu$ Cascade-Derived Value（2026-05-07）

$\mu = m_p / m_e$ 漂移由 SM cascade 從 $(\Delta\alpha, \Delta\theta_W)$ 完整 derive——**不是新 sharp test**，是 ELT 觀測對齊用的 consistency check value。

#### Step 1：$m_e$ via Higgs vev

$m_e = y_e v / \sqrt{2}$（假設 $y_e$ Yukawa 拓撲鎖定不變——lepton mass = 垂直軸 Tw integer winding × mesh 張力連通，winding 整數量子化）。

$M_Z$ 假設 mesh structural mass scale 鎖定（Z⁰ = boundary map quantum，與 D 無關）。則：

$$G_F \propto \frac{\alpha}{\sin^2\theta_W (1 - \sin^2\theta_W)}$$

對 $\sin^2 = x = 15/64$：$\frac{d\ln(x(1-x))}{d\ln x} = \frac{1-2x}{1-x} = \frac{34}{49}$

$$\Delta\ln G_F = -k_{\alpha^{-1}} D - \frac{34}{49} k_\theta \cdot D = -\left(\frac{256}{137} + \frac{68}{735}\right) D$$

$v \propto G_F^{-1/2}$：

$$\boxed{k_v = k_{m_e} = \frac{1}{2}\left(\frac{256}{137} + \frac{68}{735}\right) \approx 0.981}$$

#### Step 2：$m_p$ via $\Lambda_{\rm QCD}$（兩 Scenarios）

| Scenario | 物理 | $k_{m_p}$ |
|---|---|---|
| **A — $\Lambda_{\rm QCD}$ mesh-locked**（HFT 預設）| $T_0 = \Lambda_{\rm QCD}^2$ 是 mesh substrate intrinsic baseline tension（v13 既定 input），與 D 解耦 | $0$ |
| **B — $\Lambda_{\rm QCD}$ via GUT running** | $\Lambda_{\rm QCD} \sim M_{\rm GUT} \exp(-2\pi/(b_0\alpha_s))$；GUT scale $\alpha_s$ 漂移指數放大 | $\sim -8 \cdot k_{\alpha^{-1}} \approx -15$ |

**HFT picture 立場（geometric intuition 支持 A）**：
- $\Lambda_{\rm QCD}$ 在 v13 是 mesh substrate baseline tension，不是 GUT-running 派生量
- D 是 $S^2$ vs $S^1$ 的**各向異性 strain**，不影響 mesh **intrinsic** tension scalar
- 強作用是 $H^3$ Link 離散構型 gauge description（§6.3，無 gluons）——$\Lambda_{\rm QCD}$ 不來自連續 RG running
- → **Scenario A 對齊 HFT 整體本體論立場**

#### Step 3：$k_\mu$ Lock（Scenario A）

$$\boxed{k_\mu = k_{m_p} - k_{m_e} \approx 0 - 0.981 = -0.981}$$

對齊 §5.5 +0.023% sin² dressing（$D(t_0) \approx 0.173\%$）：

$$\frac{\Delta\mu}{\mu}\bigg|_{t_0} \approx -0.17\%$$

→ μ 在高紅移**減小約 0.17%**（HFT Scenario A 預測）。

#### Step 4：與 Primary 14:1 Lock 的關係

| 比例 | Scenario A 預測 |
|---|---|
| $\Delta\alpha^{-1}/\alpha^{-1} : \Delta\sin^2/\sin^2$ | $14.0$（primary sharp lock）|
| $\Delta\mu/\mu : \Delta\sin^2/\sin^2$ | $\approx -7.37$ |
| $\Delta\mu/\mu : \Delta\alpha^{-1}/\alpha^{-1}$ | $\approx -0.525$ |

#### Sharp Test：A vs B 觀測分辨

ELT $\Delta\mu/\mu$ 觀測直接區分兩 scenarios：

| 觀測比例 $\|\Delta\mu/\mu\| : \|\Delta\alpha/\alpha\|$ | 結論 |
|---|---|
| $\sim 0.5$ | Scenario A confirmed（$\Lambda_{\rm QCD}$ mesh-locked，HFT 本體論一致）|
| $\sim 16$（指數放大）| Scenario B（$\Lambda_{\rm QCD}$ GUT-running，違反 HFT 預設）|
| 介於兩者 | picture 有額外 D ↔ $\Lambda_{\rm QCD}$ 細節耦合，需要 picture refinement |

**HFT 預測**：Scenario A，$|\Delta\mu/\mu| \approx 0.5 |\Delta\alpha/\alpha|$，符號相反（$\mu$ 與 $\alpha$ anti-correlate）。

---

## §12. 與 v13 既有 Duality 應用的同構性

| Section | Viewpoint 1 | Viewpoint 2 | 收斂 |
|---|---|---|---|
| §4.2 $N_{\rm weak}$ | $S^2$ projection (3/8 × 5/8) | $SU(3)_3$ reps (10×3) | 都 = 30 |
| §A.1 $\alpha^{-1}$ | Knot count (128+9) | Wyler volume | 都 = 137 |
| §A.2 BH 邊界 | $N_{\rm skel}$ topology | Bekenstein-Hawking | 1.4% match |
| **§5/§8 EWSB**（本文件補完）| **A/B sin²-space + Gauss-Bonnet** | **C macro $Z_2$ accounting** | **0.34% match (= $D(t)$ stretch)** |

EWSB 是 v13 中 Epistemological Duality 應用最薄弱的環節——v13 只有 viewpoint C，本文件補完 A 與 B 並 demonstrate 三框架嚴格收斂。

---

## §13. Open Questions + 量化 Tasks

### Open Questions

| ID | 問題 |
|---|---|
| **P9** | Pre-EWSB 50/50 是嚴格還是某 entropy minimization 偏離 |
| **V8** | $\ell_{\rm braid} = 3a/2$ 從 discrete slot counting 嚴格 derive——leading candidate 鎖定（§3.0.8）並 sharp 預測 vacuum shares = $\{5/8, 3/8\}$ EWSB tilt；剩餘需證 (a) Z_3 sector count 嚴格從 trivalent + B_3 lock 為 3，(b) per-sector minimum slot scale 嚴格從 N_Ny=128 + sub-cell 結構 derive 為 $a/2$ |

### 量化 Tasks

| ID | 任務 |
|---|---|
| **F1a** | ✓ **Resolved**（§11.8.0）：$L_0 \sim c/H_0$ cosmic-scale Hopf-fiber natural length（D(t) collective mode = W(3) macro Λ-elastic 同 fiber mode），$\omega_0 = c/L_0 \sim H_0$；$\gamma \gtrsim 10$ from atomic clock self-consistency |
| **F1b** | ✓ **Resolved**（§11.8）：Phase-transition impulse source（液態 → 晶態相變），對齊 §3.0/§4.2/§10 既有 picture |
| **F1c** | ✓ **Resolved**（§11.6）：$k_\theta = 2/15$ from chirality-frozen 2 slots 在 sin² 分母不對稱 scaling |
| **F1d** | ✓ **Resolved**（§11.6）：$k_{\alpha^{-1}} = 256/137$ from $N_{\rm Ny}$ area-scaled + $N_v^2$ 拓撲不變 |
| **F1e** | ✓ **Resolved**（§11.9）：$k_\mu \approx -0.98$ in Scenario A（$\Lambda_{\rm QCD}$ mesh-locked，HFT picture 本體論預設）；Scenario B（GUT-running）給 $\sim -16$；ELT 觀測 $\|\Delta\mu/\mu\|/\|\Delta\alpha/\alpha\|$ 比例直接區分 |
| **F2** | ✓ **Resolved**（§11.6）：$\Delta\alpha^{-1}/\alpha^{-1} : \Delta\sin^2/\sin^2 = 1920/137 \approx 14.0$ 是 picture unique sharp ratio |
| **F3** | 寫入 Paper (A) §EWSB 章節骨幹 |
| **F4** | Knot type → quark flavor mapping + 第一原理推 $m_u/m_d/m_s/m_c/m_b/m_t$ |
| **F5** | 重子 binding energy 結構（3 quark vertex confinement 量化）|
| **F6** | 介子拓撲構型（single-strand connecting 2 vertices 細節）|
| **F7** | EWSB GW pulse spectrum 量化（bubble nucleation broadband + W(2)/W(3) 衰變 sharp components）|

---

## §14. 操作守則

- **v13 主論文不動**——已上 Zenodo（2026-05-05），保留 leading-order zero-free-parameter claim
- **Candidate Y 不動**——已投 FoP（2026-05-03），5.422 leading 與 4σ tension framing 不依賴 micro picture
- **§5 三框架收斂是 macro 結構閉合的核心**——剩餘為純量化 tasks（F1, F2）
- **§3-§9 微觀 picture 是 deeper instantiation**，不替代 macro framework，是其下的具體幾何過程
- **Native space 是 128-slot rational space**——所有公式優先寫成 $2/128$ 而非 $1/64$，避免約分掩蓋結構

### 公理層級透明性（2026-05-07）

HFT 採**單一拓撲公理**（Hopf bundle $S^3 \to S^2$ + trivalent mesh + $Z_3$ vertex + $k=3$ CS truncation + $\mathbb{Z}_2$ chirality）。所有 derivation 從此 follow。「為什麼這個拓撲」是形式系統公理層 boundary，所有 axiomatic 物理理論共同面對——非 HFT 特有缺陷。

**Closure criterion = Stage A 雙重 epistemology 收斂**：
- Forward / Backward derivation 互相 reproduce
- Discrete / Continuous 工具給同一 prediction

兩者收斂即 picture 達認識論最大閉合，不追問 Stage B。

**詳細 epistemological framing 見** [`[DRAFT] 鞍點地圖：三軸雙曲空間與理論的最小包圍.md`](./[DRAFT]%20鞍點地圖：三軸雙曲空間與理論的最小包圍.md)——HFT 是該地圖三層順序湧現結構的具體物理實例，本文件的 derivation chain 是 Stage A 的具體執行。

### 結構性事實

- **Edge fiber pair 無 chirality 自由度**：兩條 identical strands；網路手性鎖在 **vertex W(1) Wr 方向** (CW/CCW)，edge Tw 符號由此派生
- **EWSB = 全域 chirality lock**：單一 chirality choice 同時鎖 vertex W(1) handedness + edge Tw sign + 激活 mesh-wide 張力連通（HFT 「Higgs vev」具體身分）
- **Vacuum baseline shares = $\{5/8, 3/8\}$**：per vertex region $(3/2)t_0 = \cos^2\theta_W$，$w_0 = \sin^2\theta_W$；由 $A:C = 5:3$ × discrete slot $L_e/L_v = 2/3$ 共同 lock
- **Wr 雙重量子化**：accumulation $360°$（vertex-level）、dispersion $120°$/fiber（fiber-level，$Z_3$ 配額）；360° 是 sub-fiber routing 守恆最小量子
- **W(0) 是 $S^2$ substrate**（$N_{\rm skel} \times 5/8 = 85.625$），**不是** vertex 子集；W(1)/W(2)/W(3) 是 vertex 上 excess Wr
- **Stage-separated synthesis**：binomial 分布是 EWSB initial geometric state；v13 Boltzmann 是 final crystallized state——不衝突
- **Vertex 垂直軸 fiber 是 lepton sector 的拓撲位置**；horizontal edge sub-fiber strand 是 quark sector；兩者結構性分離
- **$\rho$ = fiber tension scalar**（非徑向振幅）：$S^1$ fiber 純圓無徑向自由度，所有 DOFs 縱向（phase 縱波 = 光子，tension 縱波 = mass，stress 縱波 = GW）；標準横波是 3D 空間方向投影 emergent

### Picture Narrative Cores

- **質量湧現 = 幾何代價**——picture 整體的 narrative core
- **三力 = bundle 結構複雜度三層次 + 1 個離散 gauge description**：fiber 內部（EM）/ fiber-base interface（Weak）/ vertex braid（Strong）/ substrate（Gravity）
- **4 上同調類精確對應 4 種力**：$H^0$/Gravity、$H^1$/EM、$H^1\to H^2$/Weak、$H^3$/Strong——3 個 propagating stress modes + 1 個離散 gauge description（HFT 不需 gluons）
- **電荷 = fiber holonomy**：lepton 整數電荷 = 垂直軸 integer winding；quark 分數電荷 = sub-fiber + $Z_3$ vertex dispersion 1/3 配額；baryon 整數電荷 emergent from $3 \times 1/3 = 1$
- **Lepton mass 機制**：垂直軸 Tw × mesh 張力連通耦合；HFT 「Higgs vev」= post-EWSB mesh-wide 張力連通本身
- **Generation 數 = winding density 階梯**：1/2/3 對應 e/μ/τ；3 是 information capacity ceiling
- **Strong force 不是 stress mode 是 gauge description**：HFT 不需要 gluons；強作用 reduce 為 vertex $B_3$ braid 離散構型躍遷 + 能量釋放透過 EM/Weak/Gravity stress modes
- **Baryon mass = vertex $B_3$ braid elastic potential**（$\sum T_{\rm strand}$）：與 lepton mass 機制（$H^1$ Twist + Higgs-like）結構分離，精確 match QCD chiral symmetry breaking 觀測
- **W(1) DM 透過 substrate gravity wave passive transport**（海浪推船）：唯一耦合 channel 是 $H^0$；Wr 量子守恆於 propagation；衰變 vs 平移嚴格區分
- **$D(t)$ 是宇宙膨脹的各向異性分量**（§11.2-11.4）：$D(t) = D_{S^2}(t) - D_{S^1}(t)$ 差量，而非 $S^2$ 絕對拉伸；isotropic component（$S^3$ synchronous expansion）對 dimensionless ratios 不可見；$S^1$ 無獨立 anisotropic stretch（phase substrate without length，本體論承諾）；anisotropic source 來自 $W^{(3)}$ stator 雙成分動力學的不同響應（Planck-cell 不可壓縮 vs Hopf-fiber 彈性 with $L_0$）
- **Tw winding（holonomy）vs Tw wave（oscillation）**：兩者在不同 cohomology class——電荷只測量 winding；中微子、光子是 Tw wave 不帶電；W(1) 在 $H^2$ 不在 $H^1$ 故不耦合 EM
- **W± 帶電不對稱性 = horizontal-vertical sector 之間整數 Tw winding 正交轉移**：Z⁰ 是 $H^1\leftrightarrow H^2$ 封閉彈性振盪（winding 守恆於單一 sector），W± 是開放非彈性振盪（winding 在 quark horizontal sub-fiber 與 lepton vertical axis 之間轉移）；這也解釋為什麼 W± 必橋接 quark vertex 與 lepton vertex（如 beta decay）。SM charge conservation 還原為 mesh $H^1$ winding 全域守恆
- **Quark flavor 雙量子數結構**（§7.3、§8.3）：完整 flavor 由 $(n, \text{integer Tw})$ 兩量子數決定——$n \in \{1, 2, 3\}$ 是 strand 在 vertex 內 winding number（決定 generation: u/d, c/s, t/b 三對 mass tier），integer Tw $\in \{0, +1\}$ 決定 charge type（down-type / up-type）。$k=3$ ceiling 同時限定 quark generation、lepton generation、W(n) Wr 階梯——皆是同一 vertex information capacity 的 multi-sector manifestation
- **Baryon Zoo = $B_3$ braid 構型枚舉**（§8.4）：proton ($uud$) = 3×$n=1$ 最低張力；$\Lambda_b$ ($udb$) = 2×$n=1$ + 1×$n=3$，b strand 繞 3 圈撐高張力給 ~6× proton mass。Allowed transitions（衰變）= strand $n$ 降階 + integer Tw 改變，micro 機制透過 W± 正交轉移 winding 至 lepton sector（與 P8 完全橋接）；無 gluon mediation
