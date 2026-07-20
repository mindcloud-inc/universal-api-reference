# Set Ysell Status with Watbot

Updates a contact's Ysell status in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/setYsellStatus`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Set Ysell Status](https://docs.watbot.ru/rabota-s-api/kontakty)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | body | `number` | yes | ID контакта. |
| `status` | body | `string` | yes | Статус Ysell, не более 64 символов. Maximum length: 64. |
