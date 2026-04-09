# Задание 2. Проектирование API

## Описание
API используется для получения списка партнёрских магазинов.

---

## Пример запроса

```http
GET /api/v1/partner-stores
Host: api.petrushka-green.ru
Accept: application/json
Authorization: Bearer <access_token>

---

```md
## Пример запроса

{
  "data": [
    {
      "id": 1,
      "name": "METRO",
      "logo_url": "https://cdn.petrushka-green.ru/metro.png",
      "delivery": {
        "type": "time_interval",
        "text": "Ближайшая доставка сегодня 21:00–23:00",
        "start_time": "21:00",
        "end_time": "23:00"
      },
      "external_url": "https://metro.ru"
    },
    {
      "id": 2,
      "name": "ВкусВилл",
      "logo_url": "https://cdn.petrushka-green.ru/vkusvill.png",
      "delivery": {
        "type": "fast_delivery",
        "text": "Быстрая доставка от 20 до 60 минут",
        "min_minutes": 20,
        "max_minutes": 60
      },
      "external_url": "https://vkusvill.ru"
    }
  ],
  "meta": {
    "count": 2
  }
}
