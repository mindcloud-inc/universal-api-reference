# Send Message To WhatsApp with Watbot

Creates a new WhatsApp message in Watbot.

## Endpoint

- **Method:** `POST`
- **Path:** `/sendMessageToWhatsApp`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Send Message To WhatsApp](https://docs.watbot.ru/rabota-s-api/otpravit-soobshenie)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | body | `number` | yes | ID бота контакта. |
| `phone` | body | `string` | yes | Номер телефона. |
| `text` | body | `string` | yes | Сообщение. |
| `name` | body | `string` | no | Имя контакта. Передавайте при первом сообщении на этот номер. |
