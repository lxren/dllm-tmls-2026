---
theme: academic
themeConfig:
  toc: false
hideInToc: true
addons:
  - '@vueuse/motion'

bibliography:
  - id: sutton2019bitter
    author: "Sutton, Richard"
    title: "The Bitter Lesson"
    year: 2019

  - id: chandrasegaran2025rnd1
    author: "Chandrasegaran et al."
    title: "RND1: Simple, Scalable AR-to-Diffusion Conversion"
    year: 2025

  - id: li2025beyondfixed
    author: "Li et al."
    title: "Beyond Fixed: Training-Free Variable-Length Denoising for Diffusion Large Language Models"
    year: 2025

  - id: wang2025timeisafeature
    author: "Wang et al."
    title: "Time Is a Feature: Exploiting Temporal Dynamics in Diffusion Language Models"
    year: 2025

  - id: lu2025adablock
    author: "Lu et al."
    title: "AdaBlock-dLLM: Semantic-Aware Diffusion LLM Inference via Adaptive Block Size"
    year: 2025

  - id: shen2025osdt
    author: "Shen & Ro"
    title: "Beyond Static Cutoffs: One-Shot Dynamic Thresholding for Diffusion Language Models"
    year: 2025

  - id: hersche2025softmasked
    author: "Hersche et al."
    title: "Soft-Masked Diffusion Language Models"
    year: 2025

  - id: wang2025creditdecoding
    author: "Wang et al."
    title: "CreditDecoding: Accelerating Parallel Decoding in Diffusion Large Language Models with Trace Credits"
    year: 2025

  - id: gao2025selfspec
    author: "Gao et al."
    title: "Self Speculative Decoding for Diffusion Large Language Models"
    year: 2025

  - id: gong2025diffucoder
    author: "Gong et al."
    title: "DiffuCoder: Understanding and Improving Masked Diffusion Models for Code Generation"
    year: 2025

  - id: prabhudesai2025diffusion
    author: "Prabhudesai et al."
    title: "Diffusion Beats Autoregressive in Data-Constrained Settings"
    year: 2025

  - id: ni2025diffusion
    author: "Ni et al."
    title: "Diffusion Language Models are Super Data Learners"
    year: 2025

  - id: du2025understanding
    author: "Du et al."
    title: "Understanding the Limitations of Diffusion LLMs through a Probabilistic Perspective"
    year: 2025

  - id: sun2025why
    author: "Sun et al."
    title: "Why Mask Diffusion Does Not Work"
    year: 2025

  - id: guidelabs2025causal
    author: "Guide Labs"
    title: "Causal Diffusion Language Models"
    year: 2025

  - id: he2025ultrallada
    author: "He et al."
    title: "UltraLLaDA: Scaling the Context Length to 128K for Diffusion Large Language Models"
    year: 2025

  - id: cheng2025sdar
    author: "Cheng et al."
    title: "SDAR: A Synergistic Diffusion-AutoRegression Paradigm for Scalable Sequence Generation"
    year: 2025

  - id: zhang2025syntaxguided
    author: "Zhang et al."
    title: "Syntax-Guided Diffusion Language Models with User-Integrated Personalization"
    year: 2025

  - id: chen2025coda
    author: "Chen et al."
    title: "CoDA: Coding LM via Diffusion Adaptation"
    year: 2025

  - id: zhu2025lladamoE
    author: "Zhu et al."
    title: "LLaDA-MoE: A Sparse MoE Diffusion Language Model"
    year: 2025

  - id: ye2025dream7b
    author: "Ye et al."
    title: "Dream 7B: Diffusion Large Language Models"
    year: 2025

  - id: khanna2025mercury
    author: "Khanna et al."
    title: "Mercury: Ultra-Fast Language Models Based on Diffusion"
    year: 2025

  - id: zhu2025llada15
    author: "Zhu et al."
    title: "LLaDA 1.5: Variance-Reduced Preference Optimization for Large Language Diffusion Models"
    year: 2025

  - id: nie2025largelldm
    author: "Nie et al."
    title: "Large Language Diffusion Models"
    year: 2025

  - id: wang2025remasking
    author: "Wang et al."
    title: "Remasking Discrete Diffusion Models with Inference-Time Scaling"
    year: 2025

  - id: huang2025remedi
    author: "Huang et al."
    title: "Don't Settle Too Early: Self-Reflective Remasking for Diffusion Language Models"
    year: 2025

  - id: xiong2025controllable
    author: "Xiong et al."
    title: "Unveiling the Potential of Diffusion Large Language Model in Controllable Generation"
    year: 2025

  - id: tseng2025dllmsurvey
    author: "Tseng et al."
    title: "Diffusion-based Large Language Models Survey"
    year: 2025

  - id: li2025dlmsurvey
    author: "Li et al."
    title: "A Survey on Diffusion Language Models"
    year: 2025

  - id: cola
    author: "Guo et al."
    title: "Continuous Latent Diffusion Language Model"
    year: 2026

  - id: ELF
    author: "Hu et al."
    title: "ELF: Embedded Language Flows"
    year: 2026

  - id: BitLM
    author: "Zhuang et al."
    title: "BitLM: Unlocking Multi-Token Language Generation with Bitwise Continuous Diffusion"
    year: 2026

  - id: CoBit
    author: "Batzolis et al."
    title: "CoBit: Language Modeling with Bitstream Diffusion"
    year: 2026

---
# dLLM — Rethinking Generation Beyond Autoregressive Models
## ICLR Blogpost 2026 | ICML 2026 Presentation
<br>

### Suhas Pai & Xiaojun Ren
### Fruitless Labs

---

# What is a diffusion Large Language Model?

> TLDR: Diffusion Large Language Models (dLLMs) provide an alternative to autoregressive Transformers, supporting parallel token generation and flexible infilling. They excel in structured, long-horizon, or data-constrained settings.

*Parallel token generation · Flexible infilling · Data efficiency*

<div class="w-1/2">
    <img src="https://substackcdn.com/image/fetch/$s_!2Fk1!,w_1456,c_limit,f_webp,q_auto:good,fl_lossy/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F0de995b3-50a1-4f6b-912a-c7ff16ac8600_800x495.gif" alt="LLaDA" class="w-full rounded shadow" />
</div>

<Footnotes separator>
  <Footnote :number="1">Nie et al. (2025) — Large Language Diffusion Models (LLaDA)</Footnote>
</Footnotes>

---

# The Problem with Autoregressive Models

Most language models follow a time-tested recipe: a **Transformer backbone** trained with a **next-token prediction** objective, generating left to right. 

ARMs factorize the joint probability of a sequence of length *T* as a product of next-step conditionals:

$$p(x_{1:T}) = \prod_{t=1}^{T} p(x_t \mid x_{<t})$$

Where:
- $p(x_{1:T})$ — joint probability of the entire sequence
- $p(x_t \mid x_{<t})$ — probability of the next token given all previous tokens
- $x_{<t} = (x_1, x_2, \ldots, x_{t-1})$ — the prefix up to time step $t-1$

<Footnotes separator>
  <Footnote :number="1">Sutton (2019) — The Bitter Lesson</Footnote>
</Footnotes>
---

# Structural Limitations of ARMs

1. **Sequential bottleneck** — latency scales with output length
2. **Error snowball** — one wrong token poisons all subsequent context
3. **No revision** — committed tokens can never be edited in-place
4. **Token-level objective** — optimizes per-token likelihood, not sequence-level goals; poor long-horizon planning
5. **Hallucination amplification** — wrong tokens become future context, producing coherent but factually wrong narratives
6. **Representation cost** — some distributions require super-polynomial AR size vs. latent-variable models

---

# Masked Diffusion: The Core Idea
<span>Instead of generating left-to-right, masked diffusion works in two phases:</span>
<div class="flex items-start gap-8">
  <div class="w-1/2">
    <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/MaskedDiffusion-1400.webp" alt="Description" class="w-full rounded shadow" />
  </div>
  <div class="w-1/2 flex flex-col justify-center">
    <p><strong>Forward process</strong> — gradually replace tokens with <code>[MASK]</code>:</p>
    <ul>
      <li>At $t = 0.2$: <code>He invented the [MASK] as a means to [MASK] vengeance upon [MASK] detractors</code></li>
      <li>At $t = 0.8$: <code>[MASK] invented [MASK] [MASK] [MASK] means [MASK] exact vengeance [MASK] [MASK]</code></li>
    </ul>
  </div>
</div>

<Footnotes separator>
  <Footnote :number="1">Nie et al. (2025) — Large Language Diffusion Models (LLaDA)</Footnote>
</Footnotes>

---

# Masked Diffusion: The Core Idea
<span>Instead of generating left-to-right, masked diffusion works in two phases:</span>
<div class="flex items-start gap-8">
  <div class="w-1/2">
    <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/MaskedDiffusion-1400.webp" alt="Description" class="w-full rounded shadow" />
  </div>
  <div class="w-1/2 flex flex-col justify-center">
    <p><strong>Reverse process</strong> — iteratively predict and "lock in" tokens until fully unmasked:</p>
    <table>
      <thead>
        <tr>
          <th>Step</th>
          <th>Output</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Step 0</td>
          <td><code>[MASK] [MASK] [MASK] [MASK] [MASK]</code></td>
        </tr>
        <tr>
          <td>Step K/2</td>
          <td><code>Yes, [MASK] is an island [MASK] Yemen.</code></td>
        </tr>
        <tr>
          <td>Step K</td>
          <td><code>Yes, Socotra is an island in Yemen.</code> ✓</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

---

# Masked Diffusion vs BERT

<span>Learning objective looks similar to masked language modeling (BERT) or denoising autoencoding (BART)</span>
<div class="flex items-start gap-8">
  <div class="w-1/2">
    <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/MaskedDiffusion-1400.webp" alt="Masked Diffusion" class="w-full rounded shadow" />
  </div>
  <div class="w-1/2 flex flex-col justify-center">
    <p><strong>Key Distinction</strong></p>
    <p>Unlike BERT/BART, the masking rate <em>t</em> varies continuously per example</p>
    <p>The model learns to denoise at <em>every</em> noise level, not just a fixed corruption rate</p>
  </div>
</div>

---

# Forward Process

<div class="flex gap-8 items-start">
  <div class="flex flex-col gap-2 w-1/2">
    <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/ForwardProcessA-1400.webp" class="w-full object-contain rounded shadow" />
    <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/ForwardProcessB-1400.webp" class="w-full object-contain rounded shadow" />
  </div>
  <div class="w-1/2 flex flex-col justify-start gap-3 [&>p]:mb-1">
    <p>The model predicts masked tokens in <em>x_t</em>, minimising a weighted cross-entropy over masked positions.</p>
    <p>The weighting term <em>w(t)</em> prevents heavily-masked examples from dominating the training signal; one common choice is <em>w(t) = 1/t</em>.</p>
    <p>In BERT the masking rate is fixed; in masked diffusion <em>t</em> varies per example — the model learns to denoise at every noise level.</p>
  </div>
</div>

$$\mathcal{L}(\theta) = \mathbb{E}_{x_0, t, x_t} \!\left[ w(t) \sum_{i \in \mathcal{M}(x_t)} -\log p_\theta(x_{0,i} \mid x_t, t) \right]$$

---

# Reverse Process

<div class="flex gap-8 items-start">
  <div class="flex flex-col gap-2 w-1/2">
    <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/ReverseProcess-1400.webp" class="w-full object-contain rounded shadow" />
    <div class="flex flex-col justify-start gap-3 [&>p]:mb-1">
      <p class="mt-0"><strong>Note:</strong> At inference the full output starts masked and is gradually unmasked, which is a discrepancy from training where only a fraction of tokens are masked.</p>
    </div>
  </div>
  <div class="w-1/2 flex flex-col justify-start gap-3 [&>p]:mb-1">
    <p>For a given prompt, the output is initialised as <code>L</code> number of <code>[MASK]</code> tokens, where <code>L</code> is a hyperparameter.</p>
    <p>The reverse process runs for <code>K</code> denoising steps. At each step the model predicts all <code>[MASK]</code> positions <strong>in parallel</strong>, then:</p>
    <ul>
      <li><strong>Commits</strong> high-confidence tokens by unmasking</li>
      <li><strong>Remasks</strong> low-confidence tokens for further refinement</li>
    </ul>
    <p>Generation stops after <code>K</code> steps; tokens after the first <code>&lt;EOS&gt;</code> are discarded.</p>
  </div>
</div>
---

# How to Train Your Own dLLM

<div class="flex flex-col gap-3">
  <p><strong>Training pipeline:</strong> Pre-training → Midtraining/Annealing → Instruction Tuning → RL</p>
  <div class="w-3/4 mx-auto">
    <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/TrainingPipeline-1400.webp" class="w-full object-contain rounded shadow" />
  </div>
  <span><i> dLLMs can be trained from scratch <em>or</em> adapted from an existing ARM via continued pre-training with a bidirectional attention mask.</i></span>
</div>

<Footnotes separator>
  <Footnote :number="1">Chandrasegaran et al. (2025) — RND1: Simple, Scalable AR-to-Diffusion Conversion</Footnote>
</Footnotes>

---

# Advantages Over ARMs

| | |
|-----------|-------------|
| **Any-order generation** | tokens predicted in any order, not locked to left-to-right |
| **In-place revision** | tokens can be remasked and regenerated at any point |
| **Parallel token prediction** | all masked positions predicted simultaneously |
| **Structured infilling** | provide a JSON/code template; dLLM fills the blanks, guaranteeing format adherence |

<div class ="w-3/4 mx-auto">
  <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/StructuredInfilling-1400.webp" class="w-full object-contain rounded shadow" />
</div>

---

# Decoding Strategies

<span><i>how to decide which tokens to commit at each step</i></span>

| Strategy | Mechanism |
|----------|-----------|
| **Confidence-Based** | Lock in highest-probability tokens first |
| **Entropy-Based** | Commit lowest-entropy positions — more robust |
| **Margin-Based** | Commit when gap between top-1 and top-2 is large |
| **PC Sampler** | Position-calibrated to suppress left-side bias |
| **EB Sampler** | Entropy-bounded: commit until entropy budget is spent |

<Footnotes separator>
  <Footnote :number="1">Gao et al. (2025) — Self Speculative Decoding for Diffusion LLMs</Footnote>
  <Footnote :number="2">Wang et al. (2025) — Remasking Discrete Diffusion Models with Inference-Time Scaling</Footnote>
  <Footnote :number="3">Zhang et al. (2025) — Syntax-Guided Diffusion Language Models with User-Integrated Personalization</Footnote>
</Footnotes>

---

# Pitfall 1: Fixed Output Length
**Problem:** Unlike ARMs, dLLMs must pre-allocate output length before generation
- Too short → truncation or skipped reasoning steps
- Too long → neural degeneration + expensive quadratic attention

---

# Pitfall 1: Fixed Output Length

**Solution — DAEDAL** *(Dynamic Adaptive Length Expansion)*
1. Start with short length (64–128 tokens); run one denoising step
2. Average `<EOS>` probability at tail — if below threshold $T$, extend
3. During denoising, insert `[MASK]` tokens at lowest-confidence positions to allow local expansion

<div class ="mx-auto">
  <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/DAEDAL-1400.webp" class="w-full object-contain rounded shadow" />
</div>

<Footnotes separator>
  <Footnote :number="1">Li et al. (2025) — Beyond Fixed: Training-Free Variable-Length Denoising for Diffusion LLMs</Footnote>
</Footnotes>

---

# Pitfall 2: Fixed Denoising Budget
**Problem:** Too few steps → incomplete answer. Too many → **temporal oscillation** (model overshoots and drifts away from a correct intermediate answer).

---

# Pitfall 2: Fixed Denoising Budget

**Solution — Temporal Semantic Entropy (TSE) + Self-Consistency Voting**
- TSE measures entropy over semantic clusters of intermediate answers; high TSE flags uncertain queries
- **Temporal Self-Consistency Voting** selects the final answer by majority vote across all denoising steps, with exponential weighting toward later steps

<Footnotes separator>
  <Footnote :number="1">Wang et al. (2025) — Time Is a Feature: Exploiting Temporal Dynamics in Diffusion LLMs</Footnote>
  <Footnote :number="2">Huang et al. (2025) — Don't Settle Too Early: Self-Reflective Remasking for Diffusion LLMs</Footnote>
</Footnotes>

---

# Pitfall 3: Fixed Block Size

**Problem:** For long outputs, tokens are divided into sequential blocks. Fixed block size causes:
- **Late decoding overhead** — high-confidence tokens outside the current block wait unnecessarily
- **Premature decoding error** — low-confidence tokens get locked in before sufficient context is available

---

# Pitfall 3: Fixed Block Size

**Solution — AdaBlock**

<div class ="w-2/3 mx-auto">
  <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/ConfidenceLandscape-1400.webp" class="w-full object-contain rounded shadow" />
</div>

The confidence landscape has three regions: *high-confidence plateau*, *volatility band* (where active decoding happens), and *low-confidence floor*. AdaBlock draws block boundaries at **semantic delimiters** (newlines, periods) identified by their confidence exceeding a threshold $T$ — making each block a self-contained semantic unit.

<Footnotes separator>
  <Footnote :number="1">Lu et al. (2025) — AdaBlock-dLLM: Semantic-Aware Diffusion LLM Inference via Adaptive Block Size</Footnote>
</Footnotes>

---

# Pitfall 4: Static Confidence Threshold
**Problem:** Mean confidence follows an **inverted-U shape** across denoising steps — low early, peaks mid-way, low again at the end.

<div class ="w-3/4 mx-auto">
  <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/ConfidenceCurves-1400.webp" class="w-full object-contain rounded shadow" />
</div>

---

# Pitfall 4: Static Confidence Threshold
**Solution — Dynamic $\tau$:** Use the task's confidence trajectory as its signature.

Set threshold adaptively per task type (e.g. GSM8K vs. GPQA datasets have distinct signatures).

<Footnotes separator>
  <Footnote :number="1">Shen & Ro (2025) — Beyond Static Cutoffs: One-Shot Dynamic Thresholding for Diffusion LLMs</Footnote>
</Footnotes>

---

# Pitfall 5: Information Not Carried Across Denoising Steps

**Problem:** At step $p$: model sees `Michael [MASK] to New York` and predicts probabilities `went: 0.4`, `moved: 0.3` — but threshold not met, so token stays masked. 

At step $p+1$, those probabilities are **discarded entirely** and recomputed from scratch.

---

# Pitfall 5: Information Not Carried Across Denoising Steps

**Solutions:**
- **Soft Masking** <sup>1</sup> — instead of a hard `[MASK]`, interpolate the embedding between `[MASK]` and a weighted sum of top-k token embeddings, scaled by prediction confidence $\alpha$. Applied to ~80% of steps, most effective in the first 20%.
- **CreditDecoding** <sup>2</sup> — maintain a running credit score $C_t(i,v)$ per position and token; inject it into logits at the next step with decay factor $\gamma$.

<Footnotes separator>
  <Footnote :number="1">Hersche et al. (2025) — Soft-Masked Diffusion Language Models</Footnote>
  <Footnote :number="2">Wang et al. (2025) — CreditDecoding: Accelerating Parallel Decoding in Diffusion LLMs</Footnote>
</Footnotes>

---

# Pitfall 6: Entropy Sink Phenomenon
Confidence-based unmasking tends to favor tokens near the prefix, inducing a left-to-right AR pattern — the very behavior dLLMs are meant to escape.

**Quantified by:** *Local AR-ness* (contiguous windows) and *Global AR-ness* (leftmost unmasked proportion). Models adapted from AR bases show higher AR-ness than models trained from scratch. Increasing temperature reduces AR-ness by flattening distributions.

---

# Future Directions: Three Bets

### ⚡ The Latency Bet
Parallel generation *should* be faster — but in practice, multiple denoising steps + blockwise decoding narrow the gap considerably. Reducing steps helps latency but hurts quality. 

---

# Future Directions: Three Bets

### 📊 The Data Efficiency Bet

In **data-limited regimes**, dLLMs have a clear edge:
- ARMs benefit from data repetition for only **~4 epochs** before saturation
- dLLMs benefit for up to **~100 epochs**; best validation loss can occur at **~500 epochs** vs ~50 for ARMs

As unique high-quality data becomes scarcer, dLLMs can extract signal from the same data far longer. 

<Footnotes separator>
  <Footnote :number="1">Prabhudesai et al. (2025) — Diffusion Beats Autoregressive in Data-Constrained Settings</Footnote>
  <Footnote :number="2">Ni et al. (2025) — Diffusion Language Models are Super Data Learners</Footnote>
  <Footnote :number="3">Cheng et al. (2025) — SDAR: A Synergistic Diffusion-AutoRegression Paradigm</Footnote>
</Footnotes>

---

# Future Directions: Three Bets

### 📊 The Data Efficiency Bet

<div class="flex gap-4 items-start">
  <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/ScalingLawsA-1400.webp" class="w-1/2 object-contain rounded shadow" />
  <img src="https://iclr-blogposts.github.io/2026/assets/img/2026-04-27-dllm/ScalingLawsB-1400.webp" class="w-1/2 object-contain rounded shadow" />
</div>

---


# Future Directions: Three Bets

### 🧠 The Hybrid Reasoning Bet
Use **diffusion for planning and reasoning** (iterative, revisable, non-linear) and **AR for final output generation** (stable, fast, left-to-right). This plays to each paradigm's natural strengths. 

---

# Open Problems

**Three open critiques:**

1. **Any-order training wastes capacity** — left-to-right and right-to-left orders are easiest to learn due to language's Markovian nature. Training on all orders forces the model to spend capacity on unnatural, hard orders.

2. **Marginal, not joint prediction** — the denoiser predicts each masked position independently. Sampling multiple tokens in parallel has no guarantee of joint coherence across positions.

3. **Train–inference mismatch** — confidence-based decoding makes inference nearly autoregressive, undermining the diverse masking patterns seen during training.

<Footnotes separator>
  <Footnote :number="1">Du et al. (2025) — Understanding the Limitations of Diffusion LLMs through a Probabilistic Perspective</Footnote>
  <Footnote :number="2">Sun et al. (2025) — Why Mask Diffusion Does Not Work</Footnote>
  <Footnote :number="3">Tseng et al. (2025) — Diffusion-based Large Language Models Survey</Footnote>
  <Footnote :number="4">Li et al. (2025) — A Survey on Diffusion Language Models</Footnote>
</Footnotes>

---

# Continuous Diffusion Large Language Models
- Discrete diffusion iterates over the token space
- Continuous diffusion iterates over the concept space

<div class="flex justify-center items-center h-64 relative mt-8">

  <div
    v-motion
    :initial="{ x: -10, opacity: 1 }"
    :enter="{ x: -100, opacity: 1, transition: { duration: 1800 } }"
    :leave="{ x: 0, opacity: 0.8, transition: { duration: 1800 } }"
    class="absolute w-52 h-52 rounded-full flex items-center justify-center"
    style="background: rgba(99, 102, 241, 0.5); border: 2px solid rgb(99, 102, 241); left: calc(50% - 160px);"
  >
    <span class="text-center text-sm font-semibold text-indigo-900 px-6 leading-tight">Global Semantic Planning</span>
  </div>

  <div
    v-motion
    :initial="{ x: 10, opacity: 1 }"
    :enter="{ x: 100, opacity: 1, transition: { duration: 1800 } }"
    :leave="{ x: x0, opacity: 0.8, transition: { duration: 1800 } }"
    class="absolute w-52 h-52 rounded-full flex items-center justify-center"
    style="background: rgba(234, 88, 12, 0.5); border: 2px solid rgb(234, 88, 12); left: calc(50% - 48px);"
  >
    <span class="text-center text-sm font-semibold text-orange-900 px-6 leading-tight">Local Lexical Realization</span>
  </div>

</div>

---

# Where Do We Add Noise in Continuous dLLMs?

<div class ="w-1/3 mx-auto">
  <img src="./AddNoise.png" class="w-full object-contain rounded shadow" />
</div>

---

# Add Noise to Token Embeddings

**Flow Matching:** Learn a velocity field that pushes noisy representations towards valid text representations

<div class ="w-3/4 mx-auto">
  <img src="./VelocityField.png" class="w-full object-contain rounded shadow" />
</div>
<Footnotes separator>
  <Footnote :number="1">Hu et al. (2026) — ELF: Embedded Language Flows</Footnote>
</Footnotes>

---

# Add Noise to Token Embeddings
<div class ="w-3/4 mx-auto">
  <h3 class="text-sm text-gray-500 mt-1">
  Training
  </h3>
  <img src="./EmbeddingLanguageFlows.png" class="w-full object-contain rounded shadow" />
</div>
<div class ="w-3/4 mx-auto">
  <h3 class="text-sm text-gray-500 mt-1">
  Inference
  </h3>
  <img src="./ELFInference.png" class="w-full object-contain rounded shadow" />
</div>


<Footnotes separator>
  <Footnote :number="1">Hu et al. (2026) — ELF: Embedded Language Flows</Footnote>
</Footnotes>

---

# Add Noise to Learned Text Latents
#### Components:
1. A text VAE (Variational Autoencoder)
2. A block causal diffusion Transformer

<div class ="w-3/4 mx-auto">
  <img src="./ContinuousLatentDLM.png" class="w-full object-contain rounded shadow" />
</div>
<Footnotes separator>
  <Footnote :number="1">Guo et al. (2026) — Continuous Latent Diffusion Language Model</Footnote>
</Footnotes>


---

# Add Noise to Binary Token Codes

For a vocabulary of size $V$, each token ID $y_i \in \{0, \dots, V - 1\}$ is mapped to a $B$-bit binary code, where $B$ is the binary code length.

<div class="mt-1 p-1 bg-gray-50 dark:bg-white/5 rounded-lg shadow-sm">
  <div class=" leading-relaxed">
    
  $$
  \phi(y_i) = 2 \cdot \text{bin}_B(y_i) - 1 \in \{-1, 1\}^B
  $$

  </div>
</div>

<div class ="w-3/4 mx-auto">
  <img src="./BitLM.png" class="w-full object-contain rounded shadow" />
</div>
<Footnotes separator>
  <Footnote :number="1">Zhuang et al. (2026) — BitLM: Unlocking Multi-Token Language Generation with Bitwise Continuous Diffusion</Footnote>
</Footnotes>

---

# Add Noise to A Whole A** Bitstream

<div class="flex gap-8 items-start">
  <div class="w-1/2">
    <img src="./BitStreamDiffusion.png" class="w-full object-contain rounded shadow" />
  </div>
  <div class="w-1/2 flex flex-col gap-4">
    <span><strong>Standard LLM:</strong></span>

$$\text{Logits} = B \times T \times V$$

<span><strong>CoBit:</strong></span>

$$\text{Logits} = B \times T \times \lceil \log_2 V \rceil$$

<span>Where $B$ is batch size, $T$ is output tokens, and $V$ is vocabulary size.</span>
  </div>
</div>

<Footnotes separator>
  <Footnote :number="1">Batzolis et al. (2026) — CoBit: Language Modeling with Bitstream Diffusion</Footnote>
</Footnotes>

---
class: text-sm
---

# The Continuous dLLM Landscape

| **Paper** | **Representation** | **Generation Style** |
|---|---|---|
| **Cola DLM** | Learned semantic latents | Block-causal latent diffusion |
| **RePlaid** | Learned continuous token embeddings | Continuous token-aligned diffusion |
| **BitLM** | Fixed binary token IDs | Causal backbone + blockwise bit diffusion |
| **ELF** | Continuous token embeddings | Flow matching until final token decoding |
| **LDLM** | Jointly learned diffusion-friendly latents | Latent diffusion |
| **TextLDM** | TextVAE latents aligned to a frozen LM | Latent DiT + flow matching |
| **Entropy-gated Bitstream Diffusion** | Whole-sequence binary bitstreams | Parallel bitstream diffusion |

---

# Key Observations From Continuous dLLMs

- The right representation matters more than denoising
- Reconstruction quality is not a good proxy for generation quality
- Perplexity is not a good proxy for generation quality in continuous diffusion models

---

# Future Direction: Latent Space Engineering
<div class ="w-1/3 mx-auto">
  <img src="./LatentSpaceEngineering.png" class="w-full object-contain rounded shadow" />
</div>

---

# Future Direction: Native Multi-Modality

Can all be represented in the same latent space

<div class="flex flex-col items-center gap-4 mt-4">
  <div class="grid grid-cols-2 gap-4 w-full">
    <div class="h-36 rounded-2xl flex items-center justify-center shadow-md" style="background: rgba(99, 102, 241, 0.15); border: 2px solid rgb(99, 102, 241);">
      <span class="text-xl font-semibold text-indigo-700">Text</span>
    </div>
    <div class="h-36 rounded-2xl flex items-center justify-center shadow-md" style="background: rgba(234, 88, 12, 0.15); border: 2px solid rgb(234, 88, 12);">
      <span class="text-xl font-semibold text-orange-700">Image</span>
    </div>
    <div class="h-36 rounded-2xl flex items-center justify-center shadow-md" style="background: rgba(22, 163, 74, 0.15); border: 2px solid rgb(22, 163, 74);">
      <span class="text-xl font-semibold text-green-700">Speech</span>
    </div>
    <div class="h-36 rounded-2xl flex items-center justify-center shadow-md" style="background: rgba(217, 70, 239, 0.15); border: 2px solid rgb(217, 70, 239);">
      <span class="text-xl font-semibold text-fuchsia-700">Video</span>
    </div>
  </div>
  <div class="w-full h-16 rounded-2xl flex items-center justify-center shadow-md" style="background: rgba(148, 163, 184, 0.15); border: 2px solid rgb(148, 163, 184);">
    <span class="text-xl font-semibold text-slate-500">...</span>
  </div>
</div>

---

# 6 Months Ago

<div class ="w-2/3 mx-auto">
  <img src="./Tweets.png" class="w-full object-contain rounded shadow" />
</div>

# 6 Months Later

<div class="grid grid-cols-4 gap-4 mt-8 items-center">
  <div class="flex items-center justify-center">
    <img src="./Radar.png" class="w-full object-contain" />
  </div>
  <div class="flex items-center justify-center">
    <img src="./GDM.png" class="w-2/3 object-contain" />
  </div>
  <div class="flex items-center justify-center">
    <img src="./InceptionLabs.webp" class="w-2/3 object-contain" />
  </div>
  <div class="flex items-center justify-center">
    <img src="./ByteDanceSeed.jpg" class="w-full object-contain" />
  </div>
</div>


---


# Conclusion

>dLLMs are pretty cracked, however

| Use dLLMs when… | Stick with ARMs when… |
|---|---|
| Data is the bottleneck, not compute | Latency-sensitive streaming |
| Infilling / structured editing is core | Purely left-to-right generation |
| Non-linear reasoning benefits from revision | Serving efficiency at scale |


**Some Ideas:** hybrid systems — diffusion for planning and reasoning, autoregressive for final output generation

**Other promising futures:** unlocking latent space engineering and true multi-modality

---
layout: center
---

# Thank You
<div class ="w-1/3 mx-auto">
  <img src="./FLL.jpeg" class="w-full object-contain rounded shadow" />
</div>
<div class="text-center mt-4">
  <span class="text-gray-400">iclr-blogposts.github.io/2026/blog/2026/dllm/</span>
  <br>
  <span class="text-gray-400">github.com/piesauce/awesome-dLLM-resources</span>
</div>
