
# Домашнее задание к занятию «Микросервисы: принципы»

Вы работаете в крупной компании, которая строит систему на основе микросервисной архитектуры.
Вам как DevOps-специалисту необходимо выдвинуть предложение по организации инфраструктуры для разработки и эксплуатации.

## Задача 1: API Gateway 

Предложите решение для обеспечения реализации API Gateway. Составьте сравнительную таблицу возможностей различных программных решений. На основе таблицы сделайте выбор решения.

Решение должно соответствовать следующим требованиям:
- маршрутизация запросов к нужному сервису на основе конфигурации,
- возможность проверки аутентификационной информации в запросах,
- обеспечение терминации HTTPS.

Обоснуйте свой выбор.

Для реализации API Gateway, соответствующего указанным требованиям, можно рассмотреть следующие популярные решения:
1) NGINX (+ Lua или модули)

2) Kong

3) Traefik

4) Envoy

5) Apache APISIX

Я бы выбрал для реализации API Gateway - Kong

Обоснование выбора:

1) Маршрутизация
    Kong предоставляет гибкую маршрутизацию на основе URL, заголовков и методов HTTP, что соответствует требованию.

2) Аутентификация
    Поддерживает JWT, OAuth2, API-ключи и другие методы аутентификации, что удобно для проверки запросов.

3) HTTPS-терминация
    Kong легко настраивается для терминации HTTPS с поддержкой Let’s Encrypt.

4) Дополнительные преимущества

- Модульность (плагины для логирования, rate limiting, мониторинга).

- Интеграция с OpenAPI/Swagger.

- Поддержка микросервисных архитектур.

## Задача 2: Брокер сообщений

Составьте таблицу возможностей различных брокеров сообщений. На основе таблицы сделайте обоснованный выбор решения.

Решение должно соответствовать следующим требованиям:
- поддержка кластеризации для обеспечения надёжности,
- хранение сообщений на диске в процессе доставки,
- высокая скорость работы,
- поддержка различных форматов сообщений,
- разделение прав доступа к различным потокам сообщений,
- простота эксплуатации.

Обоснуйте свой выбор.

## Задача 2: Брокер сообщений

Составьте таблицу возможностей различных брокеров сообщений. На основе таблицы сделайте обоснованный выбор решения.

Решение должно соответствовать следующим требованиям:
- поддержка кластеризации для обеспечения надёжности,
- хранение сообщений на диске в процессе доставки,
- высокая скорость работы,
- поддержка различных форматов сообщений,
- разделение прав доступа к различным потокам сообщений,
- простота эксплуатации.

Обоснуйте свой выбор.

|Брокер сообщений|Поддержка кластеризации для обеспечения надежности|Хранение сообщений на диске в процессе доставки|Высокая скорость работы|Поддержка различных форматов сообщений|Разделение прав доступа к различным потокам сообщений|
|---------|---|---|---|---|---|
|RabbitMQ | + | + | - | + | + |
|Apache Kafka    | + | + | + | + | + |
|Redis    | + | - | + | + | + |

Вывод: Kafka поддерживает бОльший функционал из требований, выбор очевиден.
