# 🗺 Roadmap — Dual-Teacher Distillation with Wav2Vec2

> Back to the [README](../README.md).

## Where the project stands

Status: **trained**.

## Milestones

### Phase 1 — Distillation (done)

- [x] Dual-head wav2vec2 student
- [x] Cosine distillation from ReDimNet + ASSIST
- [x] Loss tracking, report, viva material and slides

### Phase 2 — Task-level evaluation

*Goal:* Prove the student is useful on the real tasks, not only close in embedding space.

- [ ] Speaker-verification EER and minDCF on VoxCeleb1-O
- [ ] Anti-spoofing EER / t-DCF on ASVspoof 2019 LA and 2021 DF
- [ ] Compare against each teacher alone and a naive two-model pipeline
- [ ] Measure inference latency and parameter savings

### Phase 3 — Method improvements

- [ ] Weighted / uncertainty-based loss balancing between tasks
- [ ] Layer-wise feature distillation (not only final embeddings)
- [ ] Try smaller students (DistilHuBERT, wav2vec2-small) for edge deployment

### Phase 4 — Release

- [ ] Refactor notebook into a `src/` package with a CLI
- [ ] Publish the student on Hugging Face with a Gradio demo
- [ ] Write up as a workshop paper

## 🔭 Long-term Vision

A single, lightweight voice-security encoder that answers both "*is this the right person?*" and "*is this a real
human voice?*" in one forward pass — cheap enough for phones and call-centre edge devices.

## How to help

Pick any unchecked item, open an issue to discuss the approach, then send a PR. Items in the earliest unfinished milestone are the highest priority.


---
*Last updated: 2026-11-13*
