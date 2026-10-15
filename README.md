# ClaimCheck

On-premises small language model (SLM) project that cross-checks a patient's health insurance claim form against the hospital's discharge summary. A fine-tuned Qwen2.5-3B model extracts 9 fields with exact quotes from both documents, Python rules compare exact values, the model only judges whether differently-worded descriptions mean the same thing, and a human reviewer makes the final decision. Every decision is recorded in a hash-chained audit log.

A project by Shazia Mahek · Veltris × Woxsen University

## Contents

- `claimcheck_pipeline_fixed.ipynb` — the fixed end-to-end pipeline (extraction, quote checker, comparison, chat, audit log)
- `claimcheck_streamlit_colab.ipynb` — Streamlit app + Colab/Cloudflare tunnel notebook to run the demo
- `claimcheck-qwen2.5-3b-lora-adapter.zip` — the trained QLoRA adapter (Qwen2.5-3B-Instruct, rank 8, alpha 16)
- `ClaimCheck_demo_documents/` — sample claim forms and discharge summaries (clean + scanned) for 3 demo cases
- `ClaimCheck_Documentation.pdf` — full project documentation
