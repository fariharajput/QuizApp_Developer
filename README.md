# QuizApp_Developer
Table of Content
================

* * * * *
-   [Getting started](#)
-   [How to get files](#)
-   [Change and Customization](#)
-   [How this app's code helps you](#)
-   [Deployment](#)
<hr>


![QuizApp_Developer](https://github.com/fariharajput/QuizApp_Developer/blob/main/screencapture-developer-quizapp-netlify-app-2021-04-27-23_52_32.png)


<a href="https://developer-quizapp.netlify.app/">Live demo</a>
<hr>

Getting Started
===============

* * * * *

These instructions will get you a copy of the project up and running on
your local machine for development and testing purposes

First you will need to install [Git](https://git-scm.com/downloads) and [Node.js](https://nodejs.org/en/download/) on your local machine/computer.

How to get files
================

* * * * *

When you have done with installation!

Go to your required directory, and open GIT command line by right clicking on the screen and select 'GIT BASH HERE'

then you get a command line interface

put command to clone the files on your local computer
```git
\$ git clone https://github.com/fariharajput/QuizApp_Developer.git
```
**** 

Change and Customization
========================

* * * * *

You can change the `quiz.js` file to addd more functionalities to the app


following is the code of operations performing on each button 

On **start** button firstly we have to check that either any of the input field is empty or not
if the any of the input field will be empty then we show an error message to the user
Here we are also storing the _current time_ which is the starting time of the session
```js
myBtns.addEventListener('click',(e)=>{
    if(e.target.classList.contains('start')){
        if(workDuration !== '0' && workDuration !==''){
            if(breakDuration !== '0' && breakDuration !== ''){
                if(shortDesc !== ''){
                    myIntervals();
                    disabling();
                    console.log(1)
                    myBtns.children[1].classList.remove('d-none')
                    myBtns.children[2].classList.add('d-none')
                    const checkCurrtime = new Date();
                    currentTime = checkCurrtime.toLocaleTimeString();
                }
                else{
                errorMessage.classList.remove('d-none')
                }
            }
            else{
            errorMessage.classList.remove('d-none')
            }
        }
        else{
            errorMessage.classList.remove('d-none')
        }
```
On other (pause,resume,stop) buttons we are performing basic operation as if we click on the _pause button_
\
it will cause the _pause button_ to hide and show the _resume button_ same is the operation with _resume button_

Code given below is performing time decreasing operation

The _Work minutes_ and the _Break minutes_ are the _Work Duration_ and the _Break Duration_ which we get from user 

On each call of this function we are decreasing seconds and minutes respectively 

Every time the work duration become over 'workMinutes === -1' we start the break session and 
respectively and when the break session will over we again started the work session

At the End when the session will be stoped we have to clear all the inputs and the session itself
So for this purpose we do clear and reset all the variables we want to be cleared 
How this app's code helps you
========================
In the `quiz.js` file you can get the javascript code 

Using the code you can be able to creat a pomodoro timer in which you can allow the
user to set a session time in which user is needed to provide work duration and break duration 
and the short description about the task

You have to just check the working of code and apply this code in your project and make your projects more awesome

Deployment
========================
When you have done with the setup you should host your site online

You can use [NETLIFY](https://www.netlify.com/) for deployment of your

for more information please read [hosting on Netlify](https://create-react-app.dev/docs/deployment/#netlify)

