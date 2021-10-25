# Power Platform

## Block my calendar for 15 minutes after a long meeting
#### As many of us are now remote workers, it's easy to end up with a day of back-to-back events on your calendar.  
#### To promote a healthy work environment, this workflow saves time between meetings for a coffee refill, a restroom break, or just time to decompress after a long meeting.
This Power Automate workflow analyzes new events added to your calendar and if the event is longer than the specified duration (by default 90 minutes), Power Automate verifies your calendar doesn't have a event directly after the long meeting and adds a 15 minute block to your calendar.

![flow2 1](https://user-images.githubusercontent.com/45173956/138752560-5d703575-a25c-447b-a0f1-ab244926aa66.png)

Note: this workflow has a trigger condition that blocks the workflow from kicking itself off: it is based on the meeting "subject".  If you change the default subject of the meeting to something else, make sure you also change the trigger condition.
