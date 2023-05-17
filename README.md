# Домашнее задание к занятию "14.3 Карты конфигураций"

## Задача 1: Работа с картами конфигураций через утилиту kubectl в установленном minikube

Выполните приведённые команды в консоли. Получите вывод команд. Сохраните
задачу 1 как справочный материал.

### Как создать карту конфигураций?

```
kubectl create configmap nginx-config --from-file=nginx.conf
kubectl create configmap domain --from-literal=name=netology.ru
```

### Вывод команд

![Скриншот](img/Task1_1.png)

### Как просмотреть список карт конфигураций?

```
kubectl get configmaps
kubectl get configmap
```

### Вывод команд

![Скриншот](img/Task1_2.png)

### Как просмотреть карту конфигурации?

```
kubectl get configmap nginx-config
kubectl describe configmap domain
```

### Вывод команд

![Скриншот](img/Task1_3.png)

### Как получить информацию в формате YAML и/или JSON?

```
kubectl get configmap nginx-config -o yaml
kubectl get configmap domain -o json
```

### Вывод команд

![Скриншот](img/Task1_4.png)

### Как выгрузить карту конфигурации и сохранить его в файл?

```
kubectl get configmaps -o json > configmaps.json
kubectl get configmap nginx-config -o yaml > nginx-config.yml
```

### Вывод команд

![Скриншот](img/Task1_5.png)

### Как удалить карту конфигурации?

```
kubectl delete configmap nginx-config
```

### Вывод команд

![Скриншот](img/Task1_6.png)

### Как загрузить карту конфигурации из файла?

```
kubectl apply -f nginx-config.yml
```

### Вывод команд

![Скриншот](img/Task1_7.png)
