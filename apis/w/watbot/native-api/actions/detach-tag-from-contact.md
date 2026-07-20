# Detach Tag From Contact with Watbot

Detaches a tag from a contact in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/detachTagFromContact`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Detach Tag From Contact](https://docs.watbot.ru/rabota-s-api/kontakty/tegi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | ID контакта. |
| `name` | body | `string` | yes | Имя тега. |
