# perplexity-experiment

# LLM Quantization Perplexity Analysis

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)

This repository contains code and data for analyzing the impact of quantization on the perplexity of open reproductions of large language models (LLMs) (https://github.com/openlm-research/open_llama/tree/main) across different model sizes (3B, 7B, 13B).

## 📊 Results Preview
| Model | FP16 Size | Q3_K Size | Q4_K PPL | Q5_K PPL | Q8_0 PPL |
|-------|-----------|-----------|----------|----------|----------|
| 3B    | 5.6 GB    | 2.1 GB    | 5.76     | 5.75     | 5.72     |
| 7B    | 13.1 GB   | 4.8 GB    | 5.55     | 5.46     | 5.46     |
| 13B   | 24.3 GB   | 8.9 GB    | 5.17     | 5.12     | 5.08     |

Full results: [`/results_common.csv`](/results_common.csv)

## 🛠️ Setup

### Dependencies
- Python 3.9+
- Jupyter Notebook
- Libraries: pandas, matplotlib, numpy, seaborn, os

Install requirements:
```bash
pip install -r requirements.txt
```

## 🧪 Reproduce the Experiment
 1 Run perplexity measurements:

```bash
jupyter notebook notebooks/perplexity_experiment.ipynb
```
 ◦ Modify model_path and quant_type in the notebook.
 
 2 Generate charts:
```bash
jupyter notebook notebooks/perplexity_charts.ipynb
```
 ◦ Uses data/results_common.csv to plot trends.
