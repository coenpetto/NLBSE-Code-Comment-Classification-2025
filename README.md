# NLBSE'25 Code Comment Classification

> .ipynb file ran in Google Collab on T4 GPU

> To run locally all dependecies must be installed

## Authors:
- Brendan Sheidt
- Coen Petto
- Jeremiah Geisterfer

## Abstract
Code comment classification interacts with software engineering and related disciplines by enhancing code comprehension and improving maintenance protocols. Despite the effectiveness of conventional transformer-based models, they often require substantial computational overhead and introduce excessive latency, rendering them less attractive for real-time applications. In this paper, we present a lightweight sentence transformer model designed to efficiently classify code comments into meaningful categories across multiple programming languages – Java, Python, and Pharo – without introducing a significant loss in performance. In our approach, we leverage training data augmentation through synonym replacement to address the class imbalance, integrate a custom Focal Loss with label smoothing loss function to enhance model robustness, and employ a method of discovering optimal classification thresholds based on the maximization of the F1 score of each label. Through fine-tuning a compact pre-trained model (prajjwal1/bert-tiny) and using mixed precision inference, we deploy a model that can operate approximately 100 times faster than the given baseline while retaining the ability to produce comparable F1 scores. After experimentation, our results demonstrate that our model can achieve a higher submission score of 0.75 compared to the baseline’s 0.70. This validates the efficacy of prioritizing computational efficiency while maintaining competitive predictive performance. Our findings suggest that a lightweight model will offer a viable solution for practical applications that require both speed and accuracy in code comment classification.
