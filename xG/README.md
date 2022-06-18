# xG
As I previously mentioned xG is the probability that a shot will result in a goal by looking at some characteristics of the position.

## Dataset

I used some shoot dataset which at features such as position of the shot, player, last action, result, shot type, situation, match information, etc. I combined these dataset with a player dataset to obtain the information whether shots are coming from weaker foot or stronger foot. I also dropped some unrelated features. I also simplified some features because they have a lot of categories that is not good for the model.
For each method, used features and their possible values will be present at the beginning of each method.
## TabNet
First, I will use TabNet [1] that is a model achieves SOTA performance on tabular data. Since our data is tabular, I decided to apply TabNet Binary Classifier. I will evaluate the performance of the model with Mean Absolute Percentage Error between model's prediction and given xG in addition to the usual methods. Note that xG values of the dataset are not used during training, they are only used for evaluating like a baseline.
Other details are present in the [a relative link](xG_prediction_with_TabNet).
## References
[1] S. Ö. Arik και T. Pfister, ‘TabNet: Attentive Interpretable Tabular Learning’, CoRR, τ. abs/1908.07442, 2019.
