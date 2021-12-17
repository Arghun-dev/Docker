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

There is one more benefit here, When we're done with one of these applications, and don't want to work on it any more, we can remove the application and all of it's dependencies in one go, without docker as we work on different projects, our development machine gets cluttered with so many libraries and tools that are used by different applications, and then after a while, we don't know if we can remove one or more of these tools, because we're always afraid that we would mess up with some application, with docker we don't have to worry about this.

`$. docker compose down --rmi all`

because each application runs with its dependencies inside an isolated environment, we can safely remove an application, with all its dependencies to clean up our machine, isn't that great?


## Virtual Machines vs Container

**Container: ** => An isolated environment for running an applications.
**Virtual Machine** => is an abstraction of a machine (physical hardware), so we can run several virtual machines on a real physical machine, for example we have a mac, and on this mac, we can run two virtual machines, one running windows and other running linux. with virtual machine you can isolate the environments, but in this way, your system memory will be divided into several chunks. But if you use `docker` you will not have such a problem.

**Containers Advantages** => 

1. Allow running multipe apps in isolation
2. Are lightweight
3. Use OS of the host
4. Start quickly
5. Need less harware resources

## Installing Docker


