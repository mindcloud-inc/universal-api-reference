# List Contacts with Watbot

Retrieves contacts from Watbot.

## Endpoint

- **Method:** `GET`
- **Path:** `/getContacts`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [List Contacts](https://docs.watbot.ru/rabota-s-api/kontakty)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | query | `number` | no | Фильтр по дате создания контакта в формате Unix Time. |
| `date_to` | query | `number` | no | Фильтр по дате создания контакта в формате Unix Time. |
| `bot_id` | query | `number` | no | ID бота. |
