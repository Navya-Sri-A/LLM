# PSU Qwen Simple Starter

Only one shared model: Qwen2.5-0.5B-Instruct. The notebook finds three matching policy snippets using TF-IDF, asks Qwen a question, and scores the answer against the 24 public development labels. This is intentionally a naive baseline; it may predict YES for everything.

Kaggle:
1. Import `PSU_Qwen_Simple_Starter_Kaggle.ipynb` as a notebook.
2. Under Add Input, attach the `PSU_Qwen_Simple_Starter_Data.zip` dataset. Kaggle often extracts ZIPs automatically. The loader handles either layout.
3. Enable Internet if Qwen needs downloading. GPU is optional.
4. Run cells top-to-bottom. Start with `N_QUESTIONS=3`, then set it to `24`.
5. The notebook saves `PSU_Qwen_Starter_Results.csv` to `/kaggle/working`.

Included data:
- `PSU_Policy_Excerpts_v1.csv`: 23 frozen, sourced, curated paraphrases of eight public PSU policy webpages.
- `PSU_Policy_Source_Manifest.csv`: origin URLs and retrieval date.
- `PSU_24_Questions_v1.csv`: 24 development questions.
- `PSU_24_Dev_Labels_v1.csv`: development labels; 8 YES, 8 NO, 8 INSUFFICIENT_INFO.

No hidden-test questions or labels. No instructor-only notes or oracle evidence.

The generated answers are for classroom experimentation and should not be used for academic advising.
