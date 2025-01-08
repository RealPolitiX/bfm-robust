# bfm-robust
Companion repo for robustness specification in biomedical foundation models (BFMs)

Please cite the following preprint for reference
```
@misc{xian_robustness_2024,
    address = {Rochester, NY},
    type = {{SSRN} {Scholarly} {Paper}},
    title = {Robustness tests for biomedical foundation models should tailor to specification},
    url = {https://papers.ssrn.com/abstract=5013799},
    doi = {10.2139/ssrn.5013799},
    language = {en},
    urldate = {2024},
    publisher = {Social Science Research Network},
    author = {Xian, Patrick and Baker, Noah R. and David, Tom and Cui, Qiming and Holmgren, A. Jay and Bauer, Stefan and Sushil, Madhumita and Abbasi-Asl, Reza},
    month = jan,
    year = {2024},
    keywords = {AI policy, foundation model, health AI, robustness},
}
```

## Robustness tests in existing BFMs
We carreid out the search of BFMs from a few existing GitHub repositories, review papers, and directly on the internet. We selected a total of about 50 representative BFMs (mostly published in 2023-2024) in publication and preprints, covering a broad range of biomedical domains. We then extracted the relevant information on the model name, developers, modality, domain, capabilities, and any robustness tests that have been described for the each model. The information is gathered [here](https://docs.google.com/spreadsheets/d/1i2Nj4xRwwnwCti14fFUopJvHaZQyDi6ycnmAAHAYTbA/edit?usp=sharing). In the following, we break down the claimed robustness tests conducted for the BFMs. While about a third of the models don't have an explicit robustness test, a small number of models have been subject to multiple ones.

<span style="color:yellowgreen">32\%</span> &ensp; None<br>
<span style="color:yellowgreen">32\%</span> &ensp; Evaluation on multiple existing datasets (including public datasets used for finetuning)<br>
<span style="color:yellowgreen">16\%</span> &ensp; Evaluation on artificially shifted datasets (including perturbed and synthetic datasets)<br>
<span style="color:yellowgreen">8\%</span> &emsp; Evaluation on external datasets (datasets not used in development)<br>
<span style="color:yellowgreen">8\%</span> &emsp; Ablation studies<br>
<span style="color:yellowgreen">6\%</span> &emsp; Others<br>

None indicates no specified robustness tests. Most claimed robustness tests in the selected BFMs involve evaluation of model performance on some datasets, which we divide into three types: existing datasets, artificially shifted datasets, and external datasets.

## Robustness categorization and examples
A combination of theoretical and application-oriented resources are collected for robustness. The categorization of robustness follows that provided in the paper.

### Surveys \& tutorials (general domains)
Robustness in the context of foundation models
* [A.I. Robustness: a Human-Centered Perspective on Technological Challenges and Opportunities](https://dl.acm.org/doi/10.1145/3665926), *ACM Comput. Surv.* (2024)
* [Robustness at Inference: Towards Explainability, Uncertainty, and Intervenability](https://alregib.ece.gatech.edu/courses-and-tutorials/cvpr-2024-tutorial/), CVPR Tutorial (2024)
* [Machine Learning Robustness: A Primer](https://arxiv.org/abs/2404.00897), arXiv:2404.00897
* [Spurious Correlations in Machine Learning: A Survey](https://arxiv.org/abs/2402.12715), arXiv:2402.12715
* [Foundational Robustness of Foundation Models](https://sites.google.com/view/neurips2022-frfm-turotial/home), NeurIPS Tutorial (2022)

### Surveys \& tutorials (biomedical domains)
* [Toward a framework for risk mitigation of potential misuse of artificial intelligence in biomedical research](https://www.nature.com/articles/s42256-024-00926-3), *Nat. Mach. Intell.* (2024)
* [SoK: Security and Privacy Risks of Medical AI](https://arxiv.org/abs/2409.07415), arXiv:2409.07415
* [Ethical and regulatory challenges of large language models in medicine](https://www.sciencedirect.com/science/article/pii/S258975002400061X), *Lancet Digit. Health* (2024)
* [Developing robust benchmarks for driving forward AI innovation in healthcare](https://www.nature.com/articles/s42256-022-00559-4), *Nat. Mach. Intell.* (2022)
* [Shifting machine learning for healthcare from development to deployment and from models to data](https://www.nature.com/articles/s41551-022-00898-y), *Nat. Biomed. Eng.* (2022)
* [Secure and Robust Machine Learning for Healthcare: A Survey](https://ieeexplore.ieee.org/abstract/document/9153891), *IEEE Rev. Biomed. Eng.* (2020)

### Group robustness
* [Prompting is a Double-Edged Sword: Improving Worst-Group Robustness of Foundation Models](https://proceedings.mlr.press/v235/setlur24a.html), ICML (2024)
* [Improving Group Robustness on Spurious Correlation Requires Preciser Group Inference](https://proceedings.mlr.press/v235/han24g.html), ICML (2024)
* [Controllable Prompt Tuning For Balancing Group Distributional Robustness](https://proceedings.mlr.press/v235/phan24b.html), ICML (2024)
* [Multigroup Robustness](https://proceedings.mlr.press/v235/hu24l.html), ICML (2024)
* [Change is hard: a closer look at subpopulation shift](https://proceedings.mlr.press/v202/yang23s.html), ICML (2023)
* [Improving Out-of-Distribution Robustness via Selective Augmentation](https://proceedings.mlr.press/v162/yao22b.html), ICML (2022)
* [Just Train Twice: Improving Group Robustness without Training Group Information](https://proceedings.mlr.press/v139/liu21f.html), ICML (2021)
* [No Subclass Left Behind: Fine-Grained Robustness in Coarse-Grained Classification Problems](https://proceedings.neurips.cc/paper/2020/hash/e0688d13958a19e087e123148555e4b4-Abstract.html), NeurIPS (2020)

### Instance-wise robustness
* [Characterizing Data Point Vulnerability as Average-Case Robustness](https://proceedings.mlr.press/v244/han24a.html), UAI (2024)
* [Characterizing the Impacts of Instances on Robustness](https://aclanthology.org/2023.findings-acl.146/), ACL (2023)

### Interventional robustness
* [Causality-oriented robustness: exploiting general additive interventions](https://arxiv.org/abs/2307.10299), arXiv:2307.10299
* [Certified Robustness Against Natural Language Attacks by Causal Intervention](https://proceedings.mlr.press/v162/zhao22g.html), ICML (2022)
* [Towards Causal Representation Learning](https://ieeexplore.ieee.org/document/9363924), *Proc. IEEE* (2021)
* [A causal view on robustness of neural networks](https://proceedings.neurips.cc/paper_files/paper/2020/hash/02ed812220b0705fabb868ddbf17ea20-Abstract.html), NeurIPS (2020)
* [Invariance, Causality and Robustness](https://projecteuclid.org/journals/statistical-science/volume-35/issue-3/Invariance-Causality-and-Robustness/10.1214/19-STS721.full), *Statist. Sci.* (2020)

### Aggregated robustness
* [Ensemble everything everywhere: Multi-scale aggregation for adversarial robustness](https://arxiv.org/abs/2408.05446), arXiv:2408.05446
* [On the Adversarial Robustness of Mixture of Experts](https://proceedings.neurips.cc/paper_files/paper/2022/hash/3effb91593c4fb42b1da1528328eff49-Abstract-Conference.html), NeurIPS (2022)

### Uncertainty awareness \& Uncertainty-aware robustness
* [Domain-specific or Uncertainty-aware models: Does it really make a difference for biomedical text classification?](https://aclanthology.org/2024.bionlp-1.16/), ACL BioNLP Workshop (2024)
* [Certainly Uncertain: A Benchmark and Metric for Multimodal Epistemic and Aleatoric Awareness](https://arxiv.org/abs/2407.01942), arXiv:2407.01942
* [Uncertainty-Aware Pre-Trained Foundation Models for Patient Risk Prediction via Gaussian Process](https://dl.acm.org/doi/10.1145/3589335.3651456), WWW (2024)

### Longitudinal/Temporal robustness
* [Pathophysiological Features in Electronic Medical Records Sustain Model Performance under Temporal Dataset Shift](https://pmc.ncbi.nlm.nih.gov/articles/PMC11141811/), AMIA (2024)
* [Temporal Robustness against Data poisoning](https://proceedings.neurips.cc/paper_files/paper/2023/hash/94bcb01789fccf15afe2764d8fe0f40e-Abstract-Conference.html), NeurIPS (2023)
* [Stable clinical risk prediction against distribution shift in electronic health records](https://www.cell.com/patterns/fulltext/S2666-3899(23)00197-6), *Patterns* (2023)
* [EHR foundation models improve robustness in the presence of temporal distribution shift](https://www.nature.com/articles/s41598-023-30820-8), *Sci. Rep.* (2023)
* [DeepJoint: Robust Survival Modelling Under Clinical Presence Shift](https://openreview.net/forum?id=ujVubluRFHH), NeurIPS Workshp (2022)
* [Evaluation of domain generalization and adaptation on improving model robustness to temporal dataset shift in clinical medicine](https://www.nature.com/articles/s41598-022-06484-1), *Sci. Rep.* (2022)
* [Longitudinal Adversarial Attack on Electronic Health Records Data](https://dl.acm.org/doi/abs/10.1145/3308558.3313528), WWW (2019)

### Knowledge robustness
* [Medical large language models are susceptible to targeted misinformation attacks](https://www.nature.com/articles/s41746-024-01282-7), *npj Digit. Med.* (2024)
* [PromptSmooth: Certifying Robustness of Medical Vision-Language Models via Prompt Learning](https://link.springer.com/chapter/10.1007/978-3-031-72390-2_65), MICCAI (2024)
* [BAPLe: Backdoor Attacks on Medical Foundational Models using Prompt Learning](https://arxiv.org/abs/2408.07440), arXiv:2408.07440
* [Large Diverse Ensembles for Robust Clinical NLI](https://aclanthology.org/2024.semeval-1.224/), SemEval (2024)
* [MedFuzz: Exploring the Robustness of Large Language Models in Medical Question Answering](https://arxiv.org/abs/2406.06573), arXiv:2406.06573
* [Adversarial Attacks on Large Language Models in Medicine](https://arxiv.org/abs/2406.12259), arXiv:2406.12259
* [Poisoning medical knowledge using large language models](https://www.nature.com/articles/s42256-024-00899-3), *Nat. Mach. Intell.* (2024)
* [Backdoor Attack on Unpaired Medical Image-Text Foundation Models: A Pilot Study on MedCLIP](https://ieeexplore.ieee.org/document/10516621), SaTML (2024)
* [Assessing biomedical knowledge robustness in large language models by query-efficient sampling attacks](https://openreview.net/forum?id=pvol5JyVYB), TMLR (2024)
* [Demonstration of an Adversarial Attack Against a Multimodal Vision Language Model for Pathology Imaging](https://arxiv.org/abs/2401.02565), arXiv:2401.02565
* [Robust and data-efficient generalization of self-supervised machine learning for diagnostic imaging](https://www.nature.com/articles/s41551-023-01049-7), *Nat. Biomed. Eng.* (2023)

### Behavioral robustness
* [Latent Adversarial Training Improves Robustness to Persistent Harmful Behaviors in LLMs](https://arxiv.org/abs/2407.15549), arXiv:2407.15549
* [An Auditing Test To Detect Behavioral Shift in Language Models](https://openreview.net/forum?id=N0lEOF2eDm), ICML Workshop (2024)
* [Robust Conversational Agents against Imperceptible Toxicity Triggers](https://aclanthology.org/2022.naacl-main.204/), NAACL (2022)

### Pref-BFM adversarial robustness (language)
* [Evaluating the Robustness of Adverse Drug Event Classification Models using Templates](https://aclanthology.org/2024.bionlp-1.3/), ACL BioNLP Workshop (2024)
* [Incorporating Data Augmentation with Generative Models and Biomedical Knowledge to Enhance Inference Robustness](https://aclanthology.org/2024.semeval-1.15/), SemEval (2024)
* [Enhancing Robustness of Foundation Model Representations under Provenance-related Distribution Shifts](https://openreview.net/forum?id=9TVx8T0U1h), NeurIPS DistShift Workshop (2023)
* [Evaluating the Robustness of Biomedical Concept Normalization](https://proceedings.mlr.press/v203/chakraborty23a.html), NeurIPS TLNLP Workshop (2022)
* [Improving the robustness and accuracy of biomedical language models through adversarial training](https://www.sciencedirect.com/science/article/pii/S1532046422001307), *J. Biomed. Inform.* (2022)

### Pref-BFM adversarial robustness (vision)
* [Adversarial attacks in radiology – A systematic review](https://www.ejradiology.com/article/S0720-048X(23)00399-6/fulltext), *Eur. J. Radiol.* (2023)
* [Adversarial attacks and adversarial robustness in computational pathology](https://www.nature.com/articles/s41467-022-33266-0), *Nat. Comm.* (2022)
* [Advancing diagnostic performance and clinical usability of neural networks via adversarial training and dual batch normalization](https://www.nature.com/articles/s41467-021-24464-3), *Nat. Comm.* (2021)
* [Adversarial attacks on medical machine learning](https://www.science.org/doi/10.1126/science.aaw4399), *Science* (2019)

### Robustness evaluation \& monitoring
* [Scalable Drift Monitoring in Medical Imaging AI](https://arxiv.org/abs/2410.13174), arXiv:2410.13174
* [The Data Addition Dilemma](https://arxiv.org/abs/2408.04154), arXiv:2408.04154
* [Empirical data drift detection experiments on real-world medical imaging data](https://www.nature.com/articles/s41467-024-46142-w), *Nat. Comm.* (2024)
* [Off-label use of artificial intelligence models in healthcare](https://www.nature.com/articles/s41591-024-02870-6), *Nat. Med.* (2024)
* [Understanding Liability Risk from Using Health Care Artificial Intelligence Tools](https://www.nejm.org/doi/abs/10.1056/NEJMhle2308901), *New Eng. J. Med.* (2024)
* [Can You Rely on Your Model Evaluation? Improving Model Evaluation with Synthetic Test Data](https://proceedings.neurips.cc/paper_files/paper/2023/hash/05fb0f4e645cad23e0ab59d6b9901428-Abstract-Conference.html), NeurIPS (2023)
* [External validation of AI models in health should be replaced with recurring local validation](https://www.nature.com/articles/s41591-023-02540-z), *Nat. Med.* (2023)
* [Diagnosing and remediating harmful data shifts for the responsible deployment of clinical AI models](https://www.medrxiv.org/content/10.1101/2023.03.26.23286718v2), medRxiv:2023.03.26.23286718
* [Evaluating Robustness to Dataset Shift via Parametric Robustness Sets](https://proceedings.neurips.cc/paper_files/paper/2022/hash/6b7f9d9c1217a748391800871ff7d17d-Abstract-Conference.html), NeurIPS (2022)
* [A Fine-Grained Analysis on Distribution Shift](https://openreview.net/forum?id=Dl4LetuLdyK), ICLR (2022)
* [Mandoline: Model Evaluation under Distribution Shift](https://proceedings.mlr.press/v139/chen21i.html), ICML (2021)