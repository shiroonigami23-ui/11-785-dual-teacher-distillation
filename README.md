# Dual-Teacher Distillation with Wav2Vec2

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
![Last Commit](https://img.shields.io/github/last-commit/shiroonigami23-ui/11-785-dual-teacher-distillation)
![Repo Size](https://img.shields.io/github/repo-size/shiroonigami23-ui/11-785-dual-teacher-distillation)
![Git LFS](https://img.shields.io/badge/Git%20LFS-enabled-blue)

A multi-task speech representation project that distills a single `wav2vec2-base` student from two frozen teachers:
- `ReDimNet` for speaker verification (SV)
- `ASSIST` for deepfake / anti-spoofing detection (DF)

The core training objective is:
- `loss_sv = 1 - cosine(student_sv_proj, teacher_sv_embed)`
- `loss_df = 1 - cosine(student_df_proj, teacher_df_embed)`
- `total_loss = loss_sv + loss_df`

## Why this project
Most production voice-security systems run separate pipelines for speaker verification and spoof detection. This project explores a unified student model to reduce inference overhead while preserving task-specific quality.

## Technical Tags
`speech-processing` `speaker-verification` `deepfake-detection` `knowledge-distillation` `wav2vec2` `pytorch`

## Repository Contents
- `notebooks/dual_teacher_colab_v3.ipynb` - end-to-end training notebook
- `artifacts/metrics/train_meta.json` - run metadata + loss history
- `artifacts/figures/loss_curves.png` - training loss visualization
- `artifacts/models/checkpoint_latest.pt` - latest checkpoint (Git LFS)
- `docs/PSEUDOCODE.md` - implementation pseudocode
- `docs/reports/DualTeacher_MainReport.pdf` - technical report
- `docs/viva/DualTeacher_VivaQA.pdf` - viva preparation material
- `presentations/DualTeacher_Wav2Vec2.pptx` - presentation deck

## Quick Start
1. Open `notebooks/dual_teacher_colab_v3.ipynb` in Colab.
2. Configure dataset paths/tokens as needed.
3. Run distillation + fine-tuning stages.
4. Inspect `artifacts/metrics/train_meta.json` and `artifacts/figures/loss_curves.png`.

## Current Status
- Architecture implemented and trained.
- Distillation objective verified in code.
- Benchmark metrics such as EER/min-DCF can be added as additional evaluation artifacts.

## Team
- Lucky Gurjar
- Aryan Singh Chandel
- Nikhil B
- Tanuja Bhatt

Mentor: Prof. Massa Baali  
Course: 11-785
Team: 45 

## Contribution Guide
If you are a project member, please use your own GitHub account and open pull requests from your own branch so individual contributions are visible on GitHub.

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Citation
If this project helps your work, please cite it using [CITATION.cff](CITATION.cff).

## License
This repository is released under the MIT License. See [LICENSE](LICENSE).
