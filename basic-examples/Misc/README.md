Actually When we use docker as node for a pipline, Jenkins will clone git repo in jenkins workspace and bind it to docker container and once pipeline execution is done it will remove bind mounts. But git repo will still be present in jenkins workspace.

Once pipeline exection is done Jenkins will remove bind mount, because of that we can't access workspace directory inside container if we bash into it.

https://stackoverflow.com/questions/77972903/strange-behavior-while-listing-directories-in-jenkinsfile-where-docker-is-runnin

Bind Mounts - https://docs.docker.com/storage/bind-mounts/
