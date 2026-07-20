# Attach Tag To Contact with Watbot

Attaches a tag to a contact in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/attachTagToContact`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Attach Tag To Contact](https://docs.watbot.ru/rabota-s-api/kontakty/tegi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | ID контакта. |
| `name` | body | `string` | yes | Имя тега. |
