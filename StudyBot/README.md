# Study Bot v3

This sample currently uses web app bot v3 only. The v4 is coming soon. However, the Qna-Luis-Botv4 is a stand-alone bot that can run independently of the StudyBot UWP app, to demostrate the bot features only.

This sample is a UWP app that combines a LUIS-based web app bot (with Bing Spell Check enabled in luis.ai) with three QnA Maker knowledge bases to provide a question and answer chat client for a student. It also contains a relevant website query based on the chat queries entered by the student, for instance, if the user wants to know the definition of a "virus". The queries will then act as search terms for an encyclopedia, Microsoft Academic, and a Bing Search in their respective `WebView` in the app. 

## Prerequisites

1. You will need the Qna-Luis-Bot sample up and running before running this app. 

1. Follow the prerequisites for the Qna-Luis-Bot [v3](https://github.com/Azure-Samples/cognitive-services-studybot-csharp/blob/master/Qna-Luis-Bot/readme.md) or [v4](https://github.com/Azure-Samples/cognitive-services-studybot-csharp/tree/master/Qna-Luis-Botv4) that will help you create three (or 4) knowledge bases in qnamaker.ai with some accompanied LUIS intents/utterances in luis.ai, and a Basic C# web app bot in the Azure portal. 

1. Once your Qna-Luis-Bot sample is ready, you'll need its bot name and secret key for this sample (detailed below).

1. Open this Study Bot solution file in Visual Studio 2017+.

1. In `MainPage.xaml.cs`, add your Qna-Luis-Bot's bot's name (verbatum) and secret key to `botHandle` and `botSecretkey`, respectively. To find the key, go to your bot in the [Azure portal](https://ms.portal.azure.com) under the Channels menu item, then select `Edit` to the right of your bot. You'll see your secret key (either one is fine) that you can show and copy, then paste into `MainPage.xaml.cs`. 
    
    <img src="/Assets/bot-secret-key.png">

1. Next, enable Direct Line in Azure. While still in the Channels menu, click on the globe icon.

    <img src="/Assets/enable-directline.png">
  
1. The secret keys popup will show again, click "Done" at the bottom. Then you will see Direct Line has been added next to Web Chat.

    <img src="/Assets/directline-done.png">

1. NuGet packages needed: 

    Microsoft.Bot.Connector.DirectLine (if using bot v3)
    
    Microsoft.NETCore.UniversalWindowsPlatform
    
    Microsoft.Rest.ClientRuntime
    
    Newtonsoft.Json
    
## Run and Test the sample

1. Run your StudyBot solution file in Visual Studio.

1. In the UWP interface that appears, enter a query, such as "biology".

1. Enter any of your QnA Maker question terms you created.

1. The definition for these terms gets returned, or if the term does not exist in any of the knowledge bases, it will say "No good match found in Study Bot".

1. The search query also shows the term in the encyclopedia and Microsoft Academic.

1. Experiment by adding or removing your QnA Maker knowledge base question and answers (in qnamaker.ai) and your LUIS intents/utterances (in luis.ai) and try new queries based on these changes.
