### 13.01_kubernetes_config_objects </br>
Настроив кластер, подготовьте приложение к запуску в нём. Приложение стандартное: бекенд, фронтенд, база данных </br>
### Задание 1: подготовить тестовый конфиг для запуска приложения: </br>
Для начала следует подготовить запуск приложения в stage окружении с простыми настройками. Требования: </br>
под содержит в себе 3 контейнера — фронтенд, бекенд, базу;  </br>
регулируется с помощью deployment фронтенд и бекенд;  </br>
база данных — через statefulset.  </br>

### Задание 2: подготовить конфиг для production окружения: </br>


### Рабочие заметки: </br>
Настройка LocalPersistentVolume: https://serveradmin.ru/hranilishha-dannyh-persistent-volumes-v-kubernetes/ </br>
Система в k8s: https://www.digitalocean.com/community/tutorials/how-to-set-up-an-elasticsearch-fluentd-and-kibana-efk-logging-stack-on-kubernetes-ru </br>
`yum install nfs-utils nfs-utils-lib -y` - для монтирования nfs на нодах кластера k8s </br>
`mount.nfs 10.10.1.10:/var/nfs /mnt` </br>

