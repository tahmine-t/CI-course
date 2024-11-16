## Multi-Domain Classification - Phase 1

## Overview

This project focuses on multi-domain classification using the **Random Forest** algorithm. The dataset comprises five distinct domains, each containing classes for digits 0 through 9. The project is divided into three main parts, each addressing a unique challenge in multi-domain classification.

<p align="center">
  <img src="int.png" alt="Intro" width="500" />
</p>

---

## Project Structure

1. **Digit Classification**  
   - Directly classify digits from the dataset using a Random Forest model.  
   - Tune hyperparameters to achieve optimal performance.  
   - Evaluate the model using a **confusion matrix**.

   <p align="center">
     <img src="1.png" alt="Digit Classification" width="400" />
   </p>

2. **Domain and Digit Classification**  
   - Train a Random Forest classifier to classify data domains.  
   - Develop separate digit classifiers for each domain.  
   - Evaluate the pipeline by combining domain and digit classification.  
   - Fine-tune hyperparameters and analyze model effectiveness.

   <p align="center">
     <img src="2.png" alt="Domain and Digit Classification" width="700" />
   </p>

3. **Cross-Domain Influence in Digit Classification**  
   - Investigate the effect of using cross-domain data in training.  
   - Plot confusion matrices for domain classifiers and assess their impact on digit classification.  
   - Experiment with blending data from other domains and analyze the results.  
   - Compare improvements or degradations and report findings.

   <p align="center">
     <img src="3.png" alt="Cross-Domain Influence" width="700" />
   </p>

---

## Dataset and Code

The dataset and implemented code can be accessed from the following link:  
[Google Drive - Dataset and Code](https://drive.google.com/drive/folders/1jlbxKJP1Wt0fQE5MrxaTU3pFSlSV_UfJ?usp=sharing)

---

## Key Goals

- Explore the effectiveness of hyperparameter tuning in multi-domain classification.  
- Assess the interaction between domain classification and digit classification.  
- Experiment with cross-domain training to address real-world data challenges.  
- Analyze results using confusion matrices and other metrics.  

---

## Conclusion

This project provides a hands-on approach to tackling complex multi-domain classification problems, enhancing your understanding of Random Forest classifiers and their application in real-world datasets. It also emphasizes the importance of hyperparameter tuning and data blending techniques to improve classification accuracy.
