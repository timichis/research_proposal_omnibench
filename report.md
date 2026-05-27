# Cross-Model Semantic Resonance Bias — Experiment Report

## Edge F1

| Generator \ Reconstructor | gpt-oss-120b | deepseek-3.2 | qwen3-235b-a22b |
| --- | --- | --- | --- |
| **gpt-oss-120b** | 0.786 | 0.254 | 0.801 |
| **deepseek-3.2** | 0.614 | 0.431 | 0.605 |
| **qwen3-235b-a22b** | 0.689 | 0.120 | 0.915 |

## Exact Match Rate (%)

| Generator \ Reconstructor | gpt-oss-120b | deepseek-3.2 | qwen3-235b-a22b |
| --- | --- | --- | --- |
| **gpt-oss-120b** | 50.0% | 22.0% | 46.0% |
| **deepseek-3.2** | 46.0% | 34.0% | 42.0% |
| **qwen3-235b-a22b** | 38.0% | 12.0% | 40.0% |

## Cell Details

| Generator | Reconstructor | Precision | Recall | F1 | EM% | N |
| --- | --- | --- | --- | --- | --- | --- |
| gpt-oss-120b | gpt-oss-120b | 0.840 | 0.751 | 0.786 | 50.0% | 50 |
| gpt-oss-120b | deepseek-3.2 | 0.260 | 0.250 | 0.254 | 22.0% | 50 |
| gpt-oss-120b | qwen3-235b-a22b | 0.863 | 0.763 | 0.801 | 46.0% | 50 |
| deepseek-3.2 | gpt-oss-120b | 0.680 | 0.585 | 0.614 | 46.0% | 50 |
| deepseek-3.2 | deepseek-3.2 | 0.480 | 0.412 | 0.431 | 34.0% | 50 |
| deepseek-3.2 | qwen3-235b-a22b | 0.677 | 0.575 | 0.605 | 42.0% | 50 |
| qwen3-235b-a22b | gpt-oss-120b | 0.706 | 0.679 | 0.689 | 38.0% | 50 |
| qwen3-235b-a22b | deepseek-3.2 | 0.120 | 0.120 | 0.120 | 12.0% | 50 |
| qwen3-235b-a22b | qwen3-235b-a22b | 0.950 | 0.888 | 0.915 | 40.0% | 50 |

## Interpretation

- **Average diagonal F1**: `0.711`
- **Average off-diagonal F1**: `0.514`
- **Semantic resonance bias Δ**: `+0.197`

> WARNING **Evidence of semantic resonance bias detected.** Models reconstruct graphs from their own instructions 0.197 F1 points better than from cross-model instructions.