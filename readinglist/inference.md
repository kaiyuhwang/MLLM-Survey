# Multilingual Pre-trained Models Tutorial
<img src='C:\Users\huang\AppData\Roaming\Typora\typora-user-images\image-20240516202515585.png' height='400' style="float:left">

Considering the rapid growth of the research of multilingual NLP, we have established this repository to gather relevant literature in this specific multilingual domain.  *(As a contribution of the survey paper "[A Survey on Large Language Models with Multilingualism: Recent Advances and New Frontiers]()")*

This is also a tutorial of multilingual pre-trained models maintained by the Beijing Jiaotong University (BJTU) NLP Group (Continual Updated).

The past five years have witnessed the rapid development of multilingual pre-trained models, especially for data-driven large language models (LLMs). Due to the dominance of multilingual NLP at the present time, priority is given to collecting important, up-to-date multilingual pre-trained models papers and their performance. As one of the contributions of the survey, we continuously update and expand the content according to the chapters in the survey. Our list is still incomplete and the categorization might be inappropriate. We will keep adding papers and improving the list. Any suggestions are welcome!

## LLMs with Multilingualism
We only present an overview of **representative** LLMs (trainable parameters greater than ***7B***) that have certain multilingual capabilities, including their release time and details. The latest models that achieve good performance on the leaderboard will be updated in a timely manner, or contact us for updates and promotion.

### General Multilingual Leaderboard

We investigate the LLMs with multilingualism in our reconstructed benchmarks. *(If there are many versions of a model, we only choose the version that perform the best.)*

In this leaderboard we use a unified *prompt* for each task to explore the multilingual capabilities of the model. The potential enhancement capabilities of the model are explored in the next chapter "**[Multilingual Inference Strategies](##Multilingual Inference Strategies)**".

> 🎈 	Coming soon! The benchmark is under built.

### Open-Source Models

- LLaMA, Meta AI
  - LLaMA-1,
  - LLaMA-2,
  - LLaMA-3,
- GLM, ZHIPU
- Baichuan
- Qwen
- Phi
- Mistral
- OpenChat
- Deepseek
- InternLM
- BLOOM
- Bayling

### Closed-Source Systems

We only investigate a few representative closed-source LLMs because most of these commercial systems are expensive to invoke. We hope to get sponsors or voluntary enterprise responses to compare closed-source systems, otherwise our goal is to discuss the future potential of LLMs within the open-source community.

- GPT, OpenAI
  - ChatGPT (GPT-3.5-turbo)
  - GPT-4

- PaLM, Google
- Claude
- Gemini

## Multilingual Inference Strategies
We investigate several inference strategies for LLMs to explore the potential enhancement capabilities with multilingualism in the related benchmarks. *(The multilingual inference strategies are to act on prompt with external knowledge, and LLMs are frozen.)*

### Reasoning Leaderboard

<table>
    <tr>
        <th>Model</th>
        <th>Method</th>
        <th>MGSM</th>
        <th>XCOPA</th>
        <th>XNLI</th>
        <th>PAWS-X</th>
        <th>MKQA</th>
        <th>Avg.</th>
    </tr>
    <tr>
        <td rowspan="7">GPT-3.5-turbo</td>
        <td>Direct</td>
        <td>49.9</td>
        <td>72.4</td>
        <td>50.6</td>
        <td>50.3</td>
        <td>35.4</td>
        <td>51.7</td>
    </tr>
    <tr>
        <td>Direct</td>
        <td>49.9</td>
        <td>72.4</td>
        <td>50.6</td>
        <td>50.3</td>
        <td>35.4</td>
        <td>51.7</td>
    </tr>
    <tr>
        <td>Direct</td>
        <td>49.9</td>
        <td>72.4</td>
        <td>50.6</td>
        <td>50.3</td>
        <td>35.4</td>
        <td>51.7</td>
    </tr>
    <tr>
        <td>Direct</td>
        <td>49.9</td>
        <td>72.4</td>
        <td>50.6</td>
        <td>50.3</td>
        <td>35.4</td>
        <td>51.7</td>
    </tr>
    <tr>
        <td>Direct</td>
        <td>49.9</td>
        <td>72.4</td>
        <td>50.6</td>
        <td>50.3</td>
        <td>35.4</td>
        <td>51.7</td>
    </tr>
    <tr>
        <td>Trans-Google</td>
        <td>73.9</td>
        <td>84.5</td>
        <td>60.5</td>
        <td>67.2</td>
        <td>43.8</td>
        <td>66.0</td>
    </tr>
    <tr>
        <td>Trans-NLLB</td>
        <td>61.0</td>
        <td>79.7</td>
        <td>59.2</td>
        <td>67.5</td>
        <td>37.2</td>
        <td>60.9</td>
    </tr>
</table>


| 49.9 | 72.4 | 50.6 | 50.3 | 35.4 | 51.72 |
| ---- | ---- | ---- | ---- | ---- | ----- |
| 61.1 | 78.6 | 56.4 | 61.6 | 42.9 | 60.12 |
| 62.3 | 79.3 | 59.2 | 59.4 | 37.6 | 59.56 |


### Baseline Details



## Security


### Jailbreaking



### Defense



## Multidomain

### Legal

### Medical

### Finance

> Coming soon! This domain is under updated.

## Data Resource & Evaluation
### Benchmark

