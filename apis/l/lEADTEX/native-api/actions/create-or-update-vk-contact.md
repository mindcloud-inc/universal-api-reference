# Create Or Update VK Contact with LEADTEX

Creates or updates a VK contact in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/createOrUpdateContact?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Create Or Update VK Contact](https://docs.leadteh.ru/rabota-s-api/kontakty/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | query | `number` | yes | ID of the bot to create or update the contact in. |
| `messenger` | query | `string` | yes | Use vk for this action. |
| `name` | query | `string` | yes | Contact name. |
| `vk_id` | query | `number` | yes | VK user ID. |
