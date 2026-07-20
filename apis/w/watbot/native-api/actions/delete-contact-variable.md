# Delete Contact Variable with Watbot

Deletes a contact variable from Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/deleteContactVariable`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Delete Contact Variable](https://docs.watbot.ru/rabota-s-api/kontakty/polzovatelskie-peremennye)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | no | ID переменной. Обязательно, когда name не передан. |
| `contact_id` | query | `number` | yes | ID контакта. |
| `name` | query | `string` | no | Имя переменной. Обязательно, когда id не передан. |
