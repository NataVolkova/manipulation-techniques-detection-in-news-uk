## Computational Detection and Analysis of Manipulation Techniques in News Channels on Telegram in Ukraine
In this research, we aim to identify specific instances of manipulation techniques such as doubts, black-and-white fallacy, appeal to fear, and loaded language and their granularity in news text from social media. To achieve this, we developed our own manually annotated corpus with 1,877 posts from Telegram news channels in Ukraine, consisting of 3,472 manipulation techniques. Each annotation includes the fragments or spans where a manipulation technique is detected, along with the corresponding technique from a set of 10 identified techniques. We then trained a pre-trained "bert-base-multilingual-uncased" model to recognize these spans and their associated manipulation techniques. Additionally, we syntactically generated text to enhance the model's performance.

In our methodology we followed one proposed by Da San Martino, G., Yu, S., Barrón-Cedeño, A., Petrov, R., & Nakov, P. in "Fine-Grained Analysis of Propaganda in News Article. Conference on Empirical Methods in Natural Language Processing" paper in 2019.

The list of manipulation techniques:

(1)	**Doubts in Ukraine**: questioning the credibility of something or someone in Ukraine.

(1.1)	**Doubts in the Ukrainian Government**. 

(1.2)	**Doubts in the Ukrainian Army**. 

(1.3)	**Doubts in Ukrainian National/Credible Media**. 

(1.4)	**Doubts in Partners’ Help**: question the effectiveness of actions and honesty of partners who help Ukraine. 

(1.5)	**Other Doubts in Ukraine**: other doubts about the existence of Ukraine, the actions of Ukrainians as a people, or the actions of a large group of Ukrainians, refugees abroad, etc. 

(2)	**Black-and-white fallacy**: presenting two alternative options as the only possibilities, when in fact more possibilities exist.

(3)	**Appeal to Fear**: seeking to build support for an idea by instilling anxiety and/or panic in the population towards an alternative, possibly based on preconceived judgments. 

(4)	**Loaded language**: appeals to emotions or stereotypes without any reason.

(4.1) **Appeal to Anger**: causing anger by emphasizing the negative aspects of a situation in order to evoke an emotional reaction. 

(4.2) **Appeal to Hate and Disgust**: causing hate, intense dislike, or disgust by using strong negative emotions, stereotypical phrases, or words that humiliate a person or group of people or a certain idea they support. 

(4.3) **Loaded Language and Appeal to other Emotions**: other emotional appeals and phrases with strong connotations to persuade another by evoking feelings rather than providing arguments and evidence. 

#### Results:
Models with upsampling possess distinct advantages in both tasks. They are adept at handling unstructured data from social network in Ukrainian, which often contain swear words (with letters obscured by symbols), incomplete or illogical sentences, and mistakes. Hovewer, for span identificcation task it predicted much longer spans compared to the truth dataset. The model for technique detection excelled in recognizing the Loaded Language and Other Emotions class, likely due to its predominance in the dataset. However, model tend to confuse this class with other emotion-related classes. The Other Doubts class, being the least represented, was not detected by model. The inclusion of synthetic data improved predictions for most classes, including Black-and-White Fallacy, Doubts in Government, Doubts in Media, and Doubts in Partners' Help, as well as Appeal to Anger and Loaded Language and Other Emotions. A significant area for further research is addressing overlapping spans so the models can accurately predict multiple spans and predict different classes for them.
