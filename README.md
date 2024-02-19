# Technical test

## Introduction

Fabien just came back from a meeting with an incubator and told them we have a platform “up and running” to monitor people's activities and control the budget for their startups !

All others developers are busy and we need you to deliver the app for tomorrow.
Some bugs are left and we need you to fix those. Don't spend to much time on it.

We need you to follow these steps to understand the app and to fix the bug : 
 - Sign up to the app
 - Create at least 2 others users on people page ( not with signup ) 
 - Edit these profiles and add aditional information 
 - Create a project
 - Input some information about the project
 - Input some activities to track your work in the good project
  
Then, see what happens in the app and fix the bug you found doing that.

## Then
Time to be creative, and efficient. Do what you think would be the best for your product under a short period.

### The goal is to fix at least 3 bugs and implement 1 quick win feature than could help us sell the platform

## Setup api

- cd api
- Run `npm i`
- Run `npm run dev`

## Setup app

- cd app
- Run `npm i`
- Run `npm run dev`

## Finally

Send us the project and answer to those simple questions : 
- What bugs did you find ? How did you solve these and why ? 

1. Debug of User page :
The name button was disabled and the Update Button wasn't sending data to the API.
I removed the disabled for the name field and change the OnChange by Onlcik to ensure the action.

2. Debug of Project Page:
The project page was not accessible. It was because the controler for project was using the MongoDB method find. It is used to retrieve all the corresponding project. For a single result as we want we are expecting a single project, findOne is more appropriate.

3. Security Signup issue :
The password wasn't enough secured, no minimum of charaters, no checking of content.
I add the minimun of 8 characters and a regex to be sure that both numbers and letters were used.


- Which feature did you develop and why ?
On the page activity, I added the fact that each activity is done by a specific user. I added up because the app was not differentiate activity between users on a project.

- Do you have any feedback about the code / architecture of the project and what was the difficulty you encountered while doing it ? 

The Structure is not complex and have a MVC pattern. Many bugs concern more the ergonomic part and the dynamic of react is not always used, but the main elements are already present.
