# Домашнее задание к занятию «Микросервисы: принципы» - Подус Сергей

## Задача 1: API Gateway 

Предложите решение для обеспечения реализации API Gateway. Составьте сравнительную таблицу возможностей различных программных решений. На основе таблицы сделайте выбор решения.

Решение должно соответствовать следующим требованиям:
- маршрутизация запросов к нужному сервису на основе конфигурации,
- возможность проверки аутентификационной информации в запросах,
- обеспечение терминации HTTPS.

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

## Ответ: 

1. 

# Сравнительная таблица возможностей программных решений для API Gateway

| Возможности / Решения   | **Kong**                       | **Amazon API Gateway**         | **NGINX**                      | **Apigee**                     | **Traefik**                    |
|-------------------------|--------------------------------|--------------------------------|--------------------------------|--------------------------------|--------------------------------|
| **Маршрутизация запросов**       | Да                             | Да                             | Да                             | Да                             | Да                             |
| **Проверка аутентификации**      | Да (JWT, OAuth, API-ключи и др.)| Да (AWS IAM, JWT, API-ключи)   | Да (OAuth, JWT, Basic Auth)    | Да (OAuth, API-ключи, SAML и др.) | Да (JWT, OAuth, API-ключи)     |
| **Терминация HTTPS**             | Да                             | Да                             | Да                             | Да                             | Да                             |
| **Легкость интеграции**          | Высокая                        | Высокая (с AWS сервисами)      | Средняя                        | Средняя                        | Высокая                        |
| **Масштабируемость**             | Высокая                        | Высокая                        | Высокая                        | Высокая                        | Высокая                        |
| **Настраиваемость**              | Высокая                        | Средняя                        | Высокая                        | Средняя                        | Высокая                        |
| **Поддержка плагинов/расширений**| Да (большое количество плагинов)| Нет                             | Да (модули и расширения)       | Да (платформенные расширения)   | Да (плагины и middleware)      |
| **Сообщество и поддержка**       | Широкое и активное             | Поддержка от AWS               | Широкое и активное             | Поддержка от Google            | Широкое и активное             |
| **Стоимость**                    | Открытый исходный код (может потребоваться коммерческая поддержка)| Платно (на основе использования)| Открытый исходный код (может потребоваться коммерческая поддержка)| Платно (на основе использования)| Открытый исходный код (может потребоваться коммерческая поддержка)|
| **Документация**                 | Подробная                      | Подробная                      | Подробная                      | Подробная                      | Подробная                      |

# Обоснование выбора

## **Kong**
- **Маршрутизация запросов**: Kong предоставляет гибкие возможности маршрутизации, позволяя настраивать сложные правила маршрутизации на основе конфигурации.
- **Проверка аутентификации**: Поддерживает множество методов аутентификации, включая JWT, OAuth, API-ключи и другие, что делает его гибким для различных сценариев.
- **Терминация HTTPS**: Kong поддерживает терминацию HTTPS, что обеспечивает безопасность соединений.
- **Легкость интеграции**: Имеет высокую степень интеграции с другими сервисами и легко настраивается.
- **Масштабируемость**: Высокая масштабируемость благодаря микросервисной архитектуре.
- **Поддержка плагинов/расширений**: Широкий выбор плагинов позволяет легко добавлять дополнительные функциональности.
- **Сообщество и поддержка**: Активное сообщество и доступность коммерческой поддержки.
- **Стоимость**: Открытый исходный код с возможностью коммерческой поддержки делает его доступным для большинства организаций.

## **Amazon API Gateway**
- **Маршрутизация запросов**: Предоставляет возможности маршрутизации на основе конфигурации с глубокой интеграцией с другими сервисами AWS.
- **Проверка аутентификации**: Поддерживает AWS IAM, JWT и API-ключи, что обеспечивает гибкость в настройке безопасности.
- **Терминация HTTPS**: Встроенная поддержка HTTPS обеспечивает безопасные соединения.
- **Легкость интеграции**: Легко интегрируется с другими AWS сервисами, что делает его удобным для пользователей AWS.
- **Масштабируемость**: Обладает высокой масштабируемостью, автоматическим управлением и масштабированием инфраструктуры.
- **Поддержка плагинов/расширений**: Ограничена по сравнению с другими решениями, но достаточна для большинства сценариев.
- **Сообщество и поддержка**: Поддержка от AWS обеспечивает надежность и доступность ресурсов.
- **Стоимость**: Платформа предоставляет услуги на основе использования, что может быть дорого в масштабах, но эффективно для небольших проектов.

## **NGINX**
- **Маршрутизация запросов**: Обеспечивает мощные и гибкие возможности маршрутизации запросов.
- **Проверка аутентификации**: Поддерживает OAuth, JWT и Basic Auth, обеспечивая широкий спектр опций для безопасности.
- **Терминация HTTPS**: Имеет встроенную поддержку терминации HTTPS.
- **Легкость интеграции**: Интеграция может быть сложнее по сравнению с другими решениями, но возможна благодаря модульной архитектуре.
- **Масштабируемость**: Высокая масштабируемость, подходящая для больших нагрузок.
- **Поддержка плагинов/расширений**: Поддержка модулей и расширений позволяет добавлять необходимую функциональность.
- **Сообщество и поддержка**: Широкое и активное сообщество, а также коммерческая поддержка.
- **Стоимость**: Открытый исходный код, может потребоваться коммерческая поддержка для крупных проектов.

## **Apigee**
- **Маршрутизация запросов**: Обеспечивает гибкие возможности маршрутизации запросов.
- **Проверка аутентификации**: Поддерживает OAuth, API-ключи, SAML и другие методы, что делает его гибким в вопросах безопасности.
- **Терминация HTTPS**: Встроенная поддержка терминации HTTPS.
- **Легкость интеграции**: Интеграция может быть средней сложности, но Apigee предоставляет инструменты для упрощения процесса.
- **Масштабируемость**: Высокая масштабируемость, подходит для больших предприятий.
- **Поддержка плагинов/расширений**: Платформенные расширения обеспечивают необходимую гибкость.
- **Сообщество и поддержка**: Поддержка от Google обеспечивает надежность и обширную документацию.
- **Стоимость**: Платформа предоставляет услуги на основе использования, что может быть дорого для больших проектов, но эффективно для средних и малых.

## **Traefik**
- **Маршрутизация запросов**: Поддерживает гибкие возможности маршрутизации запросов.
- **Проверка аутентификации**: Поддерживает JWT, OAuth, API-ключи, обеспечивая гибкость в настройке безопасности.
- **Терминация HTTPS**: Имеет встроенную поддержку терминации HTTPS.
- **Легкость интеграции**: Легко интегрируется благодаря простой конфигурации и поддержке множества оркестраторов контейнеров.
- **Масштабируемость**: Высокая масштабируемость, особенно в средах с контейнерами.
- **Поддержка плагинов/расширений**: Поддержка плагинов и middleware обеспечивает гибкость и расширяемость.
- **Сообщество и поддержка**: Активное сообщество и поддержка.
- **Стоимость**: Открытый исходный код с возможностью коммерческой поддержки, что делает его доступным для различных организаций.

2. 

# Сравнительная таблица возможностей брокеров сообщений

| Возможности / Решения       | **RabbitMQ**           | **Apache Kafka**        | **ActiveMQ**            | **NATS**                | **Redis Streams**       |
|-----------------------------|------------------------|-------------------------|-------------------------|-------------------------|-------------------------|
| **Кластеризация**           | Да                     | Да                      | Да                      | Да                      | Да                      |
| **Хранение сообщений на диске** | Да                     | Да                      | Да                      | Нет                     | Да                      |
| **Высокая скорость работы** | Высокая                | Очень высокая           | Средняя                 | Очень высокая           | Высокая                 |
| **Поддержка различных форматов сообщений** | Да                     | Да                      | Да                      | Да                      | Да                      |
| **Разделение прав доступа** | Да                     | Да                      | Да                      | Да                      | Да                      |
| **Простота эксплуатации**   | Средняя                | Средняя                 | Средняя                 | Высокая                 | Высокая                 |
| **Поддержка различных протоколов** | AMQP, STOMP, MQTT     | Нет (только собственный)| AMQP, MQTT, OpenWire    | NATS, MQTT              | RESP                    |
| **Масштабируемость**        | Средняя                | Очень высокая           | Средняя                 | Очень высокая           | Высокая                 |
| **Сообщество и поддержка**  | Активное               | Очень активное          | Активное                | Активное                | Активное                |
| **Документация**            | Подробная              | Подробная               | Подробная               | Подробная               | Подробная               |

# Обоснование выбора

## **RabbitMQ**
- **Кластеризация и хранение сообщений на диске**: Обеспечивает высокую доступность и надёжность.
- **Скорость работы и протоколы**: Высокая скорость и поддержка многих протоколов.
- **Разделение прав доступа**: Гибкие возможности.

## **Apache Kafka**
- **Кластеризация и хранение сообщений на диске**: Высокая надёжность.
- **Скорость работы и масштабируемость**: Очень высокая скорость и пропускная способность.
- **Поддержка форматов сообщений**: Гибкая сериализация (Avro, JSON, Protobuf).
- **Разделение прав доступа**: Тонкая настройка.

## **ActiveMQ**
- **Кластеризация и хранение сообщений на диске**: Поддержка высокой доступности.
- **Скорость работы и протоколы**: Средняя скорость, поддержка AMQP, MQTT, OpenWire.

## **NATS**
- **Кластеризация и скорость работы**: Высокая доступность и очень высокая скорость.
- **Простота эксплуатации**: Лёгкость настройки.

## **Redis Streams**
- **Кластеризация и хранение сообщений на диске**: Высокая доступность.
- **Скорость работы и простота эксплуатации**: Высокая скорость и лёгкость администрирования.

# Вывод

**Apache Kafka** является наиболее подходящим решением благодаря высокой скорости работы, поддержке кластеризации, хранению сообщений на диске, разделению прав доступа и отличной масштабируемости.
