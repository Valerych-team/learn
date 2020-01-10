Данная репа служит хранилищем для обучающих материалов.

На F1, F2, B1, B2 и nginx, ставишь nginx. У F1 и F2 есть один апстрим с двумя серверами (B1, B2). У B1 и B2, тоже один апстрим (Nginx), у NGINX апстримом будет Service , на котором работает WordPress например. Базой для него являются sqlmaster и sqlslave, соответсвенно master-slave

Общая схема вот:

![Schema](https://github.com/Valerych-team/learn/raw/master/img/schema.jpg)
