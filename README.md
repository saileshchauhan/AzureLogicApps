# AzureLogicApps

Task Completed using Azure Logic Apps

1. ## Logic Apps
2. ## Twitter Sentiment Analysis Using Logic App
3. ## RSS Feed E-mail Using Logic App

* ## Logic Apps
  Azure Logic App is a cloud service that helps to schedule, automate, and orchestrate tasks when there is a need to integrate apps, data, systems,     and services across enterprises or organizations
  * #### Triggers
    * Polling Triggers :- 
      * It checks a service’s endpoint at regular intervals.
    * Push Triggers :- 
      * It creates a subscription to an endpoint and provides a call-back URL so the endpoint can notify the trigger when the specified event happens,       or data is available. Push trigger waits for the endpoint’s response to getting fired 
    * Common triggers :-
      * Web Triggers
      * Time Based Triggers
      * Office 365 Event
      * 200+ option for Triggers
  * #### Action
    * HTTP
    * Response
    * Function
    * Workflow


* ## Twitter Sentiment Analysis
  In this, project we are fetching tweets on given #hastag e.g. "#olympic" from twitter. Then, analyzing that using Azure Cognitive service e.g text analytics. Used Text analytics to get sentiment behind the posted tweeted. The sentiment, was categorised as neutral,positive and negative. Then, inserted tweet text, tweet by and tweet sentiment all three together in the google sheet, Azure Blob storage, Azure Cosmos DB container respectively.
  * #### The Triggers and Actions are as Follows:
    * Triggers:-
      When a new tweet is posted
     * Actions:
        * Use Text analytics to get sentiment behind the tweets.
        * Then, use for each condition to insert each tweet into the google sheets.
        * Use parallel action with for each condition to add each tweets into the Blob storage.
        * Use parallel action with for each condition to submit each tweet as document to CosmosDB container.
     * [Video of Implementing Twitter sentiment Analysis Using Logic App Part 1](https://youtu.be/huqh8NpnAcU)
     * [Part 2 where tweets are stored in Blob storage and Cosmos DB](https://youtu.be/S_Ssg_kgVGQ)

* ## RSS Feed
  In this, project we are getting RSS Feed of publishing media house. I have used When a new RSS Feed is generated as trigger. Then next, action I have taken is to send E-mail based on this RSS Feed to required client.
  * #### The Triggers and Actions are as Following:
    * Trigger:-
      When a new RSS Feed is generated.
    * Action:
        * Send an E-mail to provided user name
