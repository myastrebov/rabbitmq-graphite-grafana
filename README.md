# Настройка мониторинга для RabbitMQ

## Getting start

``docker compose up -d``
- Заходим в графану
- Добавляем dataSource graphite http://graphite:80
- Создаём дашборд с метрриками rabbitMq

## RabbitMQ

адрес: http://localhost:15672

login: `user`

Password: `password`

## Graphite

адрес: http://localhost:80

## Grafana

адрес: http://localhost:3000

login: `admin`

Password: `admin`


Telegraf подключается к RabbitMQ через management console и забирает с указанной периодичностью метрики, затем отправляет их в Graphite, который подключен как dataSource в Grafana
