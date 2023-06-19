# Instructions to deploy on your machine
## Local run
Here are the steps to run services locally:
* Install [Java 8](https://docs.oracle.com/javase/8/docs/technotes/guides/install/install_overview.html)
* Make sure you are using Java 8
* Run postgresql database locally:
    ```
        docker run --name some-postgres -e POSTGRES_PASSWORD=password -d postgres:15-alpine
* Run service:
    ```
        mvn spring-boot:run

### Note
In order to make all services work, please, run eureka server which will detect all other services that you are running.

## Automated Deploy
Here are the steps to deploy those applications on your machine with proper automated deployment
* Install [Dokku](https://dokku.com/docs/getting-started/installation/) on your server machine
* Create applications and git repos on Dokku:
    ```
    sudo dokku apps:create <appname>
    sudo dokku git:initialize  <appname>
* Change appname in github workflow to the one of your choice.
* Add private ssh key of your machine to github actions secrets using key SSH_PRIVATE_KEY
* Change dokku server ip in repository workflow
* Change docker registry in repository workflow
* Then merge/push to main branch
* Profit.

## Optional
You can change credentials for SonarCloud and make sonar.yml workflow working.
