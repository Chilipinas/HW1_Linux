# Linux Задание 1
Cоздадим 3 виртуальные машины Play with docker и присоединим их к локальному терминалу по SSh:
![info](img.png)

## Настройка виртуальных машин
### Linux A
![info](img_1.png)
### Linux B
![info](img_2.png)
### Linux C
![info](img_3.png)
### Веб-сервер Linux A 
![info](img_4.png)
### Веб-клиент Linux С 
![info](img_5.png)
## Проверка 
Что бы проверить работу адаптера отправляем cyrl запрос от веб-клиента к веб-серверу. В результате, мы увидим, что запрос успешно дошел.

![info](img_6.png)

Если мы поменяем порт на отличный от 5000, то запросы не смогут проходит через наш шлюз.

![info](img_7.png)

## Bash скрипт
Запустим bash скрипт для каждой виртуальной машины, который повторяет действия сделанные вручную. Для этого создадим заново 3 виртуалки и в результате сurl клиента принимает ответ от сервера из разных подсетей.

После запуска скрипта [LinuxA.sh](configs/LinuxA.sh) на машине А, будет произведена его настройка и сразу же запустится веб-сервер с ожидаем запросов.
![info](img_8.png)

После запуска скрипта [LinuxB.sh](configs/LinuxB.sh) на машине В, появятся новые порты.
![info](img_9.png)

После запуска скрипта [LinuxC.sh](configs/LinuxC.sh) на машине С, будет произведена его настройка и сразу же отправится запрос на веб-сервер А через шлюз В.

![info](img_10.png)

После исполнения последнего скрипта на веб-сервер сразу приходит запрос. Это значит, что шлюз, веб-сервер и веб-клиент работают исправно.

![info](img_11.png)



