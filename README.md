<img src="https://capsule-render.vercel.app/api?type=waving&color=0:667eea,100:764ba2&height=200&section=header&text=Julian%20Kerignard&fontSize=48&fontColor=ffffff&fontAlignY=38&desc=AI%20%2F%20ML%20Engineer%20%C2%B7%20I%20train%20language%20models%20from%20scratch&descAlignY=58&descSize=16&animation=fadeIn" width="100%" alt="Julian Kerignard" />

<div align="center">

<a href="https://huggingface.co/JulianKrgd">
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3200&pause=800&color=764BA2&center=true&vCenter=true&width=620&lines=Training+the+Julian+family+of+LLMs;JAX+%2F+Flax+on+TPU%2C+from+scratch;Raw+Wikipedia+dumps+%E2%86%92+instruct+models;Bilingual+EN+%2F+FR+language+models" alt="What I do" />
</a>

<br />

[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-JulianKrgd-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/JulianKrgd)
[![Website](https://img.shields.io/badge/Website-juliankerignard.fr-667eea?style=for-the-badge&logo=firefoxbrowser&logoColor=white)](https://juliankerignard.fr)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Julian%20Kerignard-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/julian-kerignard-b9ab6a2bb)

</div>

---

## About

I build **language models end to end** — from raw text to instruction-tuned chat.
My main line of work is the **Julian** family: bilingual (EN / FR) LLMs trained
**from scratch in JAX / Flax on TPU**, on a Wikipedia corpus I prepare and publish myself.

```
data (Wikipedia EN/FR dumps)  →  clean / tokenize (SentencePiece)  →
pretrain (JAX · Flax · Optax · FSDP on TPU)  →  SFT / instruct (ChatML)  →  ship on the Hub
```

## The Julian language models

| Model | Params | Training | Type |
|-------|:------:|----------|------|
| [**Julian-600M-40B**](https://huggingface.co/JulianKrgd/Julian-600M-40B) | 600M | 40B tokens, LLaMA-style, JAX/TPU | Base |
| [**julian-600m-40b-instruct**](https://huggingface.co/JulianKrgd/julian-600m-40b-instruct-sft100k) | 600M | SFT 30k / 100k · ChatML | Instruct |
| [julian-600m-10b](https://huggingface.co/JulianKrgd/julian-600m-10b) | 600M | 10B tokens, earlier run | Base |
| [JULIAN-100M](https://huggingface.co/JulianKrgd/JULIAN-100M) / [Instruct](https://huggingface.co/JulianKrgd/JULIAN-100M-Instruct) | 100M | first generation, GPT-style | Base + Instruct |

Plus a write-up of the whole thing: [**julian-600m-paper**](https://huggingface.co/JulianKrgd/julian-600m-paper).

## Datasets I built & published

- [wikipedia-en-julian](https://huggingface.co/datasets/JulianKrgd/wikipedia-en-julian) &nbsp;·&nbsp; [wikipedia-fr-julian](https://huggingface.co/datasets/JulianKrgd/wikipedia-fr-julian) — the bilingual pretraining corpus

## Training stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JAX](https://img.shields.io/badge/JAX-4B0082?style=flat-square&logoColor=white)
![Flax](https://img.shields.io/badge/Flax-6E44FF?style=flat-square&logoColor=white)
![Optax](https://img.shields.io/badge/Optax-8A2BE2?style=flat-square&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Safetensors](https://img.shields.io/badge/Safetensors-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Google Cloud TPU](https://img.shields.io/badge/TPU-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![SentencePiece](https://img.shields.io/badge/SentencePiece-333333?style=flat-square)

## Beyond LLMs

- [**oneiro**](https://github.com/JulianKerignard/oneiro) — a mini-DreamerV3 world model (15M params, JAX/Flax), model-based RL on Crafter
- **Model Context Protocol servers** — [Blender](https://github.com/JulianKerignard/Blender_MCP) · [Unity](https://github.com/JulianKerignard/MCP-Unity) · [Obsidian](https://github.com/JulianKerignard/MCP-obsidian) · [Trello](https://github.com/JulianKerignard/Trello_MCP) · [webcheck](https://github.com/JulianKerignard/mcp-webcheck)
- [ClawdEngine_Rust](https://github.com/JulianKerignard/ClawdEngine_Rust) — a 3D engine in Rust &nbsp;·&nbsp; [StatsMonitor_MacOS](https://github.com/JulianKerignard/StatsMonitor_MacOS) — Swift

<br />

<div align="center">

[![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=JulianKerignard&layout=compact&hide_border=true&card_width=440&theme=react&bg_color=0d1117&title_color=764ba2&text_color=c9d1d9)](https://github.com/JulianKerignard)

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:764ba2,100:667eea&height=120&section=footer" width="100%" alt="" />
