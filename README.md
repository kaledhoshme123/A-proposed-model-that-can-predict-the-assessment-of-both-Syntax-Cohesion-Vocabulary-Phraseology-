# A proposed model that can predict the assessment of both Syntax, Cohesion, Vocabulary, Phraseology, Grammar and Conventions:
The proposed model is able to predict the evaluation of both grammatical coherence, vocabulary and grammatical conventions, so that the evaluation can give each of those criteria a value between 1 and 5, I did not treat the system as a classification process, but rather it was treated as a REGRESSION issue. It includes several steps through which a few errors were reached, all ranging between 0.25 for each criterion. The values ​​of the weights that were reached can also be used to deal with the issue as a classification process (but it was not dealt with as well in this proposed methodology).
The proposed model structure:
- The idea of ​​the model is based on taking advantage of the concepts of transfer education, so that we can create a model of a neural network to evaluate three cases (considering that the characteristics that will be extracted at the end of the training, can be used to be applied to the rest of the criteria by which the text is evaluated).
- A hybrid model has been proposed to study and conclude the three criteria through Transformers + ResNet-LSTM.
![download (71)](https://user-images.githubusercontent.com/108609519/188493005-243caf16-4013-4a5f-a8cd-3d4ab3ebdc7d.png)
- At the end of the training and after reaching the value of a small loss, the weights that are in the "concatenate" layer were used with "XGBRegressor" so that part of the dataset was trained and tested on each of the criteria.

## The results were as follows:

- Loss in prediction of Syntax values ​​for test data: 0.2994971788695396
- Loss in Predicting Cohesion Values ​​for Test Data: 0.30764062967270756
- Loss in Predicting Vocabulary Values ​​for Test Data: 0.2201188132420945
- Loss in prediction of Phraseology values ​​for test data: 0.279147987968599
- Loss in prediction of Grammar values ​​for test data: 0.3888626417276952
- Loss in prediction of Conventions values ​​for test data: 0.28148406819585364
