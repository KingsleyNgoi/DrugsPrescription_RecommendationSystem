# <b>Drug Prescription Sentiment Analysis</b>
## <b>1. | Introduction</b> 👋
  * Dataset Problems 🤔 </br>
    * 👉 The <mark><b>Drug Review Dataset is taken from the UCI Machine Learning Repository</b></mark>. This Dataset <mark><b>provides patient reviews on specific drugs along with related conditions and a 10-star patient rating reflecting the overall patient satisfaction</b></mark>. The data was obtained by crawling online pharmaceutical review sites.
    * 👉 The <mark><b>Drug Review Data Set is of shape (161297, 7)</b></mark> i.e. It has <mark><b>161297 Data Points or entries</b></mark> and <mark><b>7 features including the review</b></mark>. </br>
    * 👉 The <mark><b>goal of the problem</mark></b> is to <mark><b>recommend top 5 useful drugs per each different medical conditions</b></mark> based on <b><mark>reviews and calculated usefulness from rating * usefulCount * eff_score(normalized average rating)</b></mark>.
    * 👉 Let's treat this a  <mark><b>multi-class classification problem</b></mark>.
    * 👉 Choose <mark><b>the best machine Learning Models / Deep Learning Models with highest Accuracy Score and F1 Score</mark></b> to <mark><b>recommend the top 5 most useful drugs for each different Medical Conditions</b></mark>.
  * <b>Dataset Description</b> 🧾 </br>
  👉 There are <mark><b>7 variables</b></mark> in this dataset:
    * <mark><b>FEATURES</b></mark>
    <ol start="1">
      <li> <b>uniqueID |</b> An identifier for each post.</b></li>
      <li> <b>drugName |</b> The name of the drug for which review is made.</b></li>
      <li> <b>review |</b> The review made by patients for a particular medicine.</b></li>
      <li> <b>rating |</b> Ratings, given by the patients to each medicine on a scale of 10 where 10 represents the maximum efficacy.</b></li>
      <li> <b>date |</b> Date of review entry.</b></li>
      <li> <b>usefulCount |</b> The number of users who found the review useful.</b></li>
      <li> <b>condition |</b> The name of the medical condition for which the medicine is used.</br></li>
    </ol>
  * Machine Learning Modules 👨‍💻 </br>
  👉 The <b>models</b> used in this notebook:
    <ol start="1">
        <li> <b>Linear Support Vector Machine (LinearSVC)</b>,</li>
        <li> <b>Multinomiaa Naive Bayesian (MNB)</b>,</li>
        <li> <b>Light Gradient Boosting Machine (LGBM)</b>,</li>
        <li> <b>Passive Aggressive Classifier</b>,</li>
    </ol>
  * Outcome ✅</br>
    - 👉 <mark><b>Recommend the top 5 most useful drugs for each different Medical Conditions</b></mark> by <b><mark>calculated usefulness through python @interact</b></mark>.
    - 👉 <mark><b>Recommend the top 5 most useful drugs for each different Medical Conditions</b></mark> by <b><mark>the best Machine Learning models or Deep Learning models</b></mark>.
</div>

## <b>2. | File Descriptions</b> 👓
- `drugsComTrain_raw.csv`: the train dataset file.
- `drugsComTest_raw.csv`: the test dataset file.</br>

## <b>3. | Accuracy of Best Model</b> 🧪
Passive Aggressive Classifier
- Accuracy achieved: 93.91%

## <b>4. | Conclusiion </b> 📤
- In this study respectively,
- We have tried to predict a multi-class classification problem in Drug Dataset by a variety of models to to recommend top 5 drugs for each different medical conditions based on revews given.
- We have made the detailed exploratory analysis (EDA).
	> there is missing values on the 'condition' column and drops rows containing missin values. 
- Check the top 10 Common Medical Conditions
	> "Birth Control", "Depression", "Pain", "Anxiety", "Acne", 
	  "Bipolar Disorder", "Insomnia", "Weight Loss", "Obesity" and "ADHD".
- Check the top 10 Common Drug Names Used
	> "Levonorgestrel", "Etonorgestrel", "Ethinnyl Estradiol / Norethindrone", 
	  "Nexplanon", "Ethinnyl Estradiol / Norgestimate", "Ethinnyl Estradiol / Levonorgestrel", 
	  "Phentermine", "Sertraline, "Escitalopram" and "Mirena".
- Check the top 10 Most Drugs Available per Condition, 
	> "Pain", "Birth Control", "High Blood Pressure, "Acne", 
	  "Depression", "Rheumathoid Arthritis", "Diabetes Type 2", "Allergic Rhinitis", 
	  "Osthoarthritis" and "Bipolar Disorder".
- Check Most Drug Available to be Used for Many Conditions
	> "Prednisone", "Gabapentin", "Ciprofloxacin", "Doxycycline", 
	  "Amytriptyline", "Metronidazole", "Venlafaxine", "Neurontin", 
	  "Dexamethasone" and "Lyrica".
- The review length has no clear effect on drugs ratings.
- Perform data cleaning, wrangling and feature engineering with
	- Remove all the hyperlink, html tags, punctuation, Numbers, Symbols, Special Characters,
	  space, accented characters an stop words
	- Decontract text
	- Tokenize using NLTK's word_tokenize
	- Make all texts to lowercase
	- Lemmatization
	- Text string formation)
	- Clean Medical Conditions Columns Containing Redundant Information
	- Remove Any Person Name, Location Name, Organization Name, Date & Time, Money, etc by NER
	- Remove DataFrame Rows where The Medical Conditions has Only 1 Drug
- The suitable NGrams for building machine learning model is 2-grams and 4-ngrams.
- The positive reviews are 70% of the data. This is imbalanced data.
- The best model is Paassive Aggressive Classifier with 92.75% accuracy.
- Provided 2 ways of analyzing 3/5 most useful drugs per medical conditions
	> through calculated effectiveness and usefulness of Drugs displayed using pyhton @interface magic function.
	> through machine learning drugs recommendation system.
	(The extracted keywords from reviews, bring meaningful context to each medical condition 
	 showwn by most informative features reviews fro each different classes.)
		-> Top 5 drugs recommended based on each conitions.

## <b>5. | Reference</b> 🔗
<ul><b><u>Kaggle Notebook 📚</u></b>
        <li><a style="color: #3D5A80" href="https://www.kaggle.com/code/abdelrhmanragab/prescription-drugs-using-consumer-reviews/notebook">Prescription Drugs using Consumer Reviews by ABDELRHMAN RAGAB</a></li>
        <li><a style="color: #3D5A80" href="https://www.kaggle.com/code/chocozzz/recommendation-medicines-by-using-a-review">Recommendation Medicines by using a review by CHOCP, EUNJOO MIN, JUYEON PARK, JY LEE & SUMIN</a></li>
        <li><a style="color: #3D5A80" href="https://www.kaggle.com/code/aashita/word-clouds-of-various-shapes/notebook">Word clouds of various shapes by AASHITA KESARWANI</a></li>
</ul>

<ul><b><u>Github Notebook 📚</u></b>
        <li><a style="color: #3D5A80" href="https://github.com/sharmaroshan/Drugs-Recommendation-using-Reviews/blob/master/DrugsAnalysis.ipynb">Drugs-Recommendation-using-Reviews
 by SHARMAROSHAN</a></li>
</ul>

<ul><b><u>Online Articles 🌏</u></b>
	<li><a style="color: #3D5A80" href="https://medium.com/@marshettyruthvik/drug-recommendation-system-1b32d1cda680#id_token=eyJhbGciOiJSUzI1NiIsImtpZCI6IjQ1NmI1MmM4MWUzNmZlYWQyNTkyMzFhNjk0N2UwNDBlMDNlYTEyNjIiLCJ0eXAiOiJKV1QifQ.eyJpc3MiOiJodHRwczovL2FjY291bnRzLmdvb2dsZS5jb20iLCJhenAiOiIyMTYyOTYwMzU4MzQtazFrNnFlMDYwczJ0cDJhMmphbTRsamRjbXMwMHN0dGcuYXBwcy5nb29nbGV1c2VyY29udGVudC5jb20iLCJhdWQiOiIyMTYyOTYwMzU4MzQtazFrNnFlMDYwczJ0cDJhMmphbTRsamRjbXMwMHN0dGcuYXBwcy5nb29nbGV1c2VyY29udGVudC5jb20iLCJzdWIiOiIxMTcwMTU1NTYzNTUxMTI2NTY4OTciLCJlbWFpbCI6ImtpbmdzbGV5bmtrQGdtYWlsLmNvbSIsImVtYWlsX3ZlcmlmaWVkIjp0cnVlLCJuYmYiOjE3MDQwOTgxNTksIm5hbWUiOiJLaW5nc2xleSBOZ29pIEtvayBLaGVuZyIsInBpY3R1cmUiOiJodHRwczovL2xoMy5nb29nbGV1c2VyY29udGVudC5jb20vYS9BQ2c4b2NLX2JmM3ZlUm5oc1lsczVoRHNMbWZWT2NEeC1oUE1rRUNFbUgxRnNITTc4RlU9czk2LWMiLCJnaXZlbl9uYW1lIjoiS2luZ3NsZXkgTmdvaSIsImZhbWlseV9uYW1lIjoiS29rIEtoZW5nIiwibG9jYWxlIjoiZW4tR0IiLCJpYXQiOjE3MDQwOTg0NTksImV4cCI6MTcwNDEwMjA1OSwianRpIjoiNTQzMmY1MWMzOTFiZjFkNTIxNjVlYjAxZDA1YmJkNmQxNTBiNTlkMCJ9.QF-adrOKm1QGNDDGAu-h_9gd9U1d5VvOKCljPXIPiWSfPto6nhleXckRlcAdx63s8hPXUOnStqRk6wXRDWeH0rUwP4ioO8xRH-rgIGzMby4U-gXNnr0R6V3y-WEp46FyJ6Xb91fr-sjOHtAJRCNd8Iy6d_RHbv0hTfbsUzqFf2Jj5_t1qNzdi12jzPM_h9acx1SQ2MSHMMbmarUtmkZBMJSG5-DoYTd2zE9zNFcJoiTLIJrckR9-98dvs83dGAS1kqsxTHMMkOAgD58JejPi26aU4iLq28zaz0Uu6agkowZzoXHua5XpeQWceznkTUXLceY85zyMGkmtNLQTbrd4sw">Drug Recommendation System by RUTHVIK MARSHETTY</a></li>
        <li><a style="color: #3D5A80" href="https://towardsdatascience.com/predict-patients-medical-condition-based-on-medicine-review-part-1-c22ea39d9976">Predict Patient’s Medical Condition based on Medicine Review — Part 1 by Hamiz Ahmed</a></li>
        <li><a style="color: #3D5A80" href="https://medium.com/@dudsdu/an-example-of-word-cloud-with-mask-4cbbd699fb14">An Example of Word Cloud with Mask by Eduardo Andrade</a></li>
        <li><a style="color: #3D5A80" href="https://minimaxir.com/2016/05/wordclouds/">Creating Stylish, High-Quality Word Clouds Using Python and Font Awesome Icons by Max Woolf</a></li>   
</ul>

<ul><b><u>Online Learning Channel 🌏</u></b>
        <li><a style="color: #3D5A80" href="https://www.udemy.com/course/artificial-intelligence-in-python-/learn/lecture/">Master Artificial Intelligence 2022 : Build 6 AI Projects by Dataisgood Academy</a></li>   
</ul>