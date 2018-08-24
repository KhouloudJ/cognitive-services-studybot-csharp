# Study Bot Sample in C#

Samples to create a Study Bot chat client using [QnA Maker](https://docs.microsoft.com/en-us/azure/cognitive-services/qnamaker/index), [LUIS](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/), [Bing Spell Check](https://docs.microsoft.com/en-us/azure/cognitive-services/bing-spell-check/), and Bing News Analytics (coming soon). Each query into the chat bot will be accompanied by relevant search results in an Encyclopedia, Microsoft Academic, and News/Blogs sections as a study aid. Teachers are able to create their own question and answer FAQs to create a study guide as input for the chat bot that follows a preferred curriculum. However, demo FAQs are available for this sample. The focus of this app is to enable a nonbiased experience of studying, where students can study a subject with the most relevant study aids available.

## Features

* **QnA Maker with LUIS**: There are 3 knowledge bases (created from FAQs in [qnamaker.ai](https://www.qnamaker.ai)) that LUIS directs the user to after a query is received in the chat bot. LUIS has utterances created (in [luis.ai](https://www.luis.ai)) that will allow the right knowledge base to be used. For instance, if the user types in "virus", LUIS knows to go to the biology knowledge base to retrieve a definition (answer) to the user's input.

* **Bing Spell Check**: This enables the user to make spelling mistakes for pre-defined words. For instance, from the sociology knowledge base, "Apartheid" can be recognized if the user inputs "apartide", "aparteid", "apartaid", etc.

<!--* **Bing News Analytics**: This service combines [Bing News Search](https://docs.microsoft.com/en-us/azure/cognitive-services/bing-news-search/) and [Text Analytics](https://docs.microsoft.com/en-us/azure/cognitive-services/text-analytics/) Cognitive Services to return relevant results in the News/Blogs section. The user's query will start an internet search with the keyword(s) that returns articles with the negative sentiment filtered out. For example, if the user's query in the chat bot is "sexual reproduction", the news articles about sex crimes or difficult/abusive relationships will be filtered out. 
* **More relevant searches**: The user query will also have the topic of study attached to each search. For instance, typing in "time" to the chat bot returns everything from watches to calendar events in the News/Blogs section. But this sample adds the knowledge base topic, such as "time + geology", to the search, which returns results only relevant to geologic time. If the user types "bacteria", the word "biology" is added to the query, which will filter out irrelevant articles about cleaning products that fight bacteria, and so on.
-->

## Prerequisites

1. Start with the Qna-Luis-Bot sample. Once that is up and running, then build the Study Bot sample. The Study Bot depends on the bot you build in Qna-Luis-Bot. Follow the README files in each sample.

1. Visual Studio 2017+

1. Qna-Luis-Bot is a C# .NET Standard app

1. Study Bot is a C# UWP app
