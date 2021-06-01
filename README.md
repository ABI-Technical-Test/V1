

# ABI Technical Test

## Background

The ABI platform is a web portal built in-house that allows our _analysts_ to publish online articles for _users_. _Users_ can be entitled to one or more _channel_.

A _report_ is linked to a channel and report publication details are stored in the database whenever they are published. On the online platform _users_ can view the relevant reports based on their entitled _channels_. The data is stored in the database according to the data structures below.


```
{
	"name": "user1",
	"username": "user1@email.com",
	"entitlements": [
		{
			"channel": "ammonia",
			"expiry": "20-05-2021"
		},
		{
			"channel": "urea",
			"expiry": "09-10-2021"
		}]
		,
	"subscriptions": [
	{
		"channel": "ammonia",
		"delivery": "Friday",
	},
	{
		"channel": "urea",
		"deliveryDay": "Monday"
	}]
]
}
```

|Report|
|-|
| Title |
|PublishDate| 
|Channel|


We want to deliver a new feature that will allow a user to subscribe to a _'round-up'_ email. The user will be able to specify for a channel, the day on which to receive the 'round-up' email. This data will be stored in the following format:




## Objective

The objective of this task is to build a restful API that the Email service can call that with a date (typically today's date) and return a list of users and for each user a list of reports that they should receive. The _user story_ for this is detailed below.

### Story 1

As a content publishing service I want to provide a date range and get a list of the reports that have been published within that time and the list subscribed users for each report, so I can send the 'round-up' email covering that time period.  

In order to deliver this the email service expects list of reports with all the users subscribed to that report given they have the correct entitlements, as below.

```
"Reports":[
	{
		"ReportName" : "Ammonia Weekly Report 1",
		"SubscriberEmails": ["user1@domain.com", "user2@domain.com"]
	},
	{
		"ReportName" : "Nitrates Weekly Report 1",
		"SubscriberEmails": ["user1@domain.com", "user2@domain.com"]
	}
]
```


## Additional Guidelines
* Code to be completed with an appropriate level of testing using your favourite Unit testing an mocking frameworks.
* Database implementation is not required, feel free to stub out any data access.
* Code following SOLID principles

##Thank you, and good luck!!

