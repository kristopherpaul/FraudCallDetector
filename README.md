Synopsis
========
Mobile phone scams or fraud calls have become a major issue in many countries. Current solutions employed for the detection of fraudulent mobile phone calls are simply whitelisting and blacklisting numbers. This has not shown any significant improvement in the detection of fraud in various countries. This is primarily because number spoofing is used through VoIP (Voice Over IP) in most fraudulent calls. This problem can be resolved to a great extent by alerting the user in real-time while the fraudulent call is happening. This can be effectively achieved by using the latest techniques of Deep Learning with NLP (Natural Language Processing). The results show that such fraudulent calls can be detected with an accuracy rate of 90%. This solution can be implemented via an Android/IOS mobile app to alert the user in real-time of fraudulent calls.

Introduction and objectives
===========================
Mobile phone scams have become a major issue in many countries. In the US, one in ten adults falls victim to a scam or fraud every year. Scammers try to steal your money by making false promises in a very convincing way. These phone calls come from real people or as system automated calls. The usual modus operandi of these scammers are as follows: they either offer opportunities to invest your money, receive free product trials, free grants, free student loans, lotteries, or intimidation to file lawsuits or jail threats with regards to loan debts and taxes. The main objective of this project is to detect mobile phone frauds, providing real-time detection of fraudulent calls by analyzing the content of a call. In this project, the Transformer Model technique, the latest advancement in Deep Learning with Natural Language Processing is used to create a model that can identify fraudulent calls and non-fraudulent ones with a really high accuracy rate of 90%.

Innovation
==========
Current solutions employed for the detection of fraudulent mobile phone calls are by simply whitelisting and blacklisting numbers, other solutions are there which include a trained model for predicting fraud using information such as caller's mobile phone number, duration of call, country of call it originated from etc.
But all these methods have not shown any significant improvement in detection of fraud in various countries. This is primarily because number spoofing is used through VoIP (Voice Over IP) in most of the fraudulent calls. Lack of fraudulent conversational sample data has limited the use of Machine Learning in this area. To overcome this lack of data problem, data about the latest frauds either could be collected from government's cybercrime databases or from people's complaints on social media platforms like twitter, facebook etc. For this project: Completed - (1) Constructed a dataset of fraudulent calls and complaints from scraping twitter messages. (2) Using that dataset, a Transformer based Model is trained to identify fraudulent calls. (3) Real Time analysis of call content is done using the above Model to alert the call receiver of potential mobile phone fraud. Work in progress - (1) Mobile App is being made to implement the above real time analysis to alert the call receiver of potential mobile phone fraud. (2) The Transformer based Model will be continuously updated using newer twitter messages as well as confirmed fraud calls from the app users. This will improve the accuracy rate to identify fraudulent calls.
The current test results show that such frauds can be detected effectively and could help a large community of mobile phone users.

Algorithm
=========
Automated collection of complaints of mobile phone frauds from social media like Twitter is done and various NLP (Natural Language Processing) techniques are employed to extract the relevant information from the complaints.
Another public dataset (Part 1 of Santa Barbara Corpus - A collection of call recordings and transcripts of various everyday conversations) is also obtained.
Using twitter complaints for the fraudulent data and Santa Barbara Corpus Data for the non fraudulent data, a dataset is created on which the model will be later trained. This is done so that the model better develops the ability to differentiate between fraudulent and non fraudulent calls.
The Transformer is a deep learning Model introduced in 2017, using the concept of Attention, this Model has given state of the art results in NLP. Companies like Google, Facebook, OpenAI have all come with their own Transformer Models. OpenAI's latest Transformer Model GPT-2 was found to be so powerful, that they didn't release it due to fear of it being misused. In this project, XLNet Transformer Model was trained on the Training set and the Hyperparameters were fine tuned to get the best performance on the cross validation set.

Method
======
Complaints of mobile phone fraud are collected from social media platforms like Twitter and various NLP (Natural Language Processing) techniques are used to extract the relevant information from the complaints. Samples from Santa Barbara Corpus are also taken, this corpus contains mobile phone conversations between speakers on various everyday topics. With this, a dataset of 400 samples is created which contains fraudulent as well as non-fraudulent mobile phone conversations.
This Dataset was split in a 80:20 ratio into training and cross validation sets. For the final test set, random real life call recordings of mobile phone frauds were collected from different websites on the internet. Also, equal amounts of call recordings from the Santa Barbara Corpus were taken to complete the test set.
The XLNet Transformer Model was trained on the Training set and was tested at each epoch on the cross validation set. At the end of the Model training phase, it had achieved a training accuracy rate of 98% and a cross validation accuracy rate of 93%.
The call recordings of the final test set is converted from speech to text using IBM Watson's Speech To Text with speaker diarization so that the speech of different speakers are separated. This proved to be better than converting the whole conversation into a single block of text. The Transformer Model then predicts the type of each call recording of the final test set. This approach gave an accuracy rate of 90% on the final test set.
Some sentences by one speaker could have been interrupted by the other speaker and the meaning of the sentence would be lost if the whole conversation was converted into a single block of text.

Results and Conclusions
=======================
The final model achieved an accuracy rate of 98% on the training set, 93% on the cross validation set and 90% on the final test set. This result is significantly better when compared to the existing solutions for this problem. This solution can be implemented via a mobile app to alert the user in realtime of fraudulent calls.

Acknowledgement and reference links
===================================
I would like to acknowledge my parents for being highly supportive of this endeavor and for their general guidance. Link of the model developed in this project is given below.

Link of Google Colab Notebook of this project 
---------------------------------------------
https://colab.research.google.com/drive/15sN_f8XeEjNM6tbkZfhorfRtn7Z9fewl?usp=sharing

Reference Links
---------------
1. https://www.kaggle.com/rtatman/santa-barbara-corpus-of-spoken-american-english
2. https://www.ibm.com/in-en/cloud/watson-speech-to-text
3. https://huggingface.co/transformers/model_doc/xlnet.html
4. https://towardsdatascience.com/text-normalization-7ecc8e084e31
5. https://en.wikipedia.org/wiki/Transformer_(machine_learning_model)
