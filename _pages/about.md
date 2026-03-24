---
permalink: /
title: "Yuxuan's Homepage"
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
---
layout: default
title: "Qiuhao Liu - AI Algorithm Engineer"
---

# About Me

I am **Qiuhao Liu (刘秋浩)**, an AI Algorithm Engineer currently working at **Alibaba Quark** in Beijing. I obtained my Master's degree in Electronic Information Engineering from **Nanyang Technological University (NTU)** in 2026, where I was honored as an **Outstanding Graduate (Top 10%)** and **Outstanding Student Teaching Assistant (5 recipients university-wide)**.

My research interests include **Deep Learning**, **Reinforcement Learning**, **Large Language Models**, and **Recommendation Systems**. I am passionate about bridging the gap between cutting-edge research and real-world applications.

---

## 🎓 Education

### Nanyang Technological University (NTU)
**Master of Engineering in Electronic Information Engineering** | *Sept 2024 - Feb 2026*
- QS World Ranking: 12th | Major Ranking: Top 10%
- **Honors:**
  - NTU Outstanding Graduate (Top 10%)
  - Outstanding Student Teaching Assistant (Only 5 recipients university-wide)
- **Thesis:** "Reinforcement Learning Enhanced RIS (Reconfigurable Intelligent Surface) Intelligent Reflective Panel Optimization Deployment"
  - Supervisor: Prof. Chao Yuan (IEEE Fellow)

### Beijing Jiaotong University (BJTU)
**Bachelor of Engineering in Electronic Information Engineering** | *Sept 2020 - June 2024*
- 211 Project University | Major Ranking: Top 20%
- **Honors:**
  - Beijing Outstanding Graduate
  - University Merit Student
  - National Physics Competition Third Prize (Top 10%)
  - Electronic Design Contest Second Prize
- **Core Courses:**
  - Data Structures: 98/100
  - ACM Programming: 97/100
  - Deep Learning & Pattern Recognition: 92/100
  - Video Signal Processing: 98/100
  - Linear Algebra: 98/100
  - Probability Theory: 94/100

---

## 📝 Publications

1. **Qiuhao Liu** (First Author), Ling Li, Yao Lu, Qi Xuan, Zhaowei Zhu, Jiaheng Wei. 
   *"SelectMix: Enhancing Label Noise Robustness through Targeted Sample Mixing"* 
   **ICML 2026 (Submitted)** | CCF-A Conference

2. **Qiuhao Liu** (First Author), Jiakang Zheng, Jiayi Zhang. 
   *"High-Speed Train Communications with XL-MIMO-OFDM: Performance Analysis and Optimization for URLLC"* 
   **IEEE Transactions on Wireless Communications (TWC)** | Major Revision | SCI Q1

3. **Qiuhao Liu** (First Author), Yonghao Lin, Jiakang Zheng, Zhe Wang, Jiayi Zhang, Bo Ai. 
   *"Performance Analysis of XL-MIMO-OFDM Systems for High-Speed Train Communications"* 
   **2023 IEEE ICC Workshops**, 2023, pp. 1741-1746 | CORE-A | Top Conference in Communications

---

## 💼 Work Experience

### Alibaba Quark - AI Algorithm Engineer
**Large Language Model Generative Recommendation & Ranking System** | *Nov 2025 - Feb 2026* | Beijing

**Main Responsibilities:**
- Optimizing large language models (LLMs) for generative recommendation and document reranking scenarios
- Focusing on sequence modeling, reranking decoding, and system architecture design
- Driving the deployment of LLM ranking solutions in real-world business applications

**Key Problems Solved:**

1. **Inefficient Sequence Modeling**
   - Challenge: Traditional LLM recommendation methods convert user history into long text input, resulting in extremely long sequences with high inference costs and difficulty modeling long-term interests
   - Solution: Designed hierarchical LLM modeling approach, using contrastive learning to compress user history into fixed-length dense vectors, reducing input length by 80% while improving recommendation accuracy by 5.2%

2. **Slow Reranking Decoding**
   - Challenge: Existing ranking LLMs (e.g., RankGPT) require token-by-token text generation for sorting, with huge output space and generation of invalid explanations
   - Solution: Proposed logit-based ranking method, directly computing probability distribution of candidate items at special tokens, eliminating text generation, achieving 30x speedup with comparable accuracy

3. **Objective Inconsistency & Candidate Truncation**
   - Challenge: In traditional multi-stage cascade ranking, different stages have inconsistent optimization objectives, easily losing high-potential candidates in early truncation, limiting overall ranking ceiling
   - Solution: Implemented end-to-end joint training framework, enabling LLM to perceive the complete ranking funnel during training, reducing early truncation loss rate by 40%

**Technical Highlights:**
- Built hierarchical LLM modeling + contrastive learning + memory mechanism architecture
- Designed logit-based direct ranking method, eliminating text generation overhead
- Implemented end-to-end joint training, achieving objective consistency across cascade stages
- Developed real-time inference optimization, reducing P99 latency from 1.2s to 400ms

**Project Impact:**
- System deployed to production with 50 million+ daily active users
- CTR improved by 3.8%, user engagement time increased by 6.2%
- Inference cost reduced by 70% while maintaining performance

---

### 2. Large Language Model Agent RAG Q&A Development & Optimization
**Financial Insurance Domain** | *Dec 2024 - Mar 2025*

**Project Description:**
Built a Retrieval-Augmented Generation (RAG) question-answering system for financial insurance business, integrating 5000+ multimodal documents (PDF, PPT, scanned images, video subtitles, etc.) to provide instant Q&A services based on local knowledge base for Far East Smarter Union Financial Company employees.

**Technical Highlights:**

1. **RAG Retrieval & Knowledge Construction**
   - Built local knowledge base system using llamaindex + Milvus + BGE
   - Adopted BM25 + vector similarity hybrid recall
   - Achieved precise matching of tens of thousands of product information
   - Recall@10 improved from 10% to 89%

2. **Multi-Agent Workflow**
   - Used ReAct + Reflection + Memory mechanisms
   - Decomposed user requirements for different Agents to execute
   - Including local knowledge retrieval and Web search invocation sequence
   - Reflection module for thinking and correction
   - Memory module for context retention
   - Achieved deep answers to complex questions like human sales

3. **Query Rewriting & Expansion**
   - Performed error correction and synonym expansion for colloquial, typo-ridden, and short questions
   - Example: "推销保险" → "销售保险产品"
   - Improved retrieval hit rate for short queries

4. **Embedding Fine-tuning**
   - Conducted contrastive learning fine-tuning on BGE/SimCSE and other pre-trained models using internal insurance domain Q&A data
   - Enhanced semantic understanding of terms like "保单现金价值", "住院医疗险"
   - Significantly improved precision and recall of domain semantic retrieval

5. **Multi-turn Dialogue Context Management**
   - Injected context for user follow-up questions
   - Injected core entities from previous round (e.g., "寿险产品ABC") into new questions
   - Or automatically replaced pronouns with explicit objects (Query Rewrite) before retrieval
   - Ensured semantic coherence in multi-turn interactions

**Retrieval Accuracy:**
- Hybrid retrieval + fine-tuning + reranking strategy achieved in internal testing:
  - Top 5 accurate recall rate improved from 65% to 88%
  - MRR improved from 0.50 to 0.72

**System Stability & Online:**
- The RAG system has been deployed for internal enterprise use
- Supports multiple scenarios including sales teams and customer service departments
- Monthly call volume exceeds 100,000 times
- Received positive feedback

---

## 🛠️ Technical Skills

**Programming Languages:**
- Python, C++, MATLAB

**Frameworks & Tools:**
- PyTorch (Deep Learning)
- Git (Version Control)
- Transformers Architecture
- RAG Systems (llamaindex, Milvus, BGE)
- LLM Technologies (GRPO, DAPO, GSPO, ARPO)

**Research Interests:**
- Deep Learning & Reinforcement Learning
- Large Language Models
- Recommendation Systems & Ranking
- Multi-Agent Systems
- Retrieval-Augmented Generation (RAG)

---

## 📧 Contact

- **Email:** 17380666715@163.com
- **Phone:** 173-8066-6715
- **Location:** Beijing, China
- **GitHub:** [QiuhaoLiu](https://github.com/QiuhaoLiu)
- **Google Scholar:** [Profile](https://scholar.google.com/citations?user=YOUR_GOOGLE_SCHOLAR_ID)

---

## 💡 Self-Evaluation

- **Pursuing Cutting-edge Development:** Familiar with GRPO technology and its derivative techniques (DAPO, GSPO, ARPO, etc.), well-versed in Transformers architecture
- **Strong Coding Ability:** Proficient in Python, C++, and MATLAB; skilled in PyTorch framework; capable of independently completing deep learning tasks; using Git for project version management
- **Research & Innovation:** Published papers in top-tier conferences (ICML) and SCI Q1 journals (IEEE TWC)
- **Practical Experience:** Successfully deployed large-scale AI systems serving millions of users in production environments

---

*Last updated: March 2026*



I'm a last year master student from Electrical and Electronic Engineering, [Nanyang Technological University (NTU), Singapore](https://www.ntu.edu.sg/). Prior to this, I received B.Eng. degree at Beijing Jiaotong University, China, supervised by Prof. Jiayi Zhang. My research interest includes Machine Learning, Noisy Label and LLM.

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. Suspendisse condimentum, libero vel tempus mattis, risus risus vulputate libero, elementum fermentum mi neque vel nisl. Maecenas facilisis maximus dignissim. Curabitur mattis vulputate dui, tincidunt varius libero luctus eu. Mauris mauris nulla, scelerisque eget massa id, tincidunt congue felis. Sed convallis tempor ipsum rhoncus viverra. Pellentesque nulla orci, accumsan volutpat fringilla vitae, maximus sit amet tortor. Aliquam ultricies odio ut volutpat scelerisque. Donec nisl nisl, porttitor vitae pharetra quis, fringilla sed mi. Fusce pretium dolor ut aliquam consequat. Cras volutpat, tellus accumsan mattis molestie, nisl lacus tempus massa, nec malesuada tortor leo vel quam. Aliquam vel ex consectetur, vehicula leo nec, efficitur eros. Donec convallis non urna quis feugiat.

My research interest includes neural machine translation and computer vision. I have published more than 100 papers at the top international AI conferences with total <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'>google scholar citations <strong><span id='total_cit'>260000+</span></strong></a> (You can also use google scholar badge <a href='https://scholar.google.com/citations?user=DhtAFkwAAAAJ'><img src="https://img.shields.io/endpoint?url={{ url | url_encode }}&logo=Google%20Scholar&labelColor=f6f6f6&color=9cf&style=flat&label=citations"></a>).


# 🔥 News
- *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
- *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 

# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPR 2016</div><img src='images/500x300.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[Deep Residual Learning for Image Recognition](https://openaccess.thecvf.com/content_cvpr_2016/papers/He_Deep_Residual_Learning_CVPR_2016_paper.pdf)

**Kaiming He**, Xiangyu Zhang, Shaoqing Ren, Jian Sun

[**Project**](https://scholar.google.com/citations?view_op=view_citation&hl=zh-CN&user=DhtAFkwAAAAJ&citation_for_view=DhtAFkwAAAAJ:ALROH1vI_8AC) <strong><span class='show_paper_citations' data='DhtAFkwAAAAJ:ALROH1vI_8AC'></span></strong>
- Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
</div>
</div>

- [Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet](https://github.com), A, B, C, **CVPR 2020**

# 🎖 Honors and Awards
- *2021.10* Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
- *2021.09* Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 

# 📖 Educations
- *2024.08 - 2025.06 (expected)*, M.S., Nanyang Technological University . 
- *2020.09 - 2024.06*, B.Eng., Beijing Jiaotong University.


# 💬 Invited Talks
- *2021.06*, Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
- *2021.03*, Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet.  \| [\[video\]](https://github.com/)

# 💻 Internships
- *2019.05 - 2020.02*, [Lorem](https://github.com/), China.
