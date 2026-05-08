# Day 22 Submission Summary

## Submission Option

I am submitting **Option B - Professional**:

- Core submission: public GitHub repo with executed notebook, screenshots, and reflection.
- Bonus add-on: DPO adapter pushed to HuggingFace Hub with model card.

## Links

- HuggingFace DPO adapter: https://huggingface.co/StevenMup/lab22-dpo-vn
- GitHub repo: https://github.com/StevenMup2004/Day22-Track3-DPO-Alignment-Lab.git

## Main Evidence

| Requirement | Evidence |
|---|---|
| Executed notebook output | `notebooks/Lab22-DPO-ORPO.ipynb` |
| Reflection | `submission/REFLECTION.md` |
| Required screenshots | `submission/screenshots/` |
| HF adapter upload | `https://huggingface.co/StevenMup/lab22-dpo-vn` |
| HF model card | Included in the HuggingFace repo; describes base model, datasets, hyperparameters, and evaluation results |

## Run Summary

| Item | Value |
|---|---|
| Compute tier | Kaggle T4 |
| GPU | Tesla T4, 15.6 GB reported by notebook |
| Base model | `unsloth/Qwen2.5-3B-bnb-4bit` |
| SFT data | `5CD-AI/Vietnamese-alpaca-gpt4-gg-translated`, 1,000 samples |
| Preference data | `argilla/ultrafeedback-binarized-preferences-cleaned`, 2,000 pairs |
| SFT final train loss | `1.5770` |
| DPO final loss | `0.7901` |
| DPO beta | `0.1` |
| DPO learning rate | `5e-7` |
| End chosen reward | `-0.699` |
| End rejected reward | `-0.891` |
| End reward gap | `+0.192` |
| Judge model | `gpt-4o-mini` |
| NB4 judge summary | SFT-only `1/8`, SFT+DPO `1/8`, tie `6/8` |
| GGUF smoke | `Qwen2.5-3B.Q4_K_M.gguf`, llama-cpp-python Vietnamese response |

## Benchmark Summary

| Benchmark | SFT-only | SFT+DPO | Delta |
|---|---:|---:|---:|
| IFEval | 0.000 | 0.000 | +0.000 |
| GSM8K | 1.000 | 1.000 | +0.000 |
| MMLU sampled | 0.667 | 0.667 | +0.000 |
| AlpacaEval-lite | 0.500 | 0.500 | +0.000 |

## Screenshot Checklist

| File | Status | Notes |
|---|---|---|
| `submission/screenshots/01-setup-gpu.png` | Done | Shows Kaggle T4/GPU setup |
| `submission/screenshots/02-sft-loss.png` | Done | SFT loss curve |
| `submission/screenshots/03-dpo-reward-curves.png` | Done | Chosen/rejected rewards and reward gap |
| `submission/screenshots/04-side-by-side-table.png` | Done | SFT vs SFT+DPO comparison table |
| `submission/screenshots/05-judge-output.png` | Done | API judge verdicts |
| `submission/screenshots/06-gguf-smoke.png` | Done | GGUF Q4_K_M smoke output |
| `submission/screenshots/07-benchmark-comparison.png` | Done | Benchmark comparison chart |

## Rubric Checklist

| Rubric item | Status | Evidence / action |
|---|---|---|
| NB1 SFT adapter config exists | Evidence in notebook; local artifact not present | `notebooks/Lab22-DPO-ORPO.ipynb`, SFT section |
| NB1 SFT loss decreases | Done | `02-sft-loss.png` |
| NB1 sample generation printed | Done | Executed notebook output |
| NB2 preference data parquet | Evidence in notebook; local artifact not present | Notebook shows `data/pref/train.parquet` written |
| NB2 3 inspected examples | Done | Executed notebook output |
| NB3 DPO adapter config exists | Uploaded to HF; local artifact not present | HF link + notebook output |
| NB3 reward curves | Done | `03-dpo-reward-curves.png`; interpreted in `REFLECTION.md` section 3 |
| NB4 side-by-side eval | Done | `04-side-by-side-table.png`, `05-judge-output.png` |
| NB5 GGUF smoke | Done | `06-gguf-smoke.png` |
| NB6 benchmark JSON/chart | Chart done; JSON evidence in notebook | `07-benchmark-comparison.png`, notebook output |
| Reflection 7 sections | Done | `submission/REFLECTION.md` |
| HF Hub push bonus | Done | https://huggingface.co/StevenMup/lab22-dpo-vn |

## Final LMS Submission

Submit the **public GitHub repo URL** to the VinUni LMS Day 22 submission box. No PR is required. Keep the repo public until grades are released.
