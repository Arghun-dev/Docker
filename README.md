# Docker

## What is Docker? 

Docker is a platform for building, running and shipping applications, in a consistent manner, so  if your application, works on your development machine, it can run and function in the same way on other machine.

If you are developing software for a while, you've probably come across to the situation, your application works on your development machine, but does not somewhere else.

## Why this happens?

1. One or more files missing
2. Software version mismatch (let's say your application needs Node version 14, but the target machine using Node version 9)
3. different configuration settings

**This is where Docker comes to rescue**

with `Docker` we can package our application, with everything it needs, and run it anywhere on any machine with docker. So if your application needs a specific version of Node and Mongo DB, all of these will be included in your application's package. And now we can take this package and run on any machine that uses docker. If it works on your development machine, it's definitely works on your test and production machines. And there's more, if someone joins your team, they will have to spend half a day or so, setting up the machine, to run your application, they will have to install all the different dependencies.

Instead, they simply tell `docker` => `$. docker compose up` => bring up your application, and docker itself will automatically download and install all the dependencies, inside an isolated environment called `container` => **This is the beauty of docker**

This isolated environment, allows multiple applications, use different versions of some software side by side, So one application make use Node version 14 and another application make use of Node version 9, all these applications can run side by side, on the same machine without messing each other. So this is how docker allows us to consistently run our applications on different machines.
