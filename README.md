# Celebrity Face Recognition

EfficientNetB0 transfer learning model to classify 17 celebrities.

## Results (v1)
| Metric | Score |
|---|---|
| Top-1 Accuracy | 85% |
| F1 (weighted) | — |

## Dataset
~3,400 images across 17 classes via Kaggle.

## Model Architecture
- Backbone: EfficientNetB0 (ImageNet pretrained)
- Head: GAP → BN → Dropout → Dense(256) → Softmax
- Training: 2-phase (frozen backbone → fine-tune top 30 layers)

## Planned Improvements
- [ ] MTCNN face cropping
- [ ] EfficientNetV2-S backbone
- [ ] ArcFace loss
- [ ] MixUp / CutMix augmentation