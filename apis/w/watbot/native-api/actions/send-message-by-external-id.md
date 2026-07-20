# Send Message By External ID with Watbot

Creates a new message in Watbot by external contact ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendMessage`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Send Message By External ID](https://docs.watbot.ru/rabota-s-api/otpravit-soobshenie)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | query | `number` | yes | ID бота контакта. |
| `contact_external_id` | query | `string` | yes | Номер телефона или внешний ID контакта в мессенджере. |
| `messenger` | query | `string` | yes | whatsapp, telegram, viber, vk или max. |
| `text` | query | `string` | no | Сообщение. Передайте text, image или file. |
| `image` | query | `string` | no | URL на картинку. |
| `file` | query | `string` | no | URL на файл. |
