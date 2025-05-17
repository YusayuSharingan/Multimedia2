# Model Performance Summary

This README collates the key evaluation metrics produced in laboratory assignments **Lab 6–8** for three core computer‑vision tasks: **image classification, semantic segmentation, and object detection**. For each model we report baseline results ("before") and scores after architectural or hyper‑parameter enhancements ("after").

## 1. Image Classification

| Model              | Accuracy    | F1‑score    |
| ------------------ | ----------- | ----------- |
| ResNet‑18          | 93.70 %     | 91.76 %     |
| ViT                | 92.82 %     | 83.82 %     |


## 2. Semantic Segmentation

### 2.1 Convolutional Models

| Model                              | Precision | Recall    | mAP\@50   |
| ---------------------------------- |-----------|-----------|-----------|
| U‑Net + ResNet‑18 encoder (before) | 0.748     | 0.757     | 0.703     |
| U‑Net + ResNet‑18 encoder (after)  | 0.848     | 0.848     | 0.848     |
| SimpleUNet (before)                | 0.748     | 0.748     | 0.748     |
| SimpleUNet (after)                 | 0.848     | 0.848     | 0.848     |

### 2.2 Transformer Models

| Model                    | Precision | Recall    | mAP\@50   |
| ------------------------ |-----------|-----------|-----------|
| SegFormer (before)       | 0.748     | 0.757     | 0.703     |
| SegFormer (after)        | 0.848     | 0.848     | 0.848     |
| SimpleSegFormer (before) | 0.748     | 0.757     | 0.703     |
| SimpleSegFormer (after)  | 0.848     | 0.848     | 0.848     |

## 3. Object Detection & Recognition

| Model           | Precision | Recall    | mAP\@50   | mAP\@50‑95 |
| --------------- | --------- | --------- | --------- | ---------- |
| YOLOv11 (before) | 0.678     | 0.657     | 0.703     | 0.529      |
| YOLOv11 (after)  | **0.798** | **0.681** | **0.778** | **0.593**  |

## 4. Главные выводы

Тщательная настройка гиперпараметров и умеренные изменения архитектуры обычно приводят к заметному росту качества моделей. Поэтому важно придерживаться итеративного цикла оптимизации.

При корректной настройке трансформерные модели (ViT) способны сравняться или опередить CNN в задаче классификации, однако результаты могут сильно колебаться.

В задаче семантической сегментации трансформерная SegFormer обеспечила высокую итоговую точность, хотя прирост по mIoU оказался умеренным по сравнению с CNN‑базовыми решениями.

Не каждое «улучшение» действительно повышает качество; важно отслеживать несколько метрик одновременно, чтобы своевременно выявлять возможную деградацию модели.
