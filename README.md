# spring-boot-web-buildpacks-minikube-maven-java
```
mvn -Pnative spring-boot:build-image
```
```
minikube start --cpus=4 --memory=4096
```
```
minikube image load web:0.0.1-SNAPSHOT
```
```
kubectl apply -f k8s/deployment.yaml
```
```
kubectl apply -f k8s/service.yaml
```
```
kubectl apply -f k8s/storage-pvc.yaml
```
```
kubectl port-forward svc/spring-boot-service 8080:8080
```
```
kubectl scale deployment spring-boot-app --replicas=0
```
```
minikube stop
```
