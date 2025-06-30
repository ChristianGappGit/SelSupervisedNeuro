# SelSupervisedNeuro
Self‑supervised Modelling of Neuroimaging Data: Developing a Basic Foundational Model

Self‑supervised Modelling of Neuroimaging Data: Developing a Basic Foundational Model
Philipp Goebl, Arman Eshaghi — 30 June through July 4th  2025 

Project Overview

Detect synthetic motion artefacts on brain MRIs
 Model output: Good vs Bad (with classification uncertainty) and regression (e.g., age from IXI dataset) 
 Compare a fine‑tuned self‑supervised classifier vs a purely supervised classifier.
Key questions

1. How does self‑supervised modelling improve performance?
2. What are the main advantages of self‑supervised modelling?


Project Roadmap

Day
	Focus
	Key Tasks

Day 1
	Data download & prep
	– Fetch IXI dataset– Define tasks & delegate

Day 2
	Ground‑truth & SSL pre‑training
	– Generate ground‑truth labels– Train self‑supervised model (see MONAI ViT‑UNETR SSL tutorial)

Day 3
	Fine‑tuning & Supervised baseline
	– Fine‑tune SSL model for classification– Train supervised classifier– Compare metrics

Day 4
	Results & Presentation
	– Aggregate results– Build final slides/report



Resources

* IXI dataset: https://brain-development.org/ixi-dataset/
* MONAI SSL tutorial: https://github.com/Project-MONAI/tutorials/tree/main/self_supervised_pretraining/vit_unetr_ssl


Quick Reference: SSL vs Supervised

Aspect
	Self‑supervised
	Supervised

Label requirement
	❌ (unlabelled)
	✅ (labelled)

Feature quality
	Learns rich, general features
	Task‑specific features

Transferability
	High
	Limited

Typical losses
	Contrastive, reconstruction, BYOL
	Cross‑entropy, Dice



Pipeline Diagram

      ┌────────────┐      ┌─────────────────┐      ┌───────────────────────────┐      ┌─────────────────┐
      │  Raw MRIs  │ ──► │ SSL Pre‑training │ ──► │         fine‑tune          │ ──► │ Performance Eval │
      └────────────┘      └─────────────────┘      └───────────────────────────┘      └─────────────────┘




Discussion Prompts

* What are the reasons for choosing SSL over supervised for artefact detection?
* Which SSL loss functions fit volumetric MRI best, and why?

