# Домашнее задание к занятию "`Репликация и масштабирование. Часть 1`" - `Заярченко Ивана`



### Задание 1

На лекции рассматривались режимы репликации master-slave, master-master, опишите их различия.

Ответить в свободной форме.

## Ответ 1

# Master-Slave
Один мастер (запись), один/несколько слейвов (чтение).
Данные только от мастера к слейву.
Плюсы: простота, масштабирование чтений.
Минусы: при падении мастера — ручное переключение.

# Master-Master
Оба сервера могут и писать, и читать.
Данные синхронизируются в обе стороны.
Плюсы: отказоустойчивость, запись на любом узле.

### Задание 2

Выполните конфигурацию master-slave репликации, примером можно пользоваться из лекции.

Приложите скриншоты конфигурации, выполнения работы: состояния и режимы работы серверов.

Настройка Master

![1](https://github.com/vonoid/Replication-1/blob/9ec33fa8680e113cc7d4856f933ecbd30dcd32d2/img/1.jpg)

Статус Slave

![2](https://github.com/vonoid/Replication-1/blob/9ec33fa8680e113cc7d4856f933ecbd30dcd32d2/img/2.jpg)

![3](https://github.com/vonoid/Replication-1/blob/9ec33fa8680e113cc7d4856f933ecbd30dcd32d2/img/3.jpg)

Праметры файла my.cnf

![4](https://github.com/vonoid/Replication-1/blob/9ec33fa8680e113cc7d4856f933ecbd30dcd32d2/img/4.jpg)

Подключение к базам с другого хоста:

![5](https://github.com/vonoid/Replication-1/blob/9ec33fa8680e113cc7d4856f933ecbd30dcd32d2/img/5.jpg)

Результат репликации при создании базы на Master:

![6](https://github.com/vonoid/Replication-1/blob/9ec33fa8680e113cc7d4856f933ecbd30dcd32d2/img/6.jpg)
















