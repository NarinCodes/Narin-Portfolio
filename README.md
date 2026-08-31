# [Project 1 - Text-to-SQL CLI Agent](https://github.com/NarinCodes/Text_to_SQL)
An interactive terminal agent that answers natural-language questions about any SQLite database — it writes the SQL, executes it, and prints the rows, with follow-up questions resolving against the conversation so far. Inference runs on an open-weight model served by Fireworks AI rather than a frontier proprietary one, and the agent scores 9/10 on its evaluation set at 1.15s median latency, against 1/10 for a naive "Convert this question to SQL" prompt on the same model. Three design choices drive that gap. Schema grounding introspects the live database and injects the tables, column types, and foreign-key edges into every prompt, so the model cannot invent names or guess at joins. Execution-guided self-repair runs the generated SQL immediately and feeds SQLite's own error text back for a bounded retry, which makes execution the validator rather than parsing. A two-layer guardrail declines questions the schema cannot answer, so the model's general knowledge is never laundered into something that renders like a real query result. The evaluation harness grades by result match — executing the generated SQL and comparing the returned rows to the gold answer — rather than by SQL string similarity, since many different queries answer the same question correctly. The README documents the cost analysis behind the open-weight choice, the ablations behind each prompt rule, and the failure modes the system still cannot catch.

![](/images/text-to-sql.png)

&nbsp;

&nbsp;

# [Project 2 - Generative AI Infinite Shakespeare using Transformers](https://github.com/NarinCodes/NanoGPT)
A generative AI project that leverages Transformer-architecture to build and train a Language Model. The model is trained on all the combined works of William Shakespeare. Running the main Python script will kick-off a generative process that produces infinite Shakespeare — in other words, it is capable of producing a stream of text that closely resembles the scripts of Shakespeare's plays. Under the hood, this project uses PyTorch to construct blocks comprising of MultiHead-Attention and FeedForward layers. In addition, the code also implements new ideas from the highly influential "Attention is all you need" paper — such as Skip Connections, Layer Normalization, and use of Triangular Matrices to calculate token-level affinities.

![](/images/AI_Shakespeare.jpeg)

&nbsp;

&nbsp;

# [Project 3 - Celebrity Faces (Neural Style Transfer)](https://github.com/NarinCodes/Celeb-Faces_Neural-Style-Transfer)
This project consists of two separate tasks—Binary Classification and Neural Style Transfer. Both tasks require the use of the CelebFaces Attributes (CelebA) dataset. For classification, the objective is to leverage deep learning to accurately determine whether a facial image is of a smiling individual or not. Two separate modeling techniques are explored—Custom CNN and Transfer Learning. The model architectures and performance metrics of both techniques are also analyzed. For the second task, a facial image of Turkish actor Kenan Imirzalıoğlu is combined with Joe Reimer’s Waiting on Forever landscape painting through Neural Style Transfer. The content image of the Turkish actor belongs to the CelebA dataset. A different output image is generated via each of the two modeling techniques—direct use of VGG16 and VGG19 with transfer learning.

![](/images/Vs75m.jpeg)

&nbsp;

&nbsp;

# [Project 4 - Insider Trading Predictor](https://github.com/NarinCodes/Insider_Trading_Predictor)
The aim of the project is to predict the probability of short-term increase in a company's stock price after a U.S. Congress official has invested. The final goal is to build a model which can accurately determine whether an investment made by a U.S. lawmaker will lead to immediate increase in the company's stock price. Results from this model can benefit retail investors while picking their own stocks, as well as watchdog groups to explore possible cases of insider trading.

![](/images/download.jpeg)

&nbsp;

&nbsp;

# [Project 5 - Predicting Fetal Health with FHR](https://github.com/NarinCodes/Predicting-Fetal-Health-with-FHR)
For long, the United States has witnessed skyrocketing maternal mortality and an increase in the rate of unnecessary Cesarean sections. Such unfortunate phenomena arguably originate from lack of consistent and objective interpretation of the pre-delivery CTG data. Therefore, to better facilitate the decision-making process of the clinicians, this project aims to construct an effective supervised learning model that classifies potentially pathological fetuses. Through analyses of the 22 variables extracted from the CTG fetal heart rate data, several variables stand out as key indicators for fetuses at danger. The top three are the abnormal short-term variability, percentage of time with abnormal long-term variability, and mean value of short-term variability. The optimal model is a Random Forest model that yields an overall accuracy of 0.9443 and Pathological class F1-score of 0.9122. With consistent and precise fetal heart rate tracking in the third trimester of pregnancy and accurate CTG processing, real-time classifications made with this model could support clinicians in determining fetal risk and subsequent need for Cesarean sections.

![](/images/fetal-heart-rate-2.jpeg)

&nbsp;

&nbsp;


# [Project 6 - Soccer Player Comparison Tool](https://github.com/NarinCodes/Player_Comparison)
This tool allows users to compare the stats of different soccer players. The code has been written entirely in Python, and uses the Beautiful Soup package to srape data from a soccer website. After the collection of relevant stats, extensive data processing is done using pandas and numpy before creating a dashboard using the Matplotlib package. The dashboard contains a scatterplot of Goals per Match vs. Expected Goals per Match, and a soccer field visualization depicting all the shots taken by the players. The soccer field visualization provides information about where the shots were taken, the quality of the chances, and their respective outcomes (i.e. goal or no goal).

![](/images/soccer.png)

&nbsp;

&nbsp;
