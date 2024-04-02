# azure-language-studio-practice
Practicing with Azure Language Studio - Analyzing sentiment and opinions

## Introduction
In this exercise, we practiced using Azure AI Language Studio, which is a set of tools to integrate Azure AI Language features into user's applications. It provides Natural Language Processing tools that can understand and analyze text. To do it, we followed Microsoft Learn steps avaiable [here](https://aka.ms/ai900-text-analysis).
### Setup Steps
1. With an azure subscription at hand, navigate to portal.azure.com, click "+ New Resource", select "AI + Machine Learning" in the right-hand pannel, look for "Language service" and click "create" bellow it.
Select a valid azure subscription, resource group, and create a unique resource name. Select a princing option (F0 free tier may be avaiable), check the acknowledging box, and click create at the bottom of the page.

2. Navigate to the [Language Studio](https://language.cognitive.azure.com), select the "Classify text" tab and click "Analyze Sentiment and Mine Opinions". Here we have a text box which we can use to input text and try out and test the sentiment analysis feature.

## How it works
The tool reads the text looking for key words and phrases, events and assessments; It classifies them as positive, neutral and negative, with different levels of confidence. This makes the tool very powerful for short text, given they aren't filled with irony; Ambiguous or deflecting sentences can generate confusing output. The longer the input text, the more challenging it will be for the service to give meaningful and confident output; longer texts are usually less straight-forward in its assessments, and are more prone to contain ambiguity, raising the level of complexity, thus making it harder for the NLP service to output precise classification. 

## My test impressions and personal review
 I used 4 different public product reviews from the internet - two long and two short. Both short reviews were easily handled, showing azure's NLU capacity at full. The long reviews offered more of a challenge to the sample model, which would need some tunning to achieve a better result.

### First long sample: "Miss Jerry", 1894 movie by Alexander Black

"Miss Jerry" is the oldest movie featuring a review at imdb.com. It has a single review, made by user [johnny-m](https://www.imdb.com/user/ur0781506/?ref_=tt_urv) on 19 June, 2004. It's called ["The Illusion of Motion"](https://www.imdb.com/review/rw0000021/?ref_=tt_urv).
The review is clearly a positive one; Although not complimenting the movie technique in itself, it finds the value of the movie in being visionary, featuring themes, motives and scenes that would become cliché with time. 
