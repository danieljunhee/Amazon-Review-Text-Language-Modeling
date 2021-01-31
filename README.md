# Amazon-Review-Text-Language-Modeling

In this project, we use the Amazon reivew text data (link: https://nijianmo.github.io/amazon/index.html) - in particular, review texts about electronics products. We will be working with language models to generate texts, and also a text classification model using the same text data in order to check if our language models can generate texts that are similar to the real data that they were trained with.

Our project will consist of the following steps.
- Step 1: For each rating score (i.e. 1, 2, 3, 4, 5), fine-tune a pre-trained GPT2 language model (provided by Hugging Face's "transformers" library).
- Step 2: Once the five separate language models are fine-tuned, we will be able to generate new texts from each of them. That is: we create some texts via the language model for rating score 1, similarly for score 2, 3, 4, and 5.
- Step 3: Train a text classification model using the same, or part of the, text data that we used for step 1. The model will classify a text into one of the five rating scores.
- Step 4. We let the text classification model predict on the generated texts from step 2. So basically, the generated texts are used as the test data for our classifier, where the true class for the generated texts from the rating 1 language model would be 1, the true class for the generated texts from the rating 2 language model would be 2, etc.

Ultimately, we want to see if the model's performance on predicting the generated texts by the GPT2 language models (which are fake data) is reasonably similar to its performance on the evaluation data (which are real data). If yes, it would be reasonable to say that the language models are indeed capable of generating texts that are similar to the real texts that they were trained with. Note that training the text classification model well so that its performance is high is not necessarily a key point here. We're more interested in whether the classifier's predictive performance is similar with the real data and the fake data.

[Dataset Citation]
- Justifying recommendations using distantly-labeled reviews and fined-grained aspects \
Jianmo Ni, Jiacheng Li, Julian McAuley \
Empirical Methods in Natural Language Processing (EMNLP), 2019
