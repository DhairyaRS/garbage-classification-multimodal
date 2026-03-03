GARBAGE CLASSIFICATION MODEL - EXECUTION RESULTS & METRICS
=====================================================================
Note: Due to GitHub's file size limits and rendering timeouts for 
heavy Jupyter Notebook outputs, this document summarizes the final 
execution metrics and test results of the model. 

1. MODEL ARCHITECTURE
---------------------------------------------------------------------
- Visual Branch: EfficientNet-B0 (Pretrained on ImageNet)
- Text Branch: BERT-base-uncased (Pretrained on Wikipedia/BooksCorpus)
- Fusion Head: Concatenated 2048 features -> 512 -> 256 -> 128 -> 4 classes

2. TEST SET EVALUATION
---------------------------------------------------------------------
- Overall Test Accuracy: 90.26%

Per-Class Accuracy:
- Black (General Waste): 128/154 (83.1%)
- Blue (Recyclable):     141/154 (91.6%)
- Green (Organic):       146/154 (94.8%)
- TTR (Depot):           141/154 (91.6%)

3. CLASSIFICATION REPORT
---------------------------------------------------------------------
              precision    recall  f1-score   support

       Black       0.91      0.83      0.87       154
        Blue       0.86      0.92      0.89       154
       Green       0.94      0.95      0.94       154
         TTR       0.90      0.92      0.91       154

    accuracy                           0.90       616
   macro avg       0.90      0.90      0.90       616
weighted avg       0.90      0.90      0.90       616

4. VISUAL OUTPUTS & ARTIFACTS
---------------------------------------------------------------------
The code successfully generated the following artifacts, which are 
omitted from the repository due to storage constraints but are 
available in the Google Drive / PDF backup:
* [Training Curves](https://github.com/DhairyaRS/garbage-classification-multimodal/blob/c7a926cb036e77f24e4aa1854f13cd95e9fd8433/result_images/training_curves.png)
* [Confusion Matrix](https://github.com/DhairyaRS/garbage-classification-multimodal/blob/d9bacb0ac6af843e5825220eaee53131abcd7d1c/result_images/confusion_matrix.png)
* [Misclassified Examples](https://github.com/DhairyaRS/garbage-classification-multimodal/blob/c6d4bf0eb36263f6240a7fcedc77256f037ddcb9/result_images/misclassified.png)
* [Balanced Final Model (.pth)](https://drive.google.com/file/d/1JK058-trsn7zb7HP-TRexPMCNV4eYyaA/view?usp=drive_link)
#  Detailed Execution Results

Note: To ensure the 800MB model and heavy visual outputs do not cause rendering issues, visualizations are hosted in the `/results_images` folder.

##  Performance Metrics
* Final Test Accuracy: 90.26%
* Validation Accuracy: 90.58%

##  Visual Evidence
As required by the assignment rubric, the following figures document the model's performance and experimental setup:

1. [Confusion Matrix](./results_images/confusion_matrix.png): Shows per-class precision and recall.
2. [Training Curves](./results_images/training_curves.png): Demonstrates the effect of Dropout and BatchNorm on loss/accuracy.
3. [Incorrect Classifications](./results_images/misclassified.png): Visual analysis of samples the model struggled with.

##  Classification Report

 Name       precision    recall  f1-score   support

  Black     0.91      0.83      0.87       154        [Black Result Image](./result_images/black_result.jpeg)
  
  Blue      0.86      0.92      0.89       154        [Blue Result Image](./result_images/blue_result.jpeg)
  
  Green     0.94      0.95      0.94       154        [Green Result Image](./result_images/green_result.jpeg)
  
  TTR       0.90      0.92      0.91       154        [TTR (Other) Result Image](./result_images/other_result.jpeg)
