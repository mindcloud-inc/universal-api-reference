# Create Or Update Telegram Contact with LEADTEX

Creates or updates a Telegram contact in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/createOrUpdateContact?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Create Or Update Telegram Contact](https://docs.leadteh.ru/rabota-s-api/kontakty/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | query | `number` | yes | ID of the bot to create or update the contact in. |
| `messenger` | query | `string` | yes | Use telegram for this action. |
| `name` | query | `string` | yes | Contact name. |
| `telegram_id` | query | `number` | yes | Telegram user ID. |
