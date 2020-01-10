Данная репа служит хранилищем для обучающих материалов.

Что бы начать чему то учиться, нужно знать:
1. Основы работы с Linux. Если вы не знаете, что такое git checkout, идите учите.
2. Что такое Nginx, Vagrant, Mysql, PHP, Docker. Если не знаете, рано вам еще. Подучитесь.
3. Если вы не знаете что такое апстрим, то вот вам: https://nginx.org/ru/docs/http/ngx_http_upstream_module.html
Весь тестовый стенд раскатывается вагрантом из Vagrantfile(пожалуйста).

На F1, F2, B1, B2 и nginx, устанавливается nginx. У F1 и F2 есть один апстрим с двумя серверами (B1, B2). У B1 и B2, тоже один апстрим (Nginx), у NGINX апстримом будет Service , на котором работает WordPress например. Базой для него являются sqlmaster и sqlslave, соответсвенно с master-slave репликацией.

Общая схема вот:

![Schema](https://github.com/Valerych-team/learn/raw/master/img/schema.jpg)
