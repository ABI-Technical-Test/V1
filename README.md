# ABI Technical Test

*Background*

The ABI platform allows our _analysts_ to publish online articles for _users_. _Users_ can be entitled to one or more _channel_.

A _report_ is linked to a channel and report publication details are stored in the database whenever they are published. On the online platform _users_ can view the relevant reports based on their selection. The dataset is like below:

|Report|
|-|
| Title |
|PublishDate| 
|Channel|


|User|
|-|
| Email |
|Channels| 

We want to deliver a new feature that allows a user to subscribe to a 'round-up' email. The user will use a page on the website to specify the day on which to receive the 'round-up' email. This data will be stored in the following format:

|Subscription|
|-|
|User|
|Channel|
|DeliveryDay|

**Objective**

Assume that the feature to story to allow the client to select their subscription preferences has already been built. The objective of this task is to build a restful API that the Email service can call that with a date (typically today's date) and return a list of users and for each user a list of reports that they should receive. The _user story_ for this is detailed below.

**Story 1**

As a customer I want to receive a 'round-up' email on the day I have specified for all my subscribed reports that have been published since my last 'round-up' email.
