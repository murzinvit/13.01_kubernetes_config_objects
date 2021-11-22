### 13.01_kubernetes_config_objects </br>
Настроив кластер, подготовьте приложение к запуску в нём. Приложение стандартное: бекенд, фронтенд, база данных </br>
### Задание 1: подготовить тестовый конфиг для запуска приложения: </br>
Для начала следует подготовить запуск приложения в stage окружении с простыми настройками. Требования: </br>
под содержит в себе 3 контейнера — фронтенд, бекенд, базу;  </br>
регулируется с помощью deployment фронтенд и бекенд;  </br>
база данных — через statefulset.  </br>
Перед выполнением поднял NFS сервер, и использовал NFS шару для statefulset </br>
Создание volume: [make_volume.yaml](https://github.com/murzinvit/13.01_kubernetes_config_objects/blob/2faeb6595706843e6738eebd7d609e18469e368e/make_volume.yaml) </br>
Запуск 3 контейнеров в 1 поде: [make_pod3.yaml](https://github.com/murzinvit/13.01_kubernetes_config_objects/blob/2faeb6595706843e6738eebd7d609e18469e368e/make_pod3.yaml)</br>
Результат:(посмотреть содержимое пода можно командой - `kubectl describe pod`) </br>
![3_image_in_1_pod](https://github.com/murzinvit/screen/blob/f3a37036707de1cf615f9c3ae9fe890e4f86ff23/Kuber_3_image_in_1_pod.jpg) </br>
Volume: </br>
![kuber_volume_pvc](https://github.com/murzinvit/screen/blob/fec2dee77f055bce28fc061b2f2d27082b86bdd1/Kuber_volume_pvc_2Gb.jpg) </br>

### Задание 2: подготовить конфиг для production окружения: </br>


### Рабочие заметки: </br>
Настройка LocalPersistentVolume: https://serveradmin.ru/hranilishha-dannyh-persistent-volumes-v-kubernetes/ </br>
Система в k8s: https://www.digitalocean.com/community/tutorials/how-to-set-up-an-elasticsearch-fluentd-and-kibana-efk-logging-stack-on-kubernetes-ru </br>
`yum install nfs-utils nfs-utils-lib -y` - для монтирования nfs на нодах кластера k8s </br>
`mount.nfs 10.10.1.10:/var/nfs /mnt` </br>
Volumes in deployment: https://akomljen.com/kubernetes-persistent-volumes-with-deployment-and-statefulset/ </br>
Хороший пример: https://support.huaweicloud.com/intl/en-us/usermanual-cce/cce_01_0269.html </br>

