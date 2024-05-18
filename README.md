# Multilingual Pre-trained Models Tutorial
<img src='C:\Users\huang\AppData\Roaming\Typora\typora-user-images\image-20240516202515585.png' height='400' style="float:left">

Considering the rapid growth of the research of multilingual NLP, we have established this repository to gather relevant literature in this specific multilingual domain.  *(As a contribution of the survey paper "[A Survey on Large Language Models with Multilingualism: Recent Advances and New Frontiers]()")*

This is also a tutorial of multilingual pre-trained models maintained by the Beijing Jiaotong University (BJTU) NLP Group (Continual Updated).

The past five years have witnessed the rapid development of multilingual pre-trained models, especially for data-driven large language models (LLMs). Due to the dominance of multilingual NLP at the present time, priority is given to collecting important, up-to-date multilingual pre-trained models papers and their performance. As one of the contributions of the survey, we continuously update and expand the content according to the chapters in the survey. Our list is still incomplete and the categorization might be inappropriate. We will keep adding papers and improving the list. [Any suggestions are welcome!](#cus)

## LLMs with Multilingualism
We only present an overview of **representative** LLMs (most of trainable parameters greater than ***7B***) that have certain multilingual capabilities, including their release time and details. The latest models that achieve good performance on the leaderboard will be updated in a timely manner, or contact us for updates and promotion.

### General Multilingual Leaderboard

We investigate the LLMs with multilingualism in our reconstructed benchmarks. *(If there are many versions of a model, we only choose the version that perform the best.)*

In this leaderboard we use a unified *prompt* for each task to explore the multilingual capabilities of the model. The potential enhancement capabilities of the model are explored in the next chapter "**[Multilingual Inference Strategies](#mis)**".

> 🎈 A suite for calling LLMs is coming soon! The benchmark is under built.

### Open-Source Models

> All models are available on the Internet. The link of paper or Github is given.

- LLaMA, Meta AI
  - LLaMA-1, [LLaMA: Open and Efficient Foundation Language Models](https://arxiv.org/abs/2302.13971), 2023.02.27
  - LLaMA-2, [Llama 2: Open Foundation and Fine-Tuned Chat Models](https://arxiv.org/abs/2307.09288), 2023.07.18
  - LLaMA-3, [Meta Llama 3](https://github.com/meta-llama/llama3/tree/main), 2023.04.18
- GLM, ZHIPU, [ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B), 2023.05.13, The other versions are released at their Github as well.
- Baichuan, Baichuan AI
  - Baichuan-1, [Technical Report](https://huggingface.co/baichuan-inc/Baichuan-7B), 2023.06.15
  - Baichuan-2, [Baichuan 2: Open Large-scale Language Models](https://arxiv.org/abs/2309.10305), 2023.09.06
  - Baichuan-3, [Chat Platform](https://www.baichuan-ai.com/home), 2024.01.29
- Qwen, Alibaba, [Qwen Technical Report](https://arxiv.org/abs/2309.16609)
  - Qwen, [Technical Report](https://github.com/QwenLM/Qwen/blob/main/README.md), 2023.08.03
  - Qwen-1.5, [Technical Report](https://github.com/QwenLM/Qwen1.5?tab=readme-ov-file), 2024.02.05
- Phi, Microsoft
  - Phi-1, [Textbooks Are All You Need](https://arxiv.org/abs/2306.11644), 2023.06.20
  - Phi-1.5, [Textbooks Are All You Need II: phi-1.5 technical report](https://www.microsoft.com/en-us/research/publication/textbooks-are-all-you-need-ii-phi-1-5-technical-report/), 2023.09.11
  - Phi-2, [Phi-2: The surprising power of small language models](https://www.microsoft.com/en-us/research/blog/phi-2-the-surprising-power-of-small-language-models/), 2023.12.12
  - Phi-3, [Phi-3 Technical Report: A Highly Capable Language Model Locally on Your Phone](https://export.arxiv.org/abs/2404.14219), 2024.04.23
- Mistral, [Mistral 7B](https://arxiv.org/abs/2310.06825)
  - Mistral 7B, 2023.10.10
  - Mixtral 8x7B, 2023.12.11
  - Mixtral 8x22B, 2024.04.17
- OpenChat, Tsinghua University, [OpenChat: Advancing Open-source Language Models with Mixed-Quality Data](https://arxiv.org/abs/2309.11235), 2023.09.20
- Deepseek, DeepSeek AI, [DeepSeek LLM Scaling Open-Source Language Models with Longtermism](https://arxiv.org/abs/2401.02954), 2024.01.05
- InternLM, Shanghai AI Laboratory
  - InternLM, [Repo](https://huggingface.co/internlm/internlm-7b), 2023.09.20
  - InternLM2, [InternLM2 Technical Report](https://arxiv.org/abs/2403.17297), 2024.03.26
- BLOOM, Big Science, [BLOOM: A 176B-Parameter Open-Access Multilingual Language Model](https://arxiv.org/abs/2211.05100), 2022.11.09
  - BLOOMZ-7b1, Hugging Face, [Crosslingual Generalization through Multitask Finetuning](https://arxiv.org/abs/2211.01786), 2023.05.29
- Bayling, Institute of Computing Technology, Chinese Academy of Sciences (ICT/CAS), [BayLing: Bridging Cross-lingual Alignment and Instruction Following through Interactive Translation for Large Language Models](https://arxiv.org/abs/2306.10968), 2023.06.19

### Closed-Source Systems

We only investigate a few representative closed-source LLMs because most of these commercial systems are expensive to invoke. We hope to get sponsors or voluntary enterprise responses to compare closed-source systems, otherwise our goal is to discuss the future potential of LLMs within the open-source community.

- GPT, [OpenAI](https://openai.com/)
  - ChatGPT (GPT-3.5-turbo)
  - GPT-4, [GPT-4 Technical Report](https://arxiv.org/abs/2303.08774), 2023.05.15
- PaLM, Google
  - [PaLM-2](https://ai.google/discover/palm2/)
- Claude, [Anthropic](https://claude.ai/)
- Gemini, DeepMind, [Chat with Gemini](https://gemini.google.com/?hl=zh)
<span id="mis"></span>
## Multilingual Inference Strategies
We investigate several inference strategies for LLMs to explore the potential enhancement capabilities with multilingualism in the related benchmarks. *(The multilingual inference strategies are to act on prompt with external knowledge, and LLMs are frozen.)*

### Reasoning Leaderboard

| Model               | Method       | MGSM | XCOPA | XNLI | PAWS-X | MKQA | Avg  |
| ------------------- | ------------ | ---- | ----- | ---- | ------ | ---- | ---- |
| GPT-3.5             | Basic        | 34.4 | 72.3  | 52.2 | 49.7   | 35.4 | 48.8 |
|                     | En-Basic     | 41.1 | 76.1  | 63.0 | 62.0   | 36.5 | 55.7 |
|                     | CoT          | 49.9 | 72.4  | 50.6 | 50.3   | 35.4 | 51.7 |
|                     | En-CoT       | 61.1 | 78.6  | 56.4 | 61.6   | 42.9 | 60.1 |
|                     | XLT          | 62.3 | 79.3  | 59.2 | 59.4   | 37.6 | 59.6 |
|                     | Trans-Google | 73.9 | 84.5  | 60.5 | 67.2   | 43.8 | 66.0 |
|                     | Trans-NLLB   | 61.0 | 79.7  | 59.2 | 67.5   | 37.2 | 60.9 |
| BLOOMZ-7b1          | Basic        | 1.3  | 21.4  | 8.3  | -      | 7.8  | 9.7  |
|                     | En-Basic     | 2.0  | 56.5  | 43.9 | -      | 10.6 | 28.3 |
|                     | CoT          | 1.2  | 20.9  | 8.2  | -      | 6.5  | 9.2  |
|                     | En-CoT       | 1.7  | 53.9  | 35.9 | -      | 9.3  | 25.2 |
|                     | XLT          | 1.7  | 50.5  | 35.4 | -      | 8.0  | 23.9 |
|                     | Trans-Google | 2.7  | 63.7  | 44.3 | -      | 17.2 | 32.0 |
|                     | Trans-NLLB   | 2.4  | 61.8  | 43.8 | -      | 14.7 | 30.7 |
| Mistral-7B-Instruct | Basic        | 11.2 | 54.2  | 42.8 | 44.6   | 7.8  | 32.1 |
|                     | En-Basic     | 23.8 | 34.9  | 50.2 | 46.9   | 7.0  | 32.6 |
|                     | CoT          | 17.0 | 53.8  | 43.4 | 44.3   | 7.8  | 33.3 |
|                     | En-CoT       | 27.6 | 40.8  | 50.0 | 46.6   | 11.5 | 35.3 |
|                     | XLT          | 31.8 | 61.5  | 46.0 | 47.8   | 9.6  | 39.3 |
|                     | Trans-Google | 41.3 | 59.2  | 55.0 | 51.5   | 17.0 | 44.8 |
|                     | Trans-NLLB   | 31.7 | 54.4  | 53.0 | 52.4   | 15.5 | 41.4 |
| Llama-2-7B-Chat     | Basic        | 8.4  | 46.5  | 34.6 | 48.1   | 14.4 | 30.4 |
|                     | En-Basic     | 9.3  | 49.7  | 39.0 | 48.8   | 16.1 | 32.6 |
|                     | CoT          | 10.9 | 46.3  | 35.6 | 48.3   | 13.3 | 30.9 |
|                     | En-CoT       | 13.6 | 54.9  | 41.0 | 48.7   | 13.8 | 34.4 |
|                     | XLT          | 10.4 | 50.8  | 44.8 | 44.5   | 14.6 | 33.0 |
|                     | Trans-Google | 28.6 | 67.7  | 45.5 | 57.5   | 19.8 | 43.8 |
|                     | Trans-NLLB   | 24.8 | 64.6  | 44.1 | 56.2   | 17.4 | 41.4 |
| Llama-2-13B-Chat    | Basic        | 15.6 | 50.1  | 36.4 | 54.0   | 18.3 | 34.9 |
|                     | En-Basic     | 19.0 | 54.3  | 43.4 | 59.1   | 20.2 | 39.2 |
|                     | CoT          | 18.1 | 50.9  | 35.7 | 54.8   | 15.7 | 35.0 |
|                     | En-CoT       | 19.9 | 54.5  | 43.7 | 57.6   | 19.8 | 39.1 |
|                     | XLT          | 22.3 | 56.0  | 51.4 | 55.7   | 19.0 | 40.9 |
|                     | Trans-Google | 39.1 | 71.9  | 46.1 | 58.4   | 33.8 | 49.9 |
|                     | Trans-NLLB   | 31.8 | 68.2  | 45.4 | 57.8   | 28.4 | 46.3 |
| Llama-2-70B-Chat    | Basic        | 23.6 | 51.5  | 39.0 | 52.8   | 24.8 | 38.3 |
|                     | En-Basic     | 28.6 | 55.3  | 46.5 | 60.4   | 24.7 | 43.1 |
|                     | CoT          | 23.5 | 50.5  | 37.9 | 54.9   | 21.9 | 37.7 |
|                     | En-CoT       | 30.2 | 61.2  | 45.9 | 64.9   | 31.1 | 46.7 |
|                     | XLT          | 32.8 | 58.7  | 52.2 | 55.7   | 26.6 | 45.2 |
|                     | Trans-Google | 53.3 | 80.9  | 54.0 | 68.5   | 39.7 | 59.3 |
|                     | Trans-NLLB   | 43.8 | 77.1  | 52.2 | 69.2   | 19.4 | 52.3 |

*Note: This leaderboard is followed by [Liu et al.](https://arxiv.org/abs/2403.10258), we will update it in the next version when the evaluation suite for calling LLMs is built.

### Baseline Details

```
[Question]: "制作一件袍子需要2匹蓝色纤维布料和这个数量一半的白色纤维布料。它一共需要用掉多少匹布料"
Basic: [Query]=[Question]+[Prompt: 您的最终答案的格式应为："答案: <阿拉伯数字>".]
En-Basic: [Query]=[Question]+[Prompt -> English Prompt: You should format your final answer as "Answer: <Arabic numeral>".]
CoT: [Query]=[Question]+[Prompt -> CoT: 让我们一步步思考。您的最终答案的格式应为："答案: <阿拉伯数字>".]
En-CoT: [Query]=[Question]+[Prompt -> English CoT: Let’s think step by step in English. You should format your final answer as "Answer: <Arabic numeral>".]
XLT: [Query]=[Prefix: I want you to act as an arithmetic reasoning expert for Chinese.Request: ]+[Question]+[Complex Prompt: You should retell the request in English. You should do step-by-step answer to obtain a number answer. You should step-by-step answer the request. You should tell me the answer in this format "Answer:".]
Trans-X: [Query]=[Question -> English Question by X]+[Prompt -> English CoT: Let’s think step by step in English. You should format your final answer as "Answer: <Arabic numeral>".]
```

### Reading List

We provide a [reading list](https://github.com/kaiyuhwang/MLLM-Survey/blob/main/readinglist/inference.md) (Continual Updated) for this chapter corresponding to the section 4 in the survey.

##  Security


### Jailbreaking Leaderboard

This leaderboard is built by the EasyJailbreak framework on the AdvBench.

| Method        | GPT-3.5 | GPT-4 | Llama-2-7B-Chat | Llama-2-13B-Chat | Vicuna-7B-v1.5 | Vicuna-13B-v1.5 | ChatGLM | Qwen-7B-Chat | InterLM-7B | Mistral-7B |
| ------------- | ------- | ----- | --------------- | ---------------- | -------------- | --------------- | ------- | ------------ | ---------- | ---------- |
| GCG           |         |       |                 |                  |                |                 |         |              |            |            |
| JailBroken    |         |       |                 |                  |                |                 |         |              |            |            |
| GPTFUZZER     |         |       |                 |                  |                |                 |         |              |            |            |
| AutoDAN       |         |       |                 |                  |                |                 |         |              |            |            |
| DeepInception |         |       |                 |                  |                |                 |         |              |            |            |
| ICA           |         |       |                 |                  |                |                 |         |              |            |            |
| PAIR          |         |       |                 |                  |                |                 |         |              |            |            |
| ReNeLLM       |         |       |                 |                  |                |                 |         |              |            |            |
| Multilingual  |         |       |                 |                  |                |                 |         |              |            |            |
| Cipher        |         |       |                 |                  |                |                 |         |              |            |            |
| CodeChameleon |         |       |                 |                  |                |                 |         |              |            |            |

### Reading List

We provide a [reading list](https://github.com/kaiyuhwang/MLLM-Survey/blob/main/readinglist/security.md) of jailbreaking and defense methods (Continual Updated) for this chapter corresponding to the section 5 in the survey.

## Multidomain

### Legal

> 🎈 The leaderboard of legal benchmark is under built.

### Medical

> 🎈 The leaderboard of medical benchmark is under built.

### Finance

> Coming soon! This domain is under updated.

## Data Resource & Evaluation
The data resource and popular benchmarks are listed in the [reading list](https://github.com/kaiyuhwang/MLLM-Survey/blob/main/readinglist/data.md) in details.
<span id="cus"></span>
## Contact Us

**Project Lead:** 

- Kaiyu Huang, kyhuang@bjtu.edu.cn
- Fengran Mo, fengran.mo@umontreal.ca

**Section Contributors:**

- Inference: Yulong Mao
- Security: Hongliang Li
- Multidomain: You Li

**Special Thanks:**

- Chaoqun Liu (Nanyang Technological University, Singapore) provides valuable thoughts and contributes part of the implementation of the multilingual inference strategies.

## Citation

```bib
@article{xxx,
  title={A Survey on Large Language Models with Multilingualism: Recent Advances and New Frontiers},
  author={xxx},
  journal={arXiv preprint arXiv:xxx},
  year={2024}
}
```





​	

