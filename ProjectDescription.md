# DE1TermProject1
Data Engineering 1, Term Project 1

This project looks into on 1 day of user activity during working hours from 9:00 to 18:00 focusing on building a portrait of an average user in that period and their hourly activity.

The database includes four tables united by user id.
`users` include:
- user id
- name
- last name
- age
- subscription date (UNIX timestamp)
`friends` include:
- user id 1
- user id 2
`posts` include:
- user id
- type of post
- post date (UNIX timestamp)
`reactions` include:
- user id
- type of reaction
- reaction date (UNIX timestamp)

The analytical layer aims at providing a look at the data from the perspective of an average user to build and understand their portrait with the following metrics:
- average user age
- average number of posts per user during working hours
- average number of reactions per user during working hours
- average number of friends per user
- most common post type during working hours
- most common reaction type during working hours

The following data marts are available that allow to monitor daily user activity during the working hours:
- hourly number of new users (subscriptions) during working hours (with hourly updates)
- hourly number of posts during working hours
- hourly number of reactions during working hours

The project introduces several stored procedures:
- extracting data of n most or least active (by post) users
- separating new users into "morning", "afternoon" and "evening" users by subcription time
