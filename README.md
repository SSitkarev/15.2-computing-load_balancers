# Домашнее задание к занятию «Вычислительные мощности. Балансировщики нагрузки» - Сергей Ситкарёв

## Задание 1. Yandex Cloud

### 1. Создать бакет Object Storage и разместить в нём файл с картинкой:

Создать бакет в Object Storage с произвольным именем (например, имя_студента_дата). 
Положить в бакет файл с картинкой. 
Сделать файл доступным из интернета.

[Bucket](https://github.com/SSitkarev/15.2-computing-load_balancers/blob/main/bucket.tf)

![Задание1](https://github.com/SSitkarev/15.2-computing-load_balancers/blob/main/img/1.jpg)

### 2. Создать группу ВМ в public подсети фиксированного размера с шаблоном LAMP и веб-страницей, содержащей ссылку на картинку из бакета:

Создать Instance Group с тремя ВМ и шаблоном LAMP. Для LAMP рекомендуется использовать image_id = fd827b91d99psvq5fjit.
Для создания стартовой веб-страницы рекомендуется использовать раздел user_data в meta_data.
Разместить в стартовой веб-странице шаблонной ВМ ссылку на картинку из бакета.
Настроить проверку состояния ВМ.

[Instance Group](https://github.com/SSitkarev/15.2-computing-load_balancers/blob/main/instance-group.tf)

![Задание2](https://github.com/SSitkarev/15.2-computing-load_balancers/blob/main/img/2.jpg)

![Задание2](https://github.com/SSitkarev/15.2-computing-load_balancers/blob/main/img/3.jpg)

### 3. Подключить группу к сетевому балансировщику:

Создать сетевой балансировщик.

[Load Balancer](https://github.com/SSitkarev/15.2-computing-load_balancers/blob/main/load-balancer.tf)

![Задание3](https://github.com/SSitkarev/15.2-computing-load_balancers/blob/main/img/4.jpg)

![Задание3](https://github.com/SSitkarev/15.2-computing-load_balancers/blob/main/img/5.jpg)

Проверить работоспособность, удалив одну или несколько ВМ.

![Задание3](https://github.com/SSitkarev/15.2-computing-load_balancers/blob/main/img/6.jpg)

![Задание3](https://github.com/SSitkarev/15.2-computing-load_balancers/blob/main/img/7.jpg)