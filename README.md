# Alliance Jumpstart Program

## System Requirements

Your System should have the following installed:

* [Docker CE][docker]: refer for [Linux][linux] and [Windows][windows] installation
* [JDK 8][jdk8] 

*Additional Note: Contributors should create a Docker account especially Windows Users so that you can use Docker*

## Starting The Application

Once done cloning get inside the directory:

    git clone https://github.com/Pofay/alliance-jumpstart-updated.git
    cd alliance-jumpstart-updated 

Run the Following Commands in your Terminal/Command Line as per your O.S:

For Linux & Mac

    ./mvnw install dockerfile:build

For Windows

    mvnw.cmd install dockerfile:build

**This will build the appropriate Docker Image for the Application.**

To Run the image:

    docker-compose up

*Note: Incase you get errors the first time running docker-compose don't panic, run it again and it'll probably work*


## For Rebuilds and Restarts

**To allow code changes to take effect you need to rebuild and restart the docker image.**

The commands for rebuilding and restarting are as follows:

For Linux & Mac:

    ./mvnw clean package dockerfile:build
    docker-compose up

For Windows:

    mvnw.cmd clean package dockerfile:build
    docker-compose up


[linux]: https://docs.docker.com/install/linux/docker-ce/ubuntu/
[windows]: https://hub.docker.com/editions/community/docker-ce-desktop-windows
[jdk8]: https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
[docker]: https://www.docker.com/
