# ESP8266 WebSocket MQTT Broker for IoTmanager

Библиотека для прямого подключения IoTmanager'a к ESP8266 через WebSocket без посредников, таких как cloudmqtt.com. ESP выступает в качестве точки доступа Wi-Fi и выполняет функции MQTT брокера, таким образом для общения со смартфоном не нужен доступ в интернет.

## Состав

- [MQTTbroker.h] имитация работы брокера для нескольких клиентов (с контролем подписок) 
- [MQTTbroker_lite.h] только для прямого общения с IoTmanager (без контроля подписок)

## Примеры

В библиотеки есть несколько примеров работы как с lite версией, так и с полной. 
См. Файл -> Примеры -> MQTTbroker

## Ограничения

- Брокер использует версию 3.1.1 протокола MQTT
- Используется WebSocket без SSL/TLS
- Соединяется только с использованием библиотеки Paho.js
- Публикации возможны только с QoS = 0 

## Поддерживаемое железо

Писалось и тестировалось под ESP8266

## Известные проблемы

Не получается использовать стили в конфиге, например {"descrStyle":"font-size:20px;"}, IoTmanager спотыкается и уходит в рекконект.

## Версии

v.0.1.0 - минимально работающая версия