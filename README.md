<img src="https://capsule-render.vercel.app/api?type=waving&color=0:667eea,100:764ba2&height=200&section=header&text=Julian%20Kerignard&fontSize=48&fontColor=ffffff&fontAlignY=38&desc=AI%20%2F%20ML%20Engineer%20%C2%B7%20language%20models%20%26%20world%20models%20from%20scratch&descAlignY=58&descSize=16&animation=fadeIn" width="100%" alt="Julian Kerignard" />

<div align="center">

<a href="https://huggingface.co/JulianKrgd">
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3200&pause=800&color=764BA2&center=true&vCenter=true&width=640&lines=Training+LLMs+and+world+models+from+scratch;JAX+%2F+Flax+on+TPU+and+GPU;Julian+%E2%80%94+bilingual+EN+%2F+FR+language+models;oneiro+%E2%80%94+an+agent+that+learns+in+its+dreams" alt="What I do" />
</a>

<br />

[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-JulianKrgd-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)](https://huggingface.co/JulianKrgd)
[![Website](https://img.shields.io/badge/Website-juliankerignard.fr-667eea?style=for-the-badge&logo=firefoxbrowser&logoColor=white)](https://juliankerignard.fr)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Julian%20Kerignard-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/julian-kerignard-b9ab6a2bb)

</div>

---

## About

I train neural networks **from scratch**, mostly in **JAX / Flax**. Two lines of work:

- **Language models** — the *Julian* family: bilingual (EN / FR) LLMs, from raw data to instruction-tuned chat, on TPU.
- **World models** — *oneiro*: a from-scratch DreamerV3 agent that learns its entire policy inside the imagined rollouts of its own world model.

## World model — oneiro

<div align="center">
<img src="https://raw.githubusercontent.com/JulianKerignard/oneiro/main/videos/oneiro_demo_opt.gif" width="480" alt="oneiro agent playing Crafter" />
<br />
<sub>oneiro (~64k env steps) unlocking achievements in Crafter — learned entirely from imagination rollouts</sub>
</div>

A from-scratch reimplementation of [**DreamerV3**](https://arxiv.org/abs/2301.04104) (Hafner et al., 2023) in **JAX / Flax NNX**, trained on the [Crafter](https://github.com/danijar/crafter) benchmark (sparse rewards, 64×64 pixels, 22 hierarchical achievements).

- **15.26M parameters** — DreamerV3-S class
- **Rainbow-level in 64k env steps**: 4.0 achievements/episode, vs Rainbow's 4.3 at **1M** steps — a ~16× sample-efficiency gap
- RSSM + imagination-based actor-critic, GPU-resident replay buffer, `lax.scan` everywhere
- **18+ documented training runs** with full debugging journals and a hypothesis registry — the real value of the repo

→ [**JulianKerignard/oneiro**](https://github.com/JulianKerignard/oneiro)

## Language models — the Julian family

```
Wikipedia EN/FR dumps  →  clean / tokenize (SentencePiece)  →
pretrain (JAX · Flax · Optax · FSDP on TPU)  →  SFT / instruct (ChatML)  →  ship on the Hub
```

| Model | Params | Training | Type |
|-------|:------:|----------|------|
| [**Julian-600M-40B**](https://huggingface.co/JulianKrgd/Julian-600M-40B) | 600M | 40B tokens, LLaMA-style, JAX/TPU | Base |
| [**julian-600m-40b-instruct**](https://huggingface.co/JulianKrgd/julian-600m-40b-instruct-sft100k) | 600M | SFT 30k / 100k · ChatML | Instruct |
| [julian-600m-10b](https://huggingface.co/JulianKrgd/julian-600m-10b) | 600M | 10B tokens, earlier run | Base |
| [JULIAN-100M](https://huggingface.co/JulianKrgd/JULIAN-100M) / [Instruct](https://huggingface.co/JulianKrgd/JULIAN-100M-Instruct) | 100M | first generation, GPT-style | Base + Instruct |

Plus a write-up of the whole thing: [**julian-600m-paper**](https://huggingface.co/JulianKrgd/julian-600m-paper).

**Datasets I built & published:** [wikipedia-en-julian](https://huggingface.co/datasets/JulianKrgd/wikipedia-en-julian) &nbsp;·&nbsp; [wikipedia-fr-julian](https://huggingface.co/datasets/JulianKrgd/wikipedia-fr-julian) — the bilingual pretraining corpus.

## Training stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JAX](https://img.shields.io/badge/JAX-4B0082?style=flat-square&logoColor=white)
![Flax](https://img.shields.io/badge/Flax%20NNX-6E44FF?style=flat-square&logoColor=white)
![Optax](https://img.shields.io/badge/Optax-8A2BE2?style=flat-square&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Transformers](https://img.shields.io/badge/Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Safetensors](https://img.shields.io/badge/Safetensors-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Google Cloud TPU](https://img.shields.io/badge/TPU-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![SentencePiece](https://img.shields.io/badge/SentencePiece-333333?style=flat-square)

## Tooling & systems

- **Model Context Protocol servers** — [Blender](https://github.com/JulianKerignard/Blender_MCP) · [Unity](https://github.com/JulianKerignard/MCP-Unity) · [Obsidian](https://github.com/JulianKerignard/MCP-obsidian) · [Trello](https://github.com/JulianKerignard/Trello_MCP) · [webcheck](https://github.com/JulianKerignard/mcp-webcheck)
- [ClawdEngine_Rust](https://github.com/JulianKerignard/ClawdEngine_Rust) — a 3D engine in Rust &nbsp;·&nbsp; [StatsMonitor_MacOS](https://github.com/JulianKerignard/StatsMonitor_MacOS) — Swift

<br />

<div align="center">

[![Top languages](https://github-readme-stats.vercel.app/api/top-langs/?username=JulianKerignard&layout=compact&hide_border=true&card_width=440&theme=react&bg_color=0d1117&title_color=764ba2&text_color=c9d1d9)](https://github.com/JulianKerignard)

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:764ba2,100:667eea&height=120&section=footer" width="100%" alt="" />
