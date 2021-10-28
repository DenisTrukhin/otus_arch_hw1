### Инструкция по запуску

1. Запускаем minikube
```
minikube start --vm-driver=virtualbox
```
2. Ставим ingress контроллер
```
minikube addons enable ingress
```
3. Применяем манифесты
```
kubectl apply -f .
```
4. Добавить *arch.homework* в ```/etc/hosts```


#### Тест
```
~$ curl http://arch.homework/
{"Hello":"World from hw1-deployment-59856d897-5c6v7"}

~$ curl http://arch.homework/health
{"status":"OK"}
```