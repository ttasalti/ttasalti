# Tarık Tuna Taşaltı

**LLM evaluation researcher** at NOVA FCT, working on [AMALIA](https://amaliallm.pt/), Portugal's national large language model programme.

I work on whether language models actually reason or just land on the right answer, and I do it in English, European Portuguese and Turkish. Next, I want to work on reward signals for RL with LLMs: how reliable step-level rewards need to be, and what models learn when they are wrong.

---

### What I'm working on

At AMALIA I built the reasoning-evaluation stack end to end: the CoT-Pass@k judging stage, custom vLLM serving for reasoning traces up to 64k tokens, and a benchmarking campaign of 22 model configurations across five benchmarks in three languages. That came to 252k generations, each correct one judged three times by up to four judges, or 835k inference calls and 9.26B tokens in total.

The main result came from trying to break it. I planted arithmetic errors inside otherwise correct reasoning chains and the judges accepted them 92–98% of the time; they rejected a solution mainly when its final answer was wrong. So the judge scores whether the chain agrees with the answer, not whether the reasoning is valid, and on current models CoT-Pass@k collapses onto plain Pass@k (the average gap falls from 19.7 to 4.1 points). As a side finding, raising the generation budget alone moves Pass@64 by more than 50 points while that gap stays at zero.

Portuguese and Turkish had little data for this kind of evaluation, so I built it: AIME 2026 translations with native-speaker review, plus two test sets taken from Portuguese national exams and the Turkish mathematics olympiad.

### Research

- **[Does CoT-Pass@k Really Check the CoT? A Multilingual Mathematical Audit](https://arxiv.org/abs/2609.32622)**. First author, accepted at the MRL Workshop @ EMNLP 2026. [arXiv:2609.32622](https://arxiv.org/abs/2609.32622) · [code](https://github.com/ttasalti/evalhub)
- **Cross-Lingual Mathematical Reasoning in LLMs: Benchmarking Base, Non-Think and Think Modes on Multilingual AIME 2026**. First author, abstract in the [UYIK 2026 proceedings](https://www.uyik.org/uploads/uyik-2026-proceedings-book.pdf) (p. 227, ISBN 978-625-90604-0-8)
- **Turkish dataset contribution**, [MRL 2026 Shared Task @ EMNLP](https://github.com/gsaltintas/shared-task-turkish-2026). Co-first author, submitted. 126 native-written cultural-knowledge questions in nine categories, benchmarked against four LLMs.

### Selected repositories and datasets

| | |
|---|---|
| [**evalhub**](https://github.com/ttasalti/evalhub) | CoT-Pass@K judged evaluation for LLM reasoning. Adds a judging stage on top of a Pass@K-only harness, local (vLLM) and cached API judge backends, multilingual math benchmarks, and campaign-level reporting. The code, data tables and figures behind the MRL 2026 paper. |
| [**aime2026-tr-pt**](https://huggingface.co/datasets/tariktuna/aime2026-tr-pt) | AIME 2026 in Turkish and European Portuguese, translated and audited by native speakers. On Hugging Face. |
| [**pt-exams-math-open**](https://huggingface.co/datasets/tariktuna/pt-exams-math-open) | 166 mathematics questions from Portuguese national exams, filtered from [PHEB](https://github.com/AMALIA-LLM/pheb) and converted to open answer. On Hugging Face. |
| [**shared-task-turkish-2026**](https://github.com/gsaltintas/shared-task-turkish-2026) | Turkish cultural-knowledge benchmark for the MRL 2026 shared task: 126 native-written questions across nine categories, quality-controlled and probed with four LLMs. Co-first author. |
| [**coneScenes**](https://github.com/ttasalti/coneScenes) | LiDAR cone detection and localisation for Formula Student Driverless. DBSCAN clustering, rule-based filtering, odometry attachment, and local-to-global coordinate transforms. |
| [**5G-Positioning-Competition**](https://github.com/Teknofest-High5/5G-Positioning-Competition) | TEKNOFEST 2025, Turkcell 5G positioning. Multi-output regression from live radio metrics to coordinates; XGBoost + Optuna, neighbour-cell features. Best mean error 2.7 m, passed the first stage as team lead. |
| [**tt-bootcamp-2025**](https://github.com/ttasalti/tt-bootcamp-2025) | Churn prediction over 10M rows with PySpark, segment-specific XGBoost, out-of-fold threshold selection and counterfactual explanations, plus a DuckDB recommender. 3rd place at Türk Telekom's Big Data Camp. |
| [**Bike-Sharing-Demand-SARIMAX-Hybrid-Models**](https://github.com/ttasalti/Bike-Sharing-Demand-SARIMAX-Hybrid-Models) | Bike-sharing demand forecasting in R: SARIMAX with exogenous regressors, then XGBoost, CatBoost, LightGBM and random forest fitted on the residuals. SARIMAX + XGBoost gives the lowest test RMSE. Part of a series with an [LSTM and STL notebook](https://github.com/ttasalti/Bike-Sharing-Demand-LSTM-STL-Models) and a [UK refugee forecasting study](https://github.com/ttasalti/Forecasting-UK-Refugee-Numbers-ARIMA-SVM-LSTM). |

### Tools

Python · vLLM · SGLang · Hugging Face Transformers · PyTorch · verl · SLURM · PySpark · DuckDB · XGBoost · scikit-learn · R

---

M.Sc. Data Science, graduating December 2026 · Based in Lisbon  
**Applying to PhD programs for Fall 2027 and open to research and engineering roles in LLMs from January 2027**

[LinkedIn](https://www.linkedin.com/in/tariktunatasalti) · [Kaggle](https://www.kaggle.com/tarktunataalt) · tasaltitariktuna@gmail.com
