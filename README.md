# Azure AI Language Studio practice
Practicing with Azure Language Studio text classification - analyzing sentiment and opinions

## Introduction
In this exercise, we practiced using Azure AI Language Studio, which is a set of tools to integrate Azure AI Language features into user's applications. It provides Natural Language Processing tools that can understand and analyze text. To do it, we followed Microsoft Learn steps avaiable [here](https://aka.ms/ai900-text-analysis). We also collected public product reviews throughtout the internet to use as samples; their text is in [azure-language-studio-practice/input.md](https://github.com/fmossri/azure-language-studio-practice/blob/main/input.md)
### Setup Steps
1. With an azure subscription at hand, navigate to portal.azure.com, click "+ New Resource", select "AI + Machine Learning" in the right-hand pannel, look for "Language service" and click "create" bellow it.
Select a valid azure subscription, resource group, and create a unique resource name. Select a princing option (F0 free tier may be avaiable), check the acknowledging box, and click create at the bottom of the page.

2. Navigate to the [Language Studio](https://language.cognitive.azure.com), select the "Classify text" tab and click "Analyze Sentiment and Mine Opinions". Here we have a text box which we can use to input text and try out and test the sentiment analysis feature.

## How it works
The tool reads the text looking for key words and phrases, events and assessments; it looks for sentiments and opinions. It classifies them as positive, neutral or negative, with different levels of confidence. This makes the tool very powerful for short text, given they aren't filled with irony; ambiguous or deflecting sentences can generate confusing output. The longer the input text, the more challenging it will be for the service to give meaningful and confident output; longer texts are usually less straight-forward in its assessments, and are more likely to contain ambiguity, raising the level of complexity, thus making it harder for the NLP service to output precise classification.

Iphone review by [Jonathan]((https://www.amazon.com/gp/customer-reviews/R1JY8US3MJ4BGL/ref=cm_cr_dp_d_rvw_ttl?ie=UTF8&ASIN=B09LPB9SQH)): sample assessment
![Iphone review sentiment and opinion analysis](https://github.com/fmossri/azure-language-studio-practice/assets/82612595/eb336600-6748-497a-8f33-16788dd7f252)

It both classifies the whole text, and then, thoroughly, phrase by phrase.

Gohan Lapa Restaurant review, by Google reviews user [Henry Edward Hall](https://maps.app.goo.gl/w4U8ag6WT9UQzGoS7):
![Sentences 1 and 2 analysis](https://github.com/fmossri/azure-language-studio-practice/assets/82612595/8b3d1a08-3eb3-40ac-8485-baf28af88ed5)
![Sentence 3 and 4 analysis](https://github.com/fmossri/azure-language-studio-practice/assets/82612595/cc81ec36-a5b1-459d-8e26-d86df5bdc3c3)



## My test impressions and personal review
 I used 4 different public product reviews from the internet - two long and two short. Both short reviews were easily handled, showing azure's NLU capacity at full. The long reviews offered more of a challenge to the sample model, which would need some tunning to achieve a better result.

### First long sample: "Miss Jerry", 1894 movie by Alexander Black

"Miss Jerry" is the oldest movie featuring a review at imdb.com. It has a single review, made by user [johnny-m](https://www.imdb.com/user/ur0781506/?ref_=tt_urv) on 19 June, 2004. It's called ["The Illusion of Motion"](https://www.imdb.com/review/rw0000021/?ref_=tt_urv).
The review is clearly a positive one; Although not complimenting the movie technique in itself, it finds the value of the movie in being visionary, featuring themes, motives and scenes that would become cliché with time. Despite its higher level of complexity, due both to the nature of a movie review itself, the length of the text and the particular style of the author, it's easily perceived as a positive review. The language model correctly classify the whole of the review as positive, albeit just barely; The phrase by phrase classification, on the other hand, is less satisfying:

![Document sentiment analysis](https://github.com/fmossri/azure-language-studio-practice/assets/82612595/dc1fa364-02cf-4604-853d-d4be30853d7c)

The 3 first sentences' classification is acceptable. Although positive, the compliments made to the movie are very subtle.

![Sentences 1, 2 and 3](https://github.com/fmossri/azure-language-studio-practice/assets/82612595/26a0fc7d-7b68-43be-986b-4fac284ec376)

On sentences 4 and 6, it starts to misunderstand some of the sentiment, specially on sentence 6, which is clearly a very positive compliment to the actors' ability.

![Sentences 4 and 6](https://github.com/fmossri/azure-language-studio-practice/assets/82612595/d4df25e2-2c09-4b7a-98c0-76b298b448f1)

On sentence 5 it fails completely. What is a compliment to the director's taste - the lack of dramatisation - is understood as a negative sentence.

![Sentence 5](https://github.com/fmossri/azure-language-studio-practice/assets/82612595/76c26482-ff28-45d7-a8dc-c3e4f7f36701)

The same happens with sentence 7:

![Sentences 7, 8 and 9](https://github.com/fmossri/azure-language-studio-practice/assets/82612595/664685be-400b-4a39-a496-531338c1c819)

### Second long sample: "Project Zomboid", game by [The Indie Stone](https://projectzomboid.com/blog/about-us/)

Project Zomboid is a zombie survival craft game developed by The Indie Stone. It is a popular game on [Steam](https://store.steampowered.com/) that lives on a "Losing is fun" kind of philosophy; it's player base is very fond of irony and sarcasm. Here is a randomly picked review from steam, by user [『Lazy Loser』](https://steamcommunity.com/profiles/76561198126766799/recommended/108600/). It's a higly positive review, despite it's sarcastic and ironic language. The model fails completely to understand it, missing the irony by far:

![image](https://github.com/fmossri/azure-language-studio-practice/assets/82612595/de5535d9-546a-41c5-a9ab-f22220916d52)
![image](https://github.com/fmossri/azure-language-studio-practice/assets/82612595/7f206f06-00d3-4c5a-9bf1-ec5fbf31a19e)
![image](https://github.com/fmossri/azure-language-studio-practice/assets/82612595/e55385bb-ae1c-4aed-a332-21cdbbb6249f)

## Conclusion

For the right use cases, fine tunning for one's specific needs may turn it into a valuable tool to assessing customers' sentiment and opinion; Human supervision is, of course, still needed. For some use cases, the use of a generically trained NLP model could be troublesome.


