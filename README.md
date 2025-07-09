# Lost in Pronunciation: PCR-ToxiCN

## 📍 Overview

**Phonetic Cloaking Replacement (PCR)** leverages homophonic or near-homophonic variants to bypass Chinese content moderation, presenting unique challenges for safe deployment of LLMs in moderation tasks.

This project proposes a **four-way taxonomy (Hanzi, Alphabet, Numerical, Mixed)** for Chinese PCR and introduces **PCR-ToxiCN**, the first real-world dataset containing naturally occurring, phonetically cloaked offensive language collected from RedNote (Xiaohongshu). Benchmarking leading LLMs on PCR-ToxiCN reveals significant weaknesses under realistic attacks and demonstrates that a lightweight **Pinyin-based prompting strategy** can effectively recover lost accuracy.

- 📊 **Dataset on Hugging Face:** [PCR-ToxiCN](https://huggingface.co/datasets/UTSNLPGroup/PCR-ToixCN)
- 💻 **Code on GitHub:** [HTG13503/PCR-ToxiCN](https://github.com/HTG13503/PCR-ToixCN)

---

## 🚀 Features

✅ Four-way surface-form taxonomy of PCR (HR/AR/NR/MR)  
✅ 500 real user comments (250 offensive, 250 non-offensive)  
✅ Benchmark SOTA LLMs (4o, Qwen2.5, LLaMA3.3, o3-mini, QWQ) under realistic PCR attacks  
✅ Comparative analysis of standard prompting, Chain-of-Thought (CoT), and Pinyin-based prompting  

---

## 📊 Dataset Statistics

| Class       | Offensive | Non-Offensive | Total |
|-------------|-----------|---------------|-------|
| Hanzi (HR)  | 169       | 183           | 352   |
| Alphabet (AR)| 50       | 37            | 87    |
| Numerical (NR)| 13      | 19            | 32    |
| Mixed (MR)  | 18        | 11            | 29    |
| **Total**   | 250       | 250           | 500   |

Data were manually collected and annotated by native speakers with Fleiss' kappa = 81.5% for label consistency.

---

## 🛠️ Getting Started

### Clone the Repository

```bash
git clone https://github.com/HTG13503/PCR-ToxiCN.git
cd PCR-ToxiCN
```
---

## 📈 Key Results
![5981752043387_ pic](https://github.com/user-attachments/assets/166dad4f-afa1-433e-92ee-91bd97d4ea8c)

![5971752043355_ pic](https://github.com/user-attachments/assets/e5dc22df-3294-4f66-9bd3-5269b36df7ac)

**Findings:**
- COT prompting does not improve detection under realistic PCR attacks.
- Pinyin-based Prompting effectively restores detection accuracy, approaching performance of reasoning-capable models.
---

## 👥 Contributors

Haotan Guo, Jianfei He, Jiayuan Ma, Hongbin Na, Zimu Wang, Haiyang Zhang, Qi Chen, Wei Wang, Zijing Shi, Tao Shen, Ling Chen

---

## 📄 Citation

---

## ✉️ Contact

For questions, collaborations, or dataset access:
- Haotan Guo (The University of Sydney) [hguo0293@uni.sydney.edu.au]
