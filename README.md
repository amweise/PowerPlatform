# Power Platform

## Create a "back-channel" internal chat for any meeting
#### We've all be there - you're on a call with a customer and members of your team and you want to chat with your teammates.  Unfortunately, it's a manual process.   
QuickChat is a Power App that pulls in your calendar information from your Office 365 Outlook calendar.  The app user can then select a meeting to create the internal chat for.

![quickChat1](https://user-images.githubusercontent.com/45173956/159943415-84c7212f-a5a7-43a0-8067-e22eee59e707.png)

A Power Automate workflow is then kicked off, grabbing all required attendees for that meeting and then filtering out any individual whose domain (the @company.com part of your email) that doesn't match your own domain.
A Teams group chat is then created with all internal, required attendees and is named "Internal - <Meeting Name>".  Lastly, the first chat message is sent by the Power Automate bot informing individuals that the chat was created.
The outcome is a Teams group chat, ready for you to use!
  
![quickChat4](https://user-images.githubusercontent.com/45173956/159943483-aec30f8a-184e-4a57-bbf2-fb13393cb9f9.png)
  
## Block my calendar for 15 minutes after a long meeting
#### As many of us are now remote workers, it's easy to end up with a day of back-to-back events on your calendar.  
#### To promote a healthy work environment, this workflow saves time between meetings for a coffee refill, a restroom break, or just time to decompress after a long meeting.
This Power Automate workflow analyzes new events added to your calendar and if the event is longer than the specified duration (by default 90 minutes), Power Automate verifies your calendar doesn't have a event directly after the long meeting and adds a 15 minute block to your calendar.

![flow2 1](https://user-images.githubusercontent.com/45173956/138752560-5d703575-a25c-447b-a0f1-ab244926aa66.png)

Note: this workflow has a trigger condition that blocks the workflow from kicking itself off: it is based on the meeting "subject".  If you change the default subject of the meeting to something else, make sure you also change the trigger condition.

## Send Me New Power Apps and Power Automate Blog Posts in Teams
#### These two workflows ensure that you are staying up-to-date on all the new Power Apps/Power Automate news
Using adaptive cards in Teams chat, you can receive actionable messages regarding new Power Platform updates
#### Power Apps
![appsblog2](https://user-images.githubusercontent.com/45173956/138892937-0d472831-d1e5-42b3-9c9b-67c3e719eafd.png)
#### Power Automate
![flowblog2](https://user-images.githubusercontent.com/45173956/138892950-29560ffb-1879-44fc-8a49-dfbc3b15e6d0.png)

