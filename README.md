SW Engineering Spring 2023

[FAU: CEN 4010]


# ThinkSpace Social Media 

Group: 19


## 


## Team Members

Dustin Sherwood (Dsherwoo@fau.edu)

Carlo Leiva (leivac2019@fau.edu)

Vladia Zouga (vzouga2021@fau.edu)

Omar Khan (Okhan2021@fau.edu)

Bryan Barreto (bbarreto2021@fau.edu)

**Milestone 1 Project Proposal and High-level description**

Date  3/3/23

**Github**

[https://github.com/cen4010-fa23-g04/M1](https://github.com/cen4010-fa23-g04/M1)


## TABLE OF CONTENTS

Executive Summary

Data Definition 

Initial List of Functional Specifications

List of Non:Functional Specifications 

Use Cases

High-Level System Architecture

Competitive Analysis 

Team Roles


## Executive Summary

Chat applications (particularly group chats) have become an essential part of our daily lives, helping us stay connected with friends, family, and colleagues. However, what if you could take the experience to the next level? Our team is Introducing ThinkSpace, a chat application with integrated AI. This chat application will revolutionize the way we communicate by allowing us to interact with an AI that can understand and respond to our messages, making conversations more engaging, personalized, and efficient.

One of the key features of this chat application will be its ability to understand natural language and provide important information at a moment’s notice. This means that the AI will be able to interpret your messages and provide summaries, data, website links, and in-depth explanations. The AI will also be able to learn from the message feed, and provide perfect responses tailored to the subject at hand.

Lately, a lot of discussions between coworkers and peers are typically done on instant messaging applications. Often a piece of information that was in a past conversation is now relevant and they require what was part of that conversation. Unfortunately, that information could be crucial, and the employees have no idea where that part of the conversation was. But sometimes parts of that conversation aren’t all together, and information is missed. In order to avoid that, ThinkSpace will be able to collect every part of that conversation you were looking for and repeat it or summarize it.

ThinkSpace is an instant messaging platform designed to compile information from the chats log between individual users, or groups, and display it in any desired format. This application makes use of the artificial intelligence intelligence program - ChatGPT - as a way to create readable charts, graphs and more from data that was discussed previously between peers. ThinkSpace is designed to help gather thoughts and ideas that may have been discussed and forgotten, collect seemingly random information that was brought up long ago, or even help gather information from external sources. 

This chat application will also be highly customizable, allowing you to tailor your experience to your liking. With multiple custom chat feeds, roles, and multiple predefined prompts, professional and casual users will enjoy the benefits of AI.

In conclusion, chat applications with integrated AI are the future of communication. With its ability to understand natural language, analyze sentiment, summarize previous messages, and be highly customizable, this chat application will be a constant source of insight and information. So, why settle for a regular chat application when you can have one with integrated AI?


## Data Definition


<table>
  <tr>
   <td><strong>Name</strong>
   </td>
   <td><strong>Meaning</strong>
   </td>
   <td><strong>Usage</strong>
   </td>
   <td><strong>Comment</strong>
   </td>
  </tr>
  <tr>
   <td>User
   </td>
   <td>actor
   </td>
   <td>Throughout 
   </td>
   <td>This person familiar of reference
   </td>
  </tr>
  <tr>
   <td>Prompt
   </td>
   <td>data
   </td>
   <td>Throughout
   </td>
   <td> A string sent to ChatGPT for processing
   </td>
  </tr>
  <tr>
   <td>AI
   </td>
   <td>data
   </td>
   <td>Throughout
   </td>
   <td> ChatGPT processing responses
   </td>
  </tr>
  <tr>
   <td>Response
   </td>
   <td>data
   </td>
   <td>Throughout
   </td>
   <td> The result of a ChatGPT prompt
   </td>
  </tr>
  <tr>
   <td>Feed
   </td>
   <td>data
   </td>
   <td>Throughout
   </td>
   <td> The text and images posted by users
   </td>
  </tr>
  <tr>
   <td>Message
   </td>
   <td>data
   </td>
   <td>Throughout
   </td>
   <td> Text and images posted by users
   </td>
  </tr>
  <tr>
   <td>Chatbot
   </td>
   <td>data
   </td>
   <td>Architecture, Functional Specs
   </td>
   <td> ChatGPT in the context of text prompts and responses
   </td>
  </tr>
  <tr>
   <td>Conversation
   </td>
   <td>data
   </td>
   <td>Architecture, Functional Specs
   </td>
   <td> A collection of messages
   </td>
  </tr>
  <tr>
   <td>Tokens
   </td>
   <td>data
   </td>
   <td>Non-Functional Specs
   </td>
   <td> A mechanism to limit the complexity of a prompt
   </td>
  </tr>
  <tr>
   <td>Admin
   </td>
   <td>actor
   </td>
   <td>Non-Functional Specs
   </td>
   <td> A user empowered to alter the UI of a feed and add/remove users from the feed
   </td>
  </tr>
  <tr>
   <td>Group
   </td>
   <td>actor
   </td>
   <td>Use-Cases, Non-Functional Specs
   </td>
   <td> A collection of users with access to the same feeds
   </td>
  </tr>
</table>



## Initial List of Functional Specifications



1. Real-time Messaging:

     Users should be able to send and receive messages in real:time, with minimal latency.

2. User Authentication: 

    Users should be able to create an account, log in, and log out of the app securely.

3. AI Integration: 

    The app should be able to integrate with one or more AI chatbots that can respond to user messages with pre-defined or learned responses.

4. Natural Language Processing (NLP): 

    The app should use NLP to understand and interpret prompts, allowing for more accurate AI responses and improved user experience.

5. Predefined Prompts:

    Certain prompts will be predefined and implemented in the UI, allowing users to press a button to receive a response based on the feed.

6. Sentiment Analysis: 

    The app should be able to analyze the sentiment of user messages, allowing for more personalized responses and improved customer service.

7. Personalization and Customization: 

    The app should be able to personalize the user experience based on user preferences, past conversations, and other relevant data. The Admin of a group will be able to create different feeds and control access and User roles.

8. Search Functionality: 

    Users should be able to search for past conversations and messages within the app.

9. Multi-Platform Support: 

    The app should be available on multiple platforms, including mobile devices, desktops, and web browsers.

10. Security and Privacy: 

    The app should be designed with security and privacy in mind, ensuring that user data is protected and kept confidential.



## List of Non-Functional Specifications


### Performance Requirements

Responsiveness: The AI as well as user sent messages should be processed/retrieved in near real time since web sockets will be used 

Cycle Time: The time it takes to complete a single iteration of a software development will be around a week.

Speed Per Transaction: The speed for any given transaction should be less than 400 ms considering Firebase will be used.

Reliability: Since our application will be using Firebase it will be highly reliable, downtime should be minimized further if we were to use a scalable hosting service then reliability will be even greater.

Minimum Bug Counts: We have yet to decide on the minimum bug counts as we have yet to develop the program, however we intend to have no visible bugs in the core features; that includes the main feed, signup/login, and prompts.

Execution Speed: The execution speed of this program will be fast since we will be making it in Node.js and React.js.

Storage Utilization: We will be using Firebase to store user messages and images since it is scalable and has a low cost.

Robustness: Our program will be flexible enough to deal with errors, primarily ChatGPT errors such as limited tokens or the service being down due to high-volume of requests.

Training Time: Training time will be at most a few days, since it will be similar to Snapchat’s UI/Functionalities, which many Users are accustomed to.

Browser Compatibility: The application will be compatible with all popular browsers, such as Chrome, Edge, or Firefox.

Computer and OS Compatibility: Since it is a web application it should be compatible with all OS’s and computers that aren’t from before 2007. Planned expansion to mobile or desktop will require further research.

Expected Load: We have estimated if the application were to be successful that thousands of users would be putting stress on the application.

Login/Password System: The application will be including a password system to log in and log out to save user data.

Access Control: The application will use access control to provide security for the user's message and who is able to see their messages, and specify group Admins.

Spam Protection: The application will use spam protection to remove any spam messages from unknown users. 

Resource Utilization: Firestore runs asynchronously and should provide the needed resources. At this point of time, we do not know how much storage of the entire database we’ll need since we are unsure of how much storage a single message or image and its related logs will take up, but If a rough estimate were to be given then it would range in the gigabytes area. The free tier of Firestore provides 1 GiB of storage. ChatGPT has limited processing for the free API, so prompts will be limited by tokens.

Coding Standards: We will be using coding standards such as using camel casing, using comments in code, using messages in Github commits, using branches in Github to understand/remove unneeded branches of data, and finally we will be using Jira to track the tickets that each dev will handle.

Naming Conventions: We will be using camel casing as the naming convention for the application so we can neatly organize and specify our code.


## **Use Cases**


### Use Case(1): 
Users will be able to create an account and send messages and images to one another on the chat application platform in real time to communicate with one another.


### Use Case(2): 
Users will be able to get a summary of the messages based on a person, a selected topic, or a range of dates.


### Use Case(3): 
Users will be able to get the sentiment analysis of messages, basically sentiment analysis is the emotion or feeling conveyed.


### Use Case(4): 
Users will be able to ask questions to ChatGPT through the chat application, allowing for the users to ask questions and get answers in moments.


### Use Case(5): 
Users will be able to join into group chats and message other group members as well as view messages sent by other group members.


## **High Level System Architecture**

FAU Lamp Server: Lamp Server provided and hosted by FAU. Throughout the Spring 2023 semester, this server will be used to display the product.

 

JIRA: Project board and workflow management tool. This will help assist with sprints and track our progress throughout the semester. The Teachers Assistant (TA) will likely use this to examine our workflow and grade us.

 

Discord: Computer and mobile application used as primary communication between the team. Take notes, provide resources, brainstorm ideas and similar conversations will normally take place using this application.

 

Canvas: Application used by FAU students to receive assignments and past lectures. Our team will use it to obtain our assignment throughout our project. It will also be used to contact our Professor or TA for any assistance.

 

Google Firebase: a comprehensive mobile and web application development platform that provides a suite of services to help developers build, test, and deploy applications quickly and easily. It offers a range of services including authentication, real-time database, hosting, storage, cloud messaging, and more.

 

Firebase Firestore: A fully-managed, NoSQL document database service provided by Google Firebase. It is designed to store and sync app data in real-time across multiple clients and devices. Firestore offers a flexible data model based on collections and documents, and supports queries, indexing, and real-time updates.

 

ChatGPT API: A web-based application programming interface (API) developed by OpenAI that allows developers to integrate conversational AI into their applications. It provides a natural language processing (NLP) model that can understand and respond to user queries in a conversational way. The API is accessed through a RESTful endpoint and can be used to build chatbots, virtual assistants, and other conversational applications that can understand and respond to user input. The ChatGPT API is designed to be easy to use and customizable, and supports multiple programming languages and platforms.

 

Languages: HTML, Javascript

Scripting: CSS

 

Browser Compatibility: The Product will run on Internet Explorer, Google Chrome, Safari, Opera and any other browser that supports HTML5, CSS3 and Javascript.

 

Backup Architecture: In the event that the ChatGPT or other intended features become unwieldy in conjunction with Firebase/Firestore.

 

Application Framework: Express.js is a popular open-source web application framework for Node.js. It provides a set of features for building web and mobile applications, such as handling HTTP requests and responses, managing routes, and rendering views. Node.js is an open-source, cross-platform, JavaScript runtime environment that allows developers to build server-side applications using JavaScript. It is built on the V8 JavaScript engine from Google Chrome and provides an event-driven, non-blocking I/O model that makes it lightweight and efficient. React.js is a JavaScript library for building user interfaces. React allows developers to create reusable UI components and manage the state of their applications efficiently.

 

Nodemon: a command-line tool that helps with the development of Node. js applications.

 

Backup Database: MongoDB is a cross-platform, open-source NoSQL document-oriented database system. It stores data in flexible, JSON-like documents, allowing developers to work with data in a more natural way compared to traditional relational databases. MongoDB is known for its scalability, performance, and ease of use, and is commonly used for building modern web and mobile applications. It also provides a range of features such as automatic sharding, real-time analytics, full-text search, and more.


## **Competitive Analysis**

The analysis of competitors will include social media multiple large social medias that are running on the webpage. Examples of comparative social media competitors would be facebook, Twitter, Instagram , and tiktok. The competitive analysis will utilize a numerical scale (1=bad, 2=poor, 3=fair, 4=good, 5=outstanding) and consists of 4 social medias on a webpage. Our group's social media will be called “ThinkSpace”; however, this name is not official because there might be issues with getting the name for the website. Also 


<table>
  <tr>
   <td>
   </td>
   <td>twitter
   </td>
   <td>Instagram
   </td>
   <td>Facebook 
   </td>
   <td>Tik Tok 
   </td>
   <td>ThinkSpace
   </td>
  </tr>
  <tr>
   <td>Homepage
   </td>
   <td>3
   </td>
   <td>3
   </td>
   <td>3
   </td>
   <td>4
   </td>
   <td>3
   </td>
  </tr>
  <tr>
   <td>Images content
   </td>
   <td>4
   </td>
   <td>4
   </td>
   <td>3
   </td>
   <td>2
   </td>
   <td>3
   </td>
  </tr>
  <tr>
   <td>Navigation
<p>
 
   </td>
   <td>3
   </td>
   <td>2
   </td>
   <td>3
   </td>
   <td>3
   </td>
   <td>3
   </td>
  </tr>
  <tr>
   <td>Direct message
   </td>
   <td>3
   </td>
   <td>2
   </td>
   <td>4
   </td>
   <td>2
   </td>
   <td>1
   </td>
  </tr>
  <tr>
   <td>Text feed
   </td>
   <td>5
   </td>
   <td>2.5
   </td>
   <td>4
   </td>
   <td>1
   </td>
   <td>3
   </td>
  </tr>
  <tr>
   <td>AI response
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>3
   </td>
  </tr>
  <tr>
   <td>Mean
   </td>
   <td>3.16
   </td>
   <td>2.41
   </td>
   <td>3
   </td>
   <td>2.1
   </td>
   <td>2.67
   </td>
  </tr>
</table>


**Twitter**

Twitter is a social media platform that allows users to share their thoughts, opinions, and news in 280-character messages called "tweets". 

 

<span style="text-decoration:underline;">Navigation</span> : Twitter has a top navigation bar that allows users to access different sections of the site, including Home, Explore, Notifications, Messages, and Profile.

<span style="text-decoration:underline;">Direct Messages</span>: Twitter’s Direct Messages (DMs) allow users to send private messages to other Twitter users.

<span style="text-decoration:underline;">Text Feed</span>: Twitter's main feed is a constantly updating stream of tweets from people and accounts that a user follows.

<span style="text-decoration:underline;">Homepage</span>: Twitter's homepage is where users can discover trending topics, popular tweets, and suggestions for new accounts to follow.

 

**Instagram**

 

Instagram is a social media platform that focuses on visual content, allowing users to share photos and videos with their followers.

 <span style="text-decoration:underline;">Navigation</span>: Instagram has a bottom navigation bar that allows users to access different sections of the app, including Home, Search, Reels, Shop, and Profile.

<span style="text-decoration:underline;">Direct Messages</span>: Instagram's Direct Messages (DMs) allow users to send private messages to other Instagram users

<span style="text-decoration:underline;">Text Feed:</span> Instagram's main feed is a constantly updating stream of photos and videos from people and accounts that a user follows. 

<span style="text-decoration:underline;">Homepage</span>: Instagram's homepage is where users can discover new content, including posts from accounts they don't follow, popular posts, and suggestions for new accounts to follow. 

 

**TikTok**

TikTok is a social media platform that allows users to create and share short-form videos with their followers.

<span style="text-decoration:underline;">Navigation</span>: TikTok has a bottom navigation bar that allows users to access different sections of the app, including Home, Discover, Inbox, and Profile.

<span style="text-decoration:underline;">Direct Messages</span>: TikTok's Inbox feature allows users to send private messages to other TikTok users. Users can also participate in group chats with multiple users.

<span style="text-decoration:underline;">Video Feed:</span> TikTok's main feed is a constantly updating stream of short-form videos from people and accounts that a user follows.  

<span style="text-decoration:underline;">Homepage</span>: TikTok's homepage is where users can discover new content, including videos from accounts they don't follow, popular videos, and suggestions for new accounts to follow.


### **Planned Advantages of  ThinkSpace**

An advantage our social media “ThinkSpace” will have over the others is having  an AI feature implemented to the platform which will prompt a summary of a user's post over a week's time period. The feature will also use chat gpt to send prompts and post responses. This Will be a major advantage compared to other social medias

ThinkSpace will have a simple and functional home page similar with twitter ,instagram, and facebook.The image content,text feed will consist of a hybrid of both twitter and instagram.Direct messages will be similar to facebook's messenger ;however this is a feature.


## Team Roles


### Developers



* Omar Khan
* Bryan barreto


### Scrum Masters



* Carlo Leiva
* Vladia Zouga


### Project Owner



* Dustin Sherwood
