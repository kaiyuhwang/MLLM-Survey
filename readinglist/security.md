# Security

## Attack
### Greedy Coordinate Gradient Series Attack Methods
* Andy Zou, Zifan Wang, Nicholas Carlini, Milad Nasr, J.Zico Kolter, Matt Fredrikon. 2023. [Universal and Transferable Adversarial Attacks on Aligned Language Models](https://arxiv.org/abs/2307.15043). *arXiv:2307.15043*.
* Chawin Sitawarin, Norman Mu, David Wagner, Alexandre Araujo. 2024. [PAL: Proxy-Guided Black-Box Attack on Large Language Models](https://arxiv.org/abs/2402.09674). *arXiv:2402.09674*.

### Prompt-based Attack Methods
* Alexander Wei, Nika Haghtalab, and Jacob Steinhardt. 2024. [Jailbroken: How does llm safety training fail?](https://proceedings.neurips.cc/paper_files/paper/2023/file/fd6613131889a4b656206c50a8bd7790-Paper-Conference.pdf) *Advances in Neural Information Processing Systems, 36*.
* Yi Liu, Gelei Deng, Zhengzi Xu, Yuekang Li, Yaowen Zheng, Ying Zhang, Lida Zhao, Tianwei Zhang, and Yang Liu. 2023. [Jailbreaking chatgpt via prompt engineering: An empirical study.](https://arxiv.org/pdf/2305.13860). *arXiv:2305.13860*.
* Xinyue Shen, Zeyuan Chen, Michael Backes, Yun Shen, and Yang Zhang. 2023. ["do anything now":
Characterizing and evaluating in-the-wild jailbreak prompts on large language models](https://arxiv.org/pdf/2308.03825).  *arXiv:2308.03825.*
* Gelei Deng, Yi Liu, Yuekang Li, Kailong Wang, Ying Zhang, Zefeng Li, Haoyu Wang, Tianwei Zhang, and Yang Liu. 2024. [Masterkey: Automated jailbreaking of large language model
chatbots.](https://www.ndss-symposium.org/wp-content/uploads/2024-188-paper.pdf)  *In Proc. ISOC NDSS*.
* Lijun Li, Bowen Dong, Ruohui Wang, Xuhao Hu, Wangmeng Zuo, Dahua Lin, Yu Qiao,
and Jing Shao. 2024. [Salad-bench: A hierarchical and comprehensive safety benchmark for large
language models](https://arxiv.org/pdf/2402.05044). *arXiv:2402.05044*. 
* Xiaogeng Liu, Nan Xu, Muhao Chen, and Chaowei Xiao. 2023. [Autodan: Generating stealthy
jailbreak prompts on aligned large language models.](https://arxiv.org/pdf/2310.04451) *arXiv:2310.04451*. 
* Haibo Jin, Ruoxi Chen, Andy Zhou, Jinyin Chen, Yang Zhang, and Haohan Wang. 2024. [Guard:
Role-playing to generate natural-language jailbreakings to test guideline adherence of large
language models.](https://arxiv.org/pdf/2402.03299) *arXiv:2402.03299*.

### Multilingual Attack Methods
* Lingfeng Shen, Weiting Tan, Sihao Chen, Yunmo Chen, Jingyu Zhang, Haoran Xu, Boyuan
Zheng, Philipp Koehn, and Daniel Khashabi. 2024. [The language barrier: Dissecting safety challenges of llms in multilingual contexts](https://arxiv.org/pdf/2401.13136). 
* Yue Deng, Wenxuan Zhang, Sinno Jialin Pan, and Lidong Bing. 2023. [Multilingual jailbreak challenges in large language models](https://arxiv.org/pdf/2310.06474). *arXiv:2310.06474*. 
* Poorna Chander Reddy Puttaparthi, Soham Sanjay Deo, Hakan Gul, Yiming Tang, Weiyi
Shang, and Zhe Yu. 2023. [Comprehensive evaluation of chatgpt reliability through multilingual
inquiries](https://arxiv.org/pdf/2312.10524). 
* Zheng-Xin Yong, Cristina Menghini, and Stephen H Bach. 2023. [Low-resource languages jailbreak
gpt-4](https://arxiv.org/pdf/2310.02446). *arXiv:2310.02446*.
* Nan Xu, Fei Wang, Ben Zhou, Bang Zheng Li, Chaowei Xiao, and Muhao Chen. 2023. [Cognitive overload: Jailbreaking large language models with overloaded logical thinking](https://arxiv.org/pdf/2311.09827). *arXiv:2311.09827*.
* Jie Li, Yi Liu, Chongyang Liu, Ling Shi, Xiaoning Ren, Yaowen Zheng, Yang Liu, and
Yinxing Xue. 2024. [A cross-language investigation into jailbreak attacks in large language models.](https://arxiv.org/pdf/2401.16765).
*arXiv:2401.16765*. 
* Youliang Yuan, Wenxiang Jiao, Wenxuan Wang, Jen tse Huang, Pinjia He, Shuming Shi, and
Zhaopeng Tu. 2024. [Gpt-4 is too smart to be safe: Stealthy chat with llms via cipher](https://arxiv.org/pdf/2308.06463). 
* Yangsibo Huang, Samyak Gupta, Mengzhou Xia, Kai Li, and Danqi Chen. 2023. [Catastrophic
jailbreak of open-source llms via exploiting generation](https://arxiv.org/pdf/2310.06987). *arXiv:2310.06987*.



## Defense
We are surveying more defenses.
### For Open-Source Models
* Yue Deng, Wenxuan Zhang, Sinno Jialin Pan, and Lidong Bing. 2023. [Multilingual jailbreak challenges in large language models](https://arxiv.org/pdf/2310.06474). *arXiv:2310.06474*. 
* Jie Li, Yi Liu, Chongyang Liu, Ling Shi, Xiaoning Ren, Yaowen Zheng, Yang Liu, and
Yinxing Xue. 2024. [A cross-language investigation into jailbreak attacks in large language models.](https://arxiv.org/pdf/2401.16765).
* Alexander Robey, Eric Wong, Hamed Hassani, and George J Pappas. 2023. [Smoothllm: Defending
large language models against jailbreaking attacks](https://arxiv.org/pdf/2310.03684). *arXiv:2310.03684*. 
* Andy Zhou, Bo Li, and Haohan Wang. 2024. [Robust prompt optimization for defending language
models against jailbreaking attacks](https://arxiv.org/pdf/2401.17263). *arXiv:2401.17263*. 



### For Close-Source Models
P.S. These Defense Methods are also suitable for open-source models.
* Neel Jain, Avi Schwarzschild, Yuxin Wen, Gowthami Somepalli, John Kirchenbauer, Pingyeh Chiang, Micah Goldblum, Aniruddha Saha, Jonas Geiping, and Tom Goldstein. 2023. [Baseline defenses for adversarial attacks against aligned language models.](https://arxiv.org/pdf/2309.00614) *arXiv:2309.00614*. 
* Daoyuan Wu, Shuai Wang, Yang Liu, and Ning Liu. 2024. [Llms can defend themselves against
jailbreaking in a practical manner: A vision paper](https://arxiv.org/pdf/2402.15727). 
* Yuhui Li, Fangyun Wei, Jinjing Zhao, Chao Zhang, and Hongyang Zhang. 2023. [Rain: Your language models can align themselves without finetuning](https://arxiv.org/pdf/2309.07124). *In The Twelfth International Conference on Learning Representations*. 
