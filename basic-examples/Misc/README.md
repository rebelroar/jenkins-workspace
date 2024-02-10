Actually When we use docker as node for a pipline, Jenkins uses Docker mount to inject jenkins workspace directory into the container. That is why it can list out current git repository directories and also java version installed in the tomcat image.

Once pipeline exection is done Jenkins will remove bind mount, That's why we can't see workspace directory inside container if we bash into it.
