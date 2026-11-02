# 🚀 YZM5109 Assignment I - Prompting Techniques on Qwen2.5-7B With Alpaca Dataset

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)
![Kaggle](https://img.shields.io/badge/Kaggle-035a7d?style=for-the-badge&logo=kaggle&logoColor=white)

**Student:** Beyda Bucak  
**Course:** YZM5109 - Large Language Models  

## 📁 Files Included in This Submission

| File | Description |
|------|-------------|
| 📄 `report.pdf` | The final 2-page assignment report in IEEE format. |
| 📝 `AI_Usage_Log.pdf` | A log detailing the use of AI tools during the assignment process. |
| 📓 `llmresearch1.ipynb` | The main Kaggle Notebook containing the implementation, configurations, and prompt templates. |
| 📊 `b1_predictions.csv` | Generated outputs and references for **Zero-shot** prompting. |
| 📊 `b2_predictions.csv` | Generated outputs and references for **Chain-of-Thought** prompting. |
| 📊 `b3_predictions.csv` | Generated outputs and references for **Persona** prompting. |
| 🖼️ `ss-bleu.png` | Screenshot of the BLEU metric calculations. |
| 🖼️ `ss-rougeAndBertscore.png` | Screenshot of the ROUGE and BERTScore metric calculations. |

## ⚙️ Configuration & Prompts
All prompt structures (e.g., `alpaca_prompt`, Chain-of-Thought additions, Persona roles) and model generation configurations (e.g., `max_new_tokens=256`, `seed=42`) are embedded directly within the `llmresearch1.ipynb` file. No separate configuration files are required to run the experiments.

## 🚀 How to Run

1. The code was developed and tested on **Kaggle Notebooks** using dual **T4 GPUs (T4 x2)**.
2. Upload `llmresearch1.ipynb` to Kaggle (or Google Colab with GPU enabled). Don't forget to turn **ON** the internet from the Session Options menu on Kaggle Notebook.
3. Run the first cell to install all required dependencies: `pip install unsloth torchao transformers trl evaluate rouge_score bert_score`
4. Run the notebook sequentially. It will automatically:
   - Download the `unsloth/Qwen2.5-7B` model.
   - Load 200 samples from the `yahma/alpaca-cleaned` dataset (seed=42).
   - Execute the B1, B2, and B3 evaluation conditions and compute the metrics.
