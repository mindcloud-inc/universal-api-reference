# Create Or Update Contact with Watbot

Finds a contact in Watbot, or creates one if no match is found.

## Endpoint

- **Method:** `POST`
- **Path:** `/createOrUpdateContact`
- **Base URL:** `https://watbot.ru/api/v1`
- **Official documentation:** [Create Or Update Contact](https://docs.watbot.ru/rabota-s-api/kontakty)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | body | `number` | yes | ID бота. |
| `messenger` | body | `string` | yes | Тип мессенджера. Поддерживаются whatsapp, telegram, viber и vk. |
| `name` | body | `string` | yes | Имя контакта. |
| `phone` | body | `string` | no | Номер телефона в международном формате. Обязателен для messenger=whatsapp. |
| `telegram_id` | body | `number` | no | ID пользователя в Telegram. Обязателен для Telegram. |
| `telegram_username` | body | `string` | no | Username пользователя Telegram. |
| `viber_id` | body | `string` | no | ID пользователя в Viber. Обязателен для Viber. |
| `vk_id` | body | `number` | no | ID пользователя во ВКонтакте. Обязателен для VK. |
| `email` | body | `string` | no | Email контакта. |
| `address` | body | `string` | no | Адрес контакта. |
| `tags[]` | body | `array<string>` | no | Массив тегов контакта. |
