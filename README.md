# MINTQA: A Multi-Hop Question Answering Benchmark for Evaluating LLMs on New and Long-tail Knowledge

<div align="left">
   <p>
   <a href='https://aclanthology.org/2026.acl-long.18/'><img src='https://img.shields.io/badge/ACL-2026-red'></a>
   <a href='https://aclanthology.org/2026.acl-long.18.pdf'><img src='https://img.shields.io/badge/Paper-PDF-blue'></a>
   <a href='https://www.arxiv.org/abs/2412.17032'><img src='https://img.shields.io/badge/arXiv-2412.17032-b31b1b'></a>
   <a href='https://huggingface.co/datasets/probejie/MINTQA'><img src='https://img.shields.io/badge/%F0%9F%A4%97%20Dataset-MINTQA-yellow'></a>
  </p>
</div>

## 📢 News

- **Jul 2026**: MINTQA has been accepted to **ACL 2026 (Main Conference, Long Paper)**! 🎉 [[Paper]](https://aclanthology.org/2026.acl-long.18/)
- The dataset is now available on 🤗 Hugging Face: [probejie/MINTQA](https://huggingface.co/datasets/probejie/MINTQA)

## Dataset

> We are currently organizing the entire project code and will be releasing it soon.

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

If you find MINTQA useful, please cite our ACL 2026 paper:

```bibtex
@inproceedings{he-etal-2026-mintqa,
    title = "{MINTQA}: A Multi-Hop Question Answering Benchmark for Evaluating {LLM}s on New and Long-tail Knowledge",
    author = "He, Jie  and
      Hu, Nan  and
      Long, Wanqiu  and
      Chen, Jiaoyan  and
      Pan, Jeff Z.",
    editor = "Liakata, Maria  and
      Moreira, Viviane P.  and
      Zhang, Jiajun  and
      Jurgens, David",
    booktitle = "Proceedings of the 64th Annual Meeting of the {A}ssociation for {C}omputational {L}inguistics (Volume 1: Long Papers)",
    month = jul,
    year = "2026",
    address = "San Diego, California, United States",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2026.acl-long.18/",
    doi = "10.18653/v1/2026.acl-long.18",
    pages = "445--479"
}
```
