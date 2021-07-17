# BiometricSystemsProject

This docker-compose file wraps the project up. 

## Dependencies

Before you run docker-compose you should populate this repository with the code to build the following services:
- this project repo
    - [client](https://github.com/RD-dambro/BiometricSystemsClient)
    - server
        - [web](https://github.com/RD-dambro/BiometricSystemsWeb)
        - [worker](https://github.com/RD-dambro/BiometricSystemsWorker)
    - user
        - [angapp](https://github.com/RD-dambro/BiometricSystemsApp)

Clone the repos in that structure or simply change the build paths

The following services will pull a docker image:
- [db](https://hub.docker.com/_/postgres/) 
- [rabbit](https://hub.docker.com/_/rabbitmq/)
- [media](https://github.com/illuspas/Node-Media-Server)

To run the containers run `docker-compose up --build -d`

to stop the containers run `docker-compose down`

to manage single containers use docker cli