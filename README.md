Zie https://spring.io/guides/gs/spring-boot-kubernetes/

Build app en docker image:
- $ ./mvnw install
- $ ./mvnw spring-boot:build-image

Run hem op k8s:
- $ kubectl apply -f deployment.yaml
- $ kubectl port-forward svc/demo 8080:8080

Test: 
```
$ curl localhost:8080/actuator/health
{"status":"UP"}
```
