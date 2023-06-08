# Will I want you to be my date?

## Problem Statement

Dating has existed in various forms throughout history, and people's interest in the study of dating remains consistent despite changes in traditions and dating methods. People meet numerous individuals in their lifetime, but they only interact extensively with a fraction of them. Short interactions with new people can significantly influence potential relationships. Research suggests that first impressions are formed rapidly upon meeting someone, and accurate judgments about their personality traits can be made in interactions as short as four minutes. However, the importance of different traits and interest compatibility in determining whether someone would be interested in dating a new acquaintance is not well understood. Therefore, the objective of this study is to assess the significance of demographic features and people's interests in predicting whether individuals would want to date someone they have just met. The data used in the study comes from speed dating events held at Columbia's Business School between 2002 and 2004. Participants engaged in four-minute interactions with potential romantic partners of the opposite sex and provided feedback on their encounter, including whether they would be interested in going on a date with the person or not. The study aims to utilize demographic information, personal interests, and preferences to predict dating interest based on these factors.

## Data Description and Handling

The final dataset used in the study includes information on 551 participants and 8,368 interactions between pairs of participants. Each row in the dataset represents a distinct participant-partner relationship, considering interactions between participants. Out of the original 195 features, only 43 features were selected for analysis based on their relevance to the research question. These features were categorized into four major groups: demographic information (such as religion, race, and age), interest in various leisure activities (like sports, exercise, dining, museums, art, hiking, and gaming), perceptions of the other person (regarding attractiveness, sincerity, intelligence, fun, ambition, and shared interests), and the importance assigned to these factors when choosing a significant other by each participant. The selection of these features was influenced by previous studies that explored the determinants of liking and dating choices.


## Results

|        Model           | Train Accuracy | Test Accuracy |
|------------------------|----------------|---------------|
|       Baseline         |     0.7918     |    0.7616     |
| Logistic Regression    |     0.7924     |    0.7670     |
|          KNN           |     1.0000     |    0.7742     |
|    Decision Tree       |     0.8536     |    0.7700     |
|    Random Forest       |     1.0000     |    0.7957     |
|          XGB           |     1.0000     |    0.8202     |
|       Stacking         |     1.0000     |    0.8196     |


The evaluation of different models for the given data aims to find a balance between high accuracy, low overfitting, and model simplicity. The logistic regression models (with and without regularization) and the single decision tree demonstrated the highest accuracy and lowest overfitting. Among the logistic regression models, the one with Lasso regularization is preferred due to its simplicity resulting from excluding non-important predictors. The decision between the single decision tree and the regularized logistic regression is slightly more complex. While both models performed similarly, the decision tree exhibited slightly better performance on both the train and test sets. Furthermore, decision trees offer the advantage of being intuitive and easy to interpret. Therefore, considering the accuracy, interpretability, and simplicity of the model, the decision tree is considered the best among all the models tested. However, it is important to note that decision trees can be unstable compared to other models, particularly when working with small datasets, as a small trend in the data can lead to significant changes in the tree structure. Nevertheless, the decision tree performed well and is regarded as the best model among those tested.


## Conclusions

The analysis identifies the most important predictors for the response variable, which include the level of liking towards the other person, the importance placed on attractiveness in a potential partner, and to a lesser extent, factors such as the perceived probability of the other person's interest, shared interests/hobbies, and the fun factor. The report suggests that being a likable person significantly increases one's chances of success in dating. Therefore, individuals who are single are advised to focus on being likable as it offers the best opportunity to improve their chances of going on a date with someone new. However, the concept of likability is subjective and can encompass various qualities, ranging from being outgoing and friendly to being kind and empathetic. Further research is needed to reduce the subjectivity associated with this trait.

Dating can be approached as a blend of science and art, and understanding the factors that contribute to compatibility can reduce uncertainty and help individuals improve their chances of finding a suitable romantic partner. This report contributes to the existing literature by introducing machine learning models and identifying the key features that predict whether someone would be interested in going on a date with a newly met individual. While further research is required, this study provides valuable insights into the prediction of dating interest and adds to our understanding of the subject.