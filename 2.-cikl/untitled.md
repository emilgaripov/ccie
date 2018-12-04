# 2.3 Protocol Independent IPv4 Routing. Static routing.

## Темы:

{% hint style="info" %}
_Название тем, рассматриваемых в данной главе._
{% endhint %}

* Static Routing
* Route Recursion
* Egress Interface vs. Next Hop Static
* Routing Default Routing

## ❓ Вопросы:

{% hint style="info" %}
_Вопросы для самостоятельной работы и поиска ответов._
{% endhint %}

1. Дайте понятие статическому маршруту. 
2. Будет ли статический маршрут с префиксом /24 иметь преимущество перед маршрутом, имеющим префикс /32? Дайте объяснение.
3. Дайте понятие рекурсии.
4. Что произойдет, если маршрутизатор не сможет найти исходящий интерфейс по отношению к заданному маршруту?
5. Что означает локальный маршрут\(L\)? Дайте объяснение.
6. Какую административную дистанцию имеет статический маршрут?

## 📍 Лабораторная работа:

1. В этой лабораторной работе используется [физическая](https://ccie.gitbook.io/ccie/topology#physic) и [логическая](https://ccie.gitbook.io/ccie/topology#logic) топологии проекта.
2. Загрузить [начальную конфигурацию](https://drive.google.com/open?id=0ByVf6yfX4EBfVmhGSFBxLU1LWm8) для SW1,SW2, SW3, SW4, R2, R3, R4, R5.
3. На интерфейсе E0/1.235 R2 задать ip 188.1.235.2/24, на интерфейсе E0/1.235 R3 задать ip 188.1.235.3/24, на интерфейсе E0/1.235 R5 задать ip 188.1.235.5/24, на интерфейсе E0/1.34 R3 задать ip 188.1.34.3/24, на интерфейсе E0/1.34 R4 задать ip 188.1.34.4/24.
4. Включить физические интерфейсы E0/1 на этих маршрутизаторах.
5. Проверить соединение между маршрутизаторами, отправив пинг на ip адреса настроенных интерфейсов.
6. Настроить на R3 статический маршрут к loopback интерфейсу R5, используя nexthop адрес R5 188.1.235.5/24.
7. Настроить на R3 статический маршрут к loopback интерфейсу R2, используя исходящий интерфейс E0/1.235
8. Проверить командой sh ip route настройки маршрутов на R3.
9. Отправить пинг с R3 на ip адреса loopback интерфейсов R2 и R5.
10. Настроить маршрут по умолчанию на R2, используя исходящий интерфейс E0/1.235.
11. Настроить маршрут по умолчанию на R5, используя исходящий интерфейс E0/1.235 и nexthop адрес R3 188.1.235.3/24.
12. Отправить пинг с R2 на ip адрес loopback интерфейса R5.

{% hint style="info" %}
_Если у вас возникли вопросы по заданию, пройдите по_ [_ссылке_ ](http://ccie.linkmeup.ru/2016/04/22/laboratornaya-rabota-po-teme-9-static-routing/)_и вы попадете в раздел комментариев к заданию на сайте_ [_ccie.linkmeup.ru_](http://ccie.linkmeup.ru/)_. Возможно участники проекта уже ответили на них._
{% endhint %}

## 📌 Материалы по теме для самостоятельного изучения:

Ссылки на сайт www.cisco.com:  
[http://www.cisco.com/c/en/us/td/docs/ios-xml/ios/iproute\_pi/configuration/15-mt/iri-15-mt-book/iri-iprouting.html](http://www.cisco.com/c/en/us/td/docs/ios-xml/ios/iproute_pi/configuration/15-mt/iri-15-mt-book/iri-iprouting.html)

[http://www.cisco.com/c/en/us/support/docs/dial-access/floating-static-route/118263-technote-nexthop-00.html](http://www.cisco.com/c/en/us/support/docs/dial-access/floating-static-route/118263-technote-nexthop-00.html)  
Как найти документ:  
www.cisco.com→support→documentation → IOS and NX-OS Software→IOS→IOS Software Release 15M&T→IOS 15.3M&T→Cisco IOS 15.5M&T→Configuration Guides→IP Routing: Protocol-Independent Configuration Guide, Cisco IOS Release 15M&T → Configuring IP Routing Protocol-Independent Features  
Ссылки на книгу/главу:  
CCIE Routing and Switching v5.0 Official Cert Guide Volume 1, Chapter 6

Ссылка на сайт www.xgu.ru:  
[http://goo.gl/2Dnn0i](http://goo.gl/2Dnn0i)

{% hint style="info" %}
 _Если у вас возникли вопросы по материалам, пройдите по_ [_ссылке_ ](http://ccie.linkmeup.ru/2016/04/22/materialy-po-tsiklu-2-teme-9/)_и вы попадете в раздел комментариев к материалам на сайте_ [_ccie.linkmeup.ru_](http://ccie.linkmeup.ru/)_. Возможно участники проекта уже ответили на них._
{% endhint %}

