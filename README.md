# Abdominal Trauma Detection (RSNA Challenge)

This repository presents a deep learning pipeline for identifying abdominal injuries using contrast-enhanced CT scans. The project was developed for the RSNA 2023 Abdominal Trauma Detection Kaggle competition and focuses on classifying injuries in key organs including the liver, spleen, kidney, and bowel, as well as detecting internal bleeding.

## 🧠 Project Summary

- **Goal**: Automate the classification of abdominal trauma from CT images.
- **Approach**: Multi-label classification using a modified KerasCV RetinaNet with a ResNet50 backbone.
- **Data Format**: CT DICOM volumes transformed into 2D PNG slices for training and inference.
- **Injuries Detected**:
  - Liver (low/high)
  - Kidney (low/high)
  - Spleen (low/high)
  - Bowel injury
  - Extravasation (active bleeding)
  - Any injury (summary label)

## 🔍 Highlights

- Multi-output neural network supporting binary and multi-class classification per organ.
- Custom TensorFlow data pipeline using `tf.data` for efficient loading and augmentation.
- Training included horizontal flips, brightness/contrast changes, cutouts, and resizing (256x256).
- Inference pipeline processes patient DICOMs, aggregates predictions across slices, and formats for competition submission.

## ✅ Validation Accuracy

| Organ         | Accuracy |
|---------------|----------|
| Kidney        | 0.92     |
| Liver         | 0.91     |
| Extravasation | 0.87     |
| Spleen        | ~0.79    |
| Bowel         | 0.52     |

> Results suggest strong generalization for structured injuries; further work needed for bowel and spleen labels.

## 📌 Future Directions

- Incorporating 3D CNNs or slice-aware transformers
- Weakly-supervised localization to aid interpretability
- Uncertainty estimation for clinical decision support
- Domain adaptation and real-world testing

## 📚 Acknowledgment

Developed at Friedrich-Alexander-Universität Erlangen-Nürnberg as part of the MSc. Data Science program. Supervised by Dr.-Ing. Vincent Christlein. Code contributions are available on the [GitHub repository](https://github.com/aafiakhalid5/Abdominal-Trauma-Detection).
