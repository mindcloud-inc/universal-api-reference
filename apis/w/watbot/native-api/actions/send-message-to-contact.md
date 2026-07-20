# Send Message To Contact with Watbot

Creates a new message for a Watbot contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendMessage`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Send Message To Contact](https://docs.watbot.ru/rabota-s-api/otpravit-soobshenie)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | query | `number` | yes | ID контакта. |
| `text` | query | `string` | no | Сообщение. Передайте text, image или file. |
| `image` | query | `string` | no | URL на картинку. |
| `file` | query | `string` | no | URL на файл. |
