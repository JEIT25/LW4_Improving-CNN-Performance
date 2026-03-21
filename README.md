# LW4_Improving-CNN-Performance

Google Colab Link: https://colab.research.google.com/drive/1_d80I4jE5sdfBL31kUef8_hZl-N6WGt-?usp=sharing

---
# GUIDE QUESTIONS (Student Explanation & Reflection)

## A. Model Evaluation Analysis

**1. What were the weakest-performing classes based on the confusion matrix?**

The weakest-performing classes were those with the highest number of misclassifications, as seen by the off-diagonal values in the confusion matrix. These classes were frequently confused with others, indicating that the model had difficulty distinguishing their features, possibly due to similarity or insufficient training data

**2. How did Precision, Recall, and F1-score vary across classes?**

Precision, Recall, and F1-score varied across classes. Some classes achieved high precision but lower recall, meaning the model was accurate when predicting them but missed many actual instances. Other classes had higher recall but lower precision, indicating more false positives. The F1-score reflected the balance between these two metrics and highlighted inconsistencies in performance across different classes.

**3. What does a low recall indicate in your model?**

A low recall indicates the model failed to identify many true instances of that class. In practice, this means the model is missing important signals and under-detecting that category.

**4. How does AUC score reflect model performance compared to accuracy?**

Accuracy measures overall correct predictions, while AUC reflects how well the model separates positive vs. negative classes across thresholds. A high AUC but moderate accuracy suggests the model distinguishes classes well but struggles with decision boundaries.

---

## B. Model Improvement

**5. How did data augmentation affect validation accuracy?**

Augmentation improved validation accuracy by increasing data diversity, helping the model generalize better to unseen samples.v

**6. Why is Batch Normalization important in CNNs?**

It stabilized training by normalizing activations, reduced internal covariate shift, and allowed faster convergence with higher learning rates.

**7. What role did Dropout play in improving your model?**

Dropout reduced overfitting by randomly deactivating neurons during training, forcing the network to learn more robust feat

**8. How did Early Stopping prevent overfitting?**

Early Stopping monitored validation loss and halted training before overfitting occurred, ensuring the model captured generalizable patterns.


---

## C. Performance Comparison

**9. What improvements were observed after modifying the model?**

After modifications, validation accuracy increased, loss decreased, and metrics like F1-score became more balanced across classes.

**10. Which enhancement contributed the most to performance improvement? Why?**

Batch Normalization often contributes the most because it stabilizes learning and improves convergence. However, augmentation also plays a big role in boosting generalization.

**11. Did the gap between training and validation accuracy decrease? Explain.**

Yes, the gap decreased. This indicates reduced overfitting, meaning the model’s performance on unseen data became closer to its training performance.

---

## D. Explainability (Grad-CAM Integration)

**12. How did Grad-CAM help in understanding model predictions?** 

Grad-CAM visualizations showed which image regions influenced predictions, helping confirm whether the model was “looking” at meaningful features.

**13. Did the improved model focus on more relevant regions? Provide evidence.**

Yes, the improved model highlighted more relevant regions (e.g., focusing on the object itself rather than background noise). Evidence comes from clearer heatmaps centered on the target object.

**14. Why is explainability important in real-world AI applications?**

Explainability builds trust in AI systems, ensures accountability, and helps identify biases or errors. In real-world applications like healthcare or autonomous driving, knowing why a model made a decision is as critical as the decision itself.

