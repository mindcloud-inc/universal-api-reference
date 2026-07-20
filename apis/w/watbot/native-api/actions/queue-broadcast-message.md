# Queue Broadcast Message with Watbot

Queues a broadcast message in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendMessageToQueue`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Queue Broadcast Message](https://docs.watbot.ru/rabota-s-api/rassylka)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_id` | body | `string` | yes | Уникальный ID сообщения. |
| `text` | body | `string` | yes | Текст сообщения. |
| `contact_id` | body | `number` | no | ID контакта Watbot. Нужен, когда bitrix_contact_id и phone не переданы. |
| `bitrix_contact_id` | body | `number` | no | ID контакта Битрикса. Нужен, когда contact_id и phone не переданы. |
| `phone` | body | `string` | no | Номер телефона получателя. Нужен, когда contact_id и bitrix_contact_id не переданы. |
