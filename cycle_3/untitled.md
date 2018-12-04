# 3.4 Qos. MQC Classification, Marking, BW, LLQ

## Темы:

{% hint style="info" %}
 _Название тем, рассматриваемых в данной главе._
{% endhint %}

* MQC Classification and Marking
* MQC Bandwidth Reservations and CBWFQ
* MQC Bandwidth Percent
* MQC LLQ and Remaining Bandwidth Reservations

##  ❓ Вопросы:

{% hint style="info" %}
 _Вопросы для самостоятельной работы и поиска ответов._
{% endhint %}

1. Где происходит классификация трафика?
2. Какими путями происходит классификация трафика?
3. Назовите типы маркировки трафика. Дайте объяснение.
4. Дайте понятие DSCP и IP precedence.
5. Какая маркировка применяется на только транковых линках?
6. Чем отличается EF от AF?
7. Дайте расширенное описание AF.
8. Дать понятие о Class Selector.
9. Дайте понятия о типах MQC QoS.
10. Объясните шаги конфигурирования MQC.
11. Назовите критерии классификации MQC.

## 📍 Лабораторная работа:

 В этой лабораторной работе используется [физическая](https://ccie.gitbook.io/ccie/topology#physic) и [логическая](https://ccie.gitbook.io/ccie/topology#logic) топологии проекта.

**Задание \#1 для лабораторной:**  
1. Загрузить[ начальную конфигурацию](https://drive.google.com/open?id=0B8TdfSzCKkaxZHpJcWVYaDVuYnM) на SW1, SW2, SW3, R3, R2, R5  
2. На R2 создать пользователя CCIEadmin с паролем CCIEinaYEAR. Разрешить подключение по телнет.  
3. На всех маршрутизаторах настроить протокол маршрутизации RIP версии 2 с анонсированием сети 188.1.0.0. Убрать автосуммирование маршрутов.  
4. На маршрутизаторе R3 создать class-map TELNET, Policy map R2 и классифицировать трафик по протоколу телнет, идущий через исходящий интерфейс к R2.  
5. Проверить настройки

**Задание \#2 для лабораторной:**  
1. Загрузить [начальную конфигурацию](https://drive.google.com/open?id=0B8TdfSzCKkaxWTRhSG4tbGU4QTA) R1, R2.  
2. На маршрутизаторе R1 настроить политику передачи трафика, используя для настройки подход HQF. Политику назвать HQF. Создать отдельные class-map для протоколов Telnet, HTTP, SMTP.  
3. Для Telnet установить полосу пропускания в 10%, для SMTP 20%, для HTTP 30%  
4.  Определить для HTTP трафика правило выстраивание очереди по каждому потоку \(flow\) отдельно.  
5. Проверить настройки.

**Задание \#3 для лабораторной:**  
1. Загрузить [начальную конфигурацию](https://drive.google.com/open?id=0B8TdfSzCKkaxdk1oeWlqSmZjZFU) R1, R2.  
2. На маршрутизаторе R1 настроить политику передачи трафика по технологии LLQ по умолчанию и названием LLQ. Создать отдельные class-map для протоколов Telnet, HTTP, SMTP и RTP с соответствующими названиями TELNET, HTTP, SMTP, VOIP.  
3. RTP должен быть самым приоритетным трафиком. Для Telnet установить полосу пропускания в 10%, для SMTP 20%, для HTTP 30% оставшейся полосы пропускания.  
4. На стороне R2 полоса пропускания принимает трафик только на скорости 25мб/с. На R1 настроить полосу пропускания в соответствии со скоростью приема трафика на R2, чтобы распределение полосы в политике LLQ, делалось на основе этого значения.

Проверить настройки.

{% hint style="info" %}
_Если у вас возникли вопросы по заданию, пройдите по_ [_ссылке_ ](http://ccie.linkmeup.ru/2016/05/16/laboratornaya-rabota-po-teme-16-qos-6-7-6-10/)_и вы попадете в раздел комментариев к заданию на сайте_ [_ccie.linkmeup.ru_](http://ccie.linkmeup.ru/)_. Возможно участники проекта уже ответили на них._
{% endhint %}

## 📌 Материалы по теме для самостоятельного изучения:



**Ссылки на сайт** [**www.cisco.com**](http://www.cisco.com)**:**

* [http://www.cisco.com/c/en/us/td/docs/ios-xml/ios/qos/config\_library/15-mt/qos-15-mt-library.html](http://www.cisco.com/c/en/us/td/docs/ios-xml/ios/qos/config_library/15-mt/qos-15-mt-library.html)
* [http://www.cisco.com/c/en/us/td/docs/ios-xml/ios/qos\_conmgt/configuration/15-mt/qos-conmgt-15-mt-book.html](http://www.cisco.com/c/en/us/td/docs/ios-xml/ios/qos_conmgt/configuration/15-mt/qos-conmgt-15-mt-book.html)

**Как найти документ:**

* Cisco.com&gt;Documentation&gt; Products &gt;IOS and NX-OS SoftwareIOS&gt;IOS Software Release 15.42 Family&gt;IOS Software Releases 15.4 Mainline&gt; Quality of Service Solutions Configuration Guide Library, Cisco IOS Release 15M&T
* Cisco.com&gt;Documentation&gt; Products &gt;IOS and NX-OS SoftwareIOS&gt;IOS Software Release 15.42 Family&gt;IOS Software Releases 15.4 Mainline&gt; Quality of Service Solutions Configuration Guide Library, Cisco IOS Release 15M&T&gt;QoS: Congestion Management Configuration Guide, Cisco IOS Release 15M&T

**Ссылки на книгу/главу:**

* Deploing QOS for cisco IP and next generation networks

**Ссылки на сайт xgu.ru:**

* [http://www.xgu.ru/wiki/QoS\_%D0%B2\_Cisco](http://www.xgu.ru/wiki/QoS_%D0%B2_Cisco)
* [http://xgu.ru/wiki/QoS](http://xgu.ru/wiki/QoS)

**Другие ссылки:**

* [http://blog.ine.com/2008/08/17/insights-on-cbwfq/](http://blog.ine.com/2008/08/17/insights-on-cbwfq/)

{% hint style="info" %}
_Если у вас возникли вопросы по материалам, пройдите по_ _ссылке_ _и вы попадете в раздел комментариев к материалам на сайте_ [_ccie.linkmeup.ru_](http://ccie.linkmeup.ru/)_. Возможно участники проекта уже ответили на них._
{% endhint %}

