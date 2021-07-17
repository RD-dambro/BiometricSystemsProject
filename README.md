# BiometricSystemsProject

This docker-compose file wraps the project up. 

## QuickStart

Simply open a linux terminal and type:
- > `sudo chmod +x bsp_setup.sh`
- > `./bsp_setup.sh`
- > `docker-compose up --build -d`


## Dependencies

Before you run docker-compose you need to populate this repository with the code to build the following services:
- this project repo
    - [client](https://github.com/RD-dambro/BiometricSystemsClient)
    - server
        - [web](https://github.com/RD-dambro/BiometricSystemsWeb)
        - [worker](https://github.com/RD-dambro/BiometricSystemsWorker)
    - user
        - [angapp](https://github.com/RD-dambro/BiometricSystemsApp)

This is done in `bsp_setup.sh` by running the following commands:
- > git clone https://github.com/RD-dambro/BiometricSystemsClient.git client
- > git clone https://github.com/RD-dambro/BiometricSystemsWeb.git server/web
- > git clone https://github.com/RD-dambro/BiometricSystemsWorker.git server/worker
- > git clone https://github.com/RD-dambro/BiometricSystemsApp.git angapp

The following services will pull a docker image:
- [db](https://hub.docker.com/_/postgres/) 
- [rabbit](https://hub.docker.com/_/rabbitmq/)
- [media](https://github.com/illuspas/Node-Media-Server)

To run the containers run docker-compose up --build -d

to stop the containers run docker-compose down

to manage single containers use docker cli