# Tarık Tuna Taşaltı

**LLM evaluation researcher** at NOVA FCT, working on [AMALIA](https://amaliallm.pt/), Portugal's national large language model programme.

I work on whether language models actually reason, or just land on the right answer — and I do it in English, European Portuguese and Turkish.

---

### What I'm working on

At AMALIA I built the reasoning-evaluation stack end to end: the CoT-Pass@k judging stage, custom vLLM and SGLang serving for reasoning traces up to 64k tokens, and a benchmarking campaign of 20+ model configurations across five benchmarks in three languages (~230k generations, judged three times each).

The interesting result came from trying to break it. I planted arithmetic errors inside otherwise correct reasoning chains, and the judges accepted them 93–98% of the time. Raising the generation budget alone moved Pass@64 by more than 50 points while the reasoning gap the metric claims to expose stayed at zero.

Portuguese and Turkish had almost no data for this kind of evaluation, so I built it: a translation pipeline with native-speaker review, plus two test sets written from scratch.

### Research

- **Does CoT-Pass@k Really Check the CoT? A Multilingual Mathematical Audit** — first author, under review at the MRL Workshop @ EMNLP 2026
- **Cross-Lingual Mathematical Reasoning in LLMs: Benchmarking Base, Non-Think and Think Modes on Multilingual AIME 2026** — first author, [UYIK 2026 proceedings](https://www.uyik.org/uploads/uyik-2026-proceedings-book.pdf) (p. 227)
- **Turkish dataset contribution**, [MRL 2026 Shared Task @ EMNLP](https://github.com/gsaltintas/shared-task-turkish-2026) — co-first author, submitted. 126 native-written cultural-knowledge questions in nine categories, benchmarked against four LLMs.

### Selected repositories

| | |
|---|---|
| [**evalhub**](https://github.com/ttasalti/evalhub) | CoT-Pass@K judged evaluation for LLM reasoning. Adds a judging stage on top of a Pass@K-only harness, local (vLLM) and cached API judge backends, multilingual math benchmarks, and campaign-level reporting. Research codebase behind a multilingual audit of the metric's judging step. |
| [**shared-task-turkish-2026**](https://github.com/gsaltintas/shared-task-turkish-2026) | Turkish cultural-knowledge benchmark for the MRL 2026 shared task: 126 native-written questions across nine categories, quality-controlled and probed with four LLMs. Co-first author. |
| [**coneScenes**](https://github.com/ttasalti/coneScenes) | LiDAR cone detection and localisation for Formula Student Driverless. DBSCAN clustering, rule-based filtering, odometry attachment, and local-to-global coordinate transforms. |
| [**5G-Positioning-Competition**](https://github.com/Teknofest-High5/5G-Positioning-Competition) | TEKNOFEST 2025, Turkcell 5G positioning. Multi-output regression from live radio metrics to coordinates; XGBoost + Optuna, neighbour-cell features. Best mean error 2.7 m. |
| [**tt-bootcamp**](https://github.com/ttasalti/tt-bootcamp/tree/main/week2/capstone/TarikTunaTasalti) | Churn prediction over 10M rows with PySpark, segment-specific XGBoost, out-of-fold threshold optimisation, counterfactual explanations. 3rd place at Türk Telekom's Big Data Camp. |

### Tools

Python · vLLM · SGLang · Hugging Face Transformers · PyTorch · verl · SLURM · PySpark · DuckDB · XGBoost · scikit-learn · R

---

M.Sc. Data Science, graduating December 2026 · Based in Lisbon  
**Available for full-time roles from January 2027**

[LinkedIn](https://www.linkedin.com/in/tariktunatasalti) · [Kaggle](https://www.kaggle.com/tarktunataalt) · tasaltitariktuna@gmail.com
