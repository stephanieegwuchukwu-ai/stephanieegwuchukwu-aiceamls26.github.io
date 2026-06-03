---
layout: project
title: About My Project
permalink: /about-my-project.html

subtitle: A Multi-Run Analysis of Deep Learning Models
project_title: "Predictive Stability vs. Fairness Instability in Clinical ECG Classification"

problem: |
  AI tools are increasingly being used in hospitals and clinics to help doctors diagnose heart conditions from ECG (electrocardiogram) recordings. But there's a growing concern: these AI systems don't always work equally well for everyone. They can quietly perform worse for certain groups of patients, like older women or men in a specific age range, even when their overall accuracy looks fine on paper. This means some patients may be more likely to receive a missed or incorrect diagnosis simply because of who they are.
 What makes this problem even trickier is that we don't fully understand how consistent these fairness issues are. A model might seem fair one time you train it, and unfair the next, even when trained on the same data. This gap in our understanding is dangerous: if fairness is unstable, then testing a model once and calling it "fair" isn't good enough.
 This project tackles that gap directly. We're asking: even if an AI's accuracy stays steady across repeated training runs, does its fairness stay steady too? If the answer is no, and we suspect it often isn't, then the field needs better tools and standards for evaluating and building trustworthy medical AI.

approach: |
  - Step 1 — Load and preprocess the PTB-XL dataset, a publicly available collection of nearly 22,000 real ECG recordings from PhysioNet, and organize patient data by age group and sex for subgroup analysis.
  - Step 2 — Build and train two deep learning models for heart condition classification: a 1D Convolutional Neural Network (CNN) and a hybrid CNN-Transformer model, using PyTorch in Google Colab.
  - Step 3 — Run each model multiple times (multi-run analysis) and measure both accuracy (AUROC, F1-score) and fairness (False Negative Rate gaps, Equalized Odds) across demographic subgroups, computing confidence intervals to see how stable each metric is.
  - Step 4 — Apply bias mitigation techniques; sample reweighting and class-balanced loss, and measure whether they improve fairness without sacrificing accuracy.
  - Step 5 — Use Grad-CAM (a visual explanation tool) to show which parts of an ECG signal the model is actually paying attention to, and present all findings in a final research report and symposium presentation.

outcome: |
  By the end of the program, we expect to produce a complete research pipeline including trained models, fairness evaluation results across demographic subgroups, and statistical analysis showing how both performance and fairness vary across runs. The deliverables will include research-quality visualizations (learning curves, fairness metric tables, Grad-CAM heatmaps), a structured written research report, and a presentation at the SAIRI Research Symposium in late July.
We hope others, that is, including researchers, clinicians, and future students, can use this work to better understand the risks of declaring an AI system "fair" based on a single evaluation. The code and analysis pipeline will be documented clearly enough that it can be extended to other medical datasets and classification tasks beyond ECG.

final_report_url: https://example.com/your-report.pdf

grad_mentor:
  name: Sudip Sharma
  linkedin: https://www.linkedin.com/in/nxxis?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app

faculty_mentor:
  name: Dr. Blessing Ojeme
  linkedin: https://www.linkedin.com/in/blessing-ojeme-phd-259a7342?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app
---
