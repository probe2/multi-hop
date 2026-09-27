# MINTQA: A Multi-Hop Question Answering Benchmark for Evaluating LLMs on New and Tail Knowledge

<div align="left">
   <p>
   <a href='https://www.arxiv.org/abs/2412.17032'><img src='https://img.shields.io/badge/arXiv-2412.17032-b31b1b'></a>
  </p>
</div>

## We are currently organizing the entire project code and will be releasing it soon.

We release the annotated MINTQA dataset, divided into two subsets: **MINTQA-POP** (17,887 questions, popular vs. unpopular knowledge) and **MINTQA-TI** (10,479 questions, new vs. old knowledge).

### 🤗 Load from Hugging Face

The dataset is available on Hugging Face: [probejie/MINTQA](https://huggingface.co/datasets/probejie/MINTQA)

```python
from datasets import load_dataset

pop = load_dataset("probejie/MINTQA", "pop", split="test")  # MINTQA-POP
ti  = load_dataset("probejie/MINTQA", "ti",  split="test")  # MINTQA-TI
```

Each example contains `question`, `answer`, `type` (per-hop knowledge label), `num_hops`, `subquestion`, `subanswer`, `triple` (Wikidata reasoning chain) and `facts`.

The raw JSONL files are also in this repo: `MINTQA-POP.json` and `MINTQA-TI.json` (one JSON object per line).

The **MINTQA Knowledge Graph** (a subset of Wikidata) is available on Hugging Face:

🔗 [Check the MINTQA KG here](https://huggingface.co/Sp1der/MintQA-KG/tree/main)

## Citation

```bibtex
@article{he2024mintqa,
  title   = {MINTQA: A Multi-Hop Question Answering Benchmark for Evaluating LLMs on New and Tail Knowledge},
  author  = {He, Jie and Hu, Nan and Long, Wanqiu and Chen, Jiaoyan and Pan, Jeff Z.},
  journal = {arXiv preprint arXiv:2412.17032},
  year    = {2024}
}
```
