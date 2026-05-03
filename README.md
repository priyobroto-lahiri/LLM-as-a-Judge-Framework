# LLM-as-a-Judge Framework

An advanced evaluation framework that utilizes "frontier" models (GPT-4o/Claude 3.5 Sonnet) to grade the performance of smaller, specialized, or open-source LLMs using custom rubrics and persona-based testing.

## 🎯 The Problem
Standard metrics (BLEU, ROUGE) are great for word overlap but fail to capture "nuance," "helpfulness," or "logical reasoning." Human evaluation is too slow and expensive to scale. This project implements the **LLM-as-a-Judge** pattern to provide human-level evaluation at API speeds and costs.

## 🛠️ The Approach
This framework moves beyond simple scoring to deep behavioral analysis:

1.  **G-Eval (Generative Evaluation):** Using Chain-of-Thought (CoT) reasoning to force the judge to "think" and justify its score before awarding it.
2.  **Persona-Based Evaluation:** Implementing 3 distinct judge personas (e.g., Strict Technical Architect, End-User, Business Executive) to surface how different stakeholders might perceive the same answer.
3.  **Bias Detection:** Quantifying and mitigating **Position Bias** (preferring the first answer) and **Verbosity Bias** (preferring longer answers).

## 📊 Reliability Metrics (Preview)
| Evaluator Persona | Agreement with Human (%) | Avg Score (Model A) | Avg Score (Model B) |
| :--- | :--- | :--- | :--- |
| **Strict Architect** | TBD | TBD | TBD |
| **Business User** | TBD | TBD | TBD |
| **System Reliability** | TBD | TBD | TBD |

## 🚀 Tech Stack
- **Judges:** GPT-4o-mini, Llama 3 70B (Groq)
- **Frameworks:** DeepEval, Prometheus (LLM Judge)
- **Analysis:** Cohen's Kappa for Inter-Rater Reliability
- **Logic:** Python, Pydantic (Structured Outputs)
