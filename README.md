# llSPS-INT-66-AI-Powered-News-Search-App-Level-1-
AI Powered News Search App (Level-1)


# Introduction


## 1. Overview

The web is home to massive amounts of data, with more being created every day. Organizations can harness this constant stream of information to gain understanding, plan strategies, and find opportunities. Enriched news data can help your application make dynamic connections across current events faster.


## 2 .Purpose

The purpose of this project is to develop a web application that meets our need to find the most relevant and recent new articles worldwide and update them regularly.

Since the discovery service is integrated with Slack, it gives a bot to search news with a keyword.
In addition, the web application also analyzes the sentiment present in this news article and extracts key words and concepts to make it easier for the user to decipher what is important and what is not.


## 3. Literature Survey
 
Existing Problem
All current news applications can be confusing for the average person, with multiple functions and exaggerated design, these applications still do not meet the demand of the latest news users and often get results from the past days, weeks and months, which confuses the user only.
Also, there is no way in these apps to know what the approximate feeling of the audience is regarding the article or news topic, which makes it less interactive and easy to use.
 
## 4. Proposed Solution
 Discovery service available in the IBM cloud, creating a web app to get the latest news results is fast and hassle-free. When integrated with Red Node Flow, the IBM Discovery Service can create a simple, engaging, organized user interface that provides users with relevant news articles as Discovery Service continuously crawls the web for the latest news to provide.
By adding emotional analysis, we make the user interface more interactive and easier to understand.



















# Setting up the development Environtment 

## 1. Installing Git 

Install Git on Windows. The most official build is available for download on the Git website. Just go to https://git-scm.com/download/win and the download will start automatically. Note that this is a project called Git for Windows, which is separate from Git itself.

## 2. Installing Node.js 

Introduction

Node.js is a run-time environment which includes everything you need to execute a program written in JavaScript. It’s used for running scripts on the server to render content before it is delivered to a web browser.

2.1.1 Download Node.js Installer

In a web browser, navigate to https://nodejs.org/en/download/ 
The installer will prompt you for the installation location. Leave the default location, unless you have a specific need to install it somewhere else – then click Next.

#### Verify Installation

Open a command prompt (or PowerShell), and enter the following:

> node –v
	


## 3. Installing Node-RED

Introduction

Node-RED is a programming tool for wiring together hardware devices, APIs and online services in new and interesting ways.

It provides a browser-based editor that makes it easy to wire together flows using the wide range of nodes in the palette that can be deployed to its runtime in a single-click.

#### Installing Node-RED as a global module adds the command node-red to your system path. Execute the following at the command prompt:

> npm install -g --unsafe-perm node-red


### Adding A collection of Node-RED nodes for IBM Watson services:

> npm install node-red-node-watson


### Adding node-red-dashboard module:

This module provides a set of nodes in Node-RED to create a live data dashboard quickly.
> npm install node-red-dashboard




	
                                             




	   


# Task 1 Creating and deploying Watson discovery news app locally.

## 1.1 Creating Watson Discovery service on IBM cloud.

Pre-requisites :  IBM cloud account.

About Watson Discovery: IBM Watson Discovery, we can ingest, normalize, enrich, and search your unstructured data (JSON, HTML, PDF, Word, and more) with speed and accuracy. It packages core Watson APIs such as Natural Language Understanding and Document Conversion along with UI tools that enable you to easily upload, enrich, and index large collections of private or public data.

Step 1: Login to IBM cloud account.
Step 2: Click 'Create resource' on your IBM Cloud dashboard.
Step 3: Search the catalog for Discovery.
Step 4: Click Discovery to launch the create panel.
Step 5: From the panel, enter a unique name, a region and resource group, and a plan type (select the 		default lite plan). Click Create to create and enable your service..
The next step is to configure your Watson Discovery service.


## 1.2 Configuring Watson Discovery service on IBM cloud.

Step 1: Find the Discovery service in your IBM Cloud Dashboard.
Step 2: Click on the service and then click Launch tool

The Watson Discovery News data collection is already associated with your service. You'll use this collection as the data source for your app. To access the collection, you must find the COLLECTION_ID and ENVIRONMENT_ID. To find these values:

Step 3: Click on the collection from the Manage Data panel. In this case, it is named Watson Discovery News.
Step 4: Click on the drop-down icon located in the top right corner of the panel.






## 1.3 Saving Watson Discovery credentials.

you'll need to add the Watson Discovery credentials to the .env file Later.

Step 1: Locate the service credentials listed on the home page of your Discovery service.

Step 2: click on the download link and save the file.









## 1.4 Deploying Watson-discovery-news App locally. 

Note: Since deploying App on IBM cloud is not possible with Lite account so we deploy locally on your machines.

#### Step 1: Use the following command to clone the Watson-discovery-news GitHub repository.

> git clone https://github.com/ibm/watson-discovery-news



##### Step 2 : Use the following command to create .env file
> copy env.sample .env




### Step 3: Use the following command to Enter Watson discovery service credentials in .env file 
step to download credentials here
Copy paste the credentials from downloaded file to .env. 

> Notepad .env
	



#### Step 4: Installing packages and dependencies

A package is a folder containing a program described by a package.json file

This command installs a package, and any packages that it depends on.
> npm install 
	

	
#### Step 5: Running the deployed app. 

> npm start


The application will be available in your browser at http://localhost:3000
	



# Task 2 Integrating Slack bot with Watson discovery news app.

To integrate a new Slack Bot into your existing Slack team, navigate to https://<my.slack.com>/apps/manage/custom-integrations, where <my.slack.com> is the Slack workspace you want to customize.

## 2.1 Creating slack bot

Step 1: From the Cutsom Integrations page, select the Bots option.



Step 2: To add a new bot, select the Add Configuration button.


Step 3: Enter a username for the bot and click Add bot integration.


Step 4: Once created, save the API Token that is generated.



## 2.2 Configuring slack bot

Step 1: Edit the .env file and enter the Slack Bot API Token saved in the previous step.

> #Slack
> SLACK_BOT_TOKEN=<slack_bot_token>
> #note paste token without the brackets

Step 2: Restart application 

> npm start

# Task 3 Creating App user interface using node-red

Refer the project_report.pdf file in the repository for complete guid in building the UI 


> You can then access the Node-RED editor by pointing your browser at http://localhost:1880.


	


	
The Watson discovery application will be able to fetch relevant news articles within milliseconds, provide sentiment analysis on the fetched data, extract features, concepts, and keywords in the data all in the from of a simple UI.
User Interface can be found at http://localhost:1880/ui
	

## Advantages and Disadvantages
 
The web application provides interactive sentiment analysis.
It can be accessed through more than one platform that is through slack.
It collects and delivers the most recent data.
It does not have additional features like storing news history.
It does not provide a stand-alone app rather uses a web application. 

 
## Applications
 
This web applications can be used by any user in need of accurate and fast results.
Can be used by firms and organizations.
Can be used in stock market to make predictions.

 
## Conclusion
 
This project gives some basic working knowledge of the Watson Discovery Service and showed you how to use Discovery along with JavaScript and Node.js to build your own news mining web application.
 It also gives insight into real-world applications of AI and helps us understand Slack better.

 
## Future Scope
 
The web application van be integrated with cloud and made into a mobile app to use it on-the-go.
Additional sentiments can be added in the UI.
Related and trending news topics can be shown to the user.

## Bibliography


https://github.com/IBM/watson-discovery-news/

 https://nodered.org/

https://slack.com/intl/en-in/help/articles/360002079527-A-guide-to-Slack%E2%80%99s-Discovery-APIs 

https://www.w3schools.com/
















	

