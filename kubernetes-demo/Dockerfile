FROM openjdk:17
EXPOSE 8080
ADD target/kubernetes-demo.jar kubernetes-demo.jar
ENTRYPOINT ["java","-jar","/kubernetes-demo.jar"]