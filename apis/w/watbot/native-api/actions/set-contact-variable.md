# Set Contact Variable with Watbot

Sets a contact variable in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/setContactVariable`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Set Contact Variable](https://docs.watbot.ru/rabota-s-api/kontakty/polzovatelskie-peremennye)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID контакта. |
| `name` | query | `string` | yes | Имя переменной. |
| `value` | query | `string` | yes | Значение переменной. |
| `deletable` | query | `number` | no | 0 — не удалять после заявки, 1 — удалять после заявки. |
