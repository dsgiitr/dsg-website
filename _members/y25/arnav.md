---
title: ""
permalink: /members/arnav/
layout: single
---


# Arnav Bendre

<img src="{{ site.baseurl }}/assets/images/members/y25/arnav.png" width="200" height="200" alt="Arnav Bendre">


*Core Member, DSG IIT Roorkee*

---

## Education  
- **BTech**, Energy Engineering , IIT Roorkee (2024–2029)    
---

## Research Interests  
- Computer vision
- Probabilistic Modeling
- Multimodal Safety
- Efficient Inference

---

## Projects  
### BranchDistillation: Dense Supervision for Diffusion Distillation
*Accepted as B-DENSE at the ICLR 2026 Workshop on Deep Learning for Theory (DeLTa)*
- Built a diffusion-distillation framework that supervises the student on the teacher's full denoising trajectory through K-fold branched output channels, recovering the intermediate denoising steps that standard distillation discards.
- Cut FID against Progressive Distillation on CIFAR-10 (39.66 → 20.81 at 128 steps) and against SFD on ImageNet-64 at NFE 2 (10.25 → 9.57), for ~0.01% extra FLOPs and identical inference cost.

### Rethinking Contrastive Decoding
*Reproducibility study and extension, arXiv preprint (2026)*
- Stress-tested contrastive decoding methods (VCD, ICD, SID) for object hallucination across LLaVA-1.5 (7B/13B) and Qwen2.5-VL on POPE, MME and CHAIR.
- Showed CD is statistically indistinguishable from spurious, non-visual control methods: its gains come from a recall shift (+12.21pp, p<0.001), not better visual grounding.
- Used logit-lens analysis to localize the layers where the intervention breaks down, showing CD's apparent gains are a distributional artifact rather than corrected perception.

### Refusal Across Modalities in Vision-Language Models
*Does a VLM have one refusal direction for text and images, or does the image pathway carry a separate, weaker signal?*
- Extracted text- and image-side refusal directions (class-mean differences of last-token residual-stream states at every layer) from LLaVA-1.5-7B and Qwen2.5-VL-7B, using 1,040 AdvBench/Alpaca prompts, each also rendered as an image.
- The result depends on architecture. In adapter-style LLaVA the two directions stay apart (peak cosine 0.45, image vector 2–9× weaker at every layer, modality gap persists to the last layer). In natively trained Qwen they merge by about two-thirds depth (cosine 0.95, equal norms, no modality gap in PCA).
- Checked that the gap is real with bootstrap CIs, a split-half noise ceiling (~0.99), disattenuated cosines and a random-direction null (0.03).
- Causal steering on LLaVA: adding the text refusal direction to harmless images makes the model refuse ~40–45% of them (≤3% for a random direction of the same norm). The image direction does not transfer back: it never induces refusal on text, and ablating it only cuts text refusal from 0.79 to 0.54, against 0.04 for the text direction.

### Visual-CoT
- Built an end-to-end, resumable pipeline that turns raw ChartQA samples into a supervised fine-tuning corpus of structured visual chain-of-thought traces (chart summary → extraction → computation → answer).
- Sampled 3 traces per item from a frontier VLM teacher and filtered them through five gates (schema, answer correctness, numeric grounding, arithmetic re-verification, 2-of-3 self-consistency), keeping the best-grounded trace at a 95% yield.






---

## Follow
[GitHub](https://github.com/Aurnawr) | [LinkedIn](https://www.linkedin.com/in/arnav-bendre-3b8466323/) | [Portfolio](https://aurnawr.github.io/)

---
