# Get Bot Details with Cloud BOT

Retrieves bot details from Cloud BOT.

## Endpoint

- **Method:** `GET`
- **Path:** `/:public_id/bots/:bot_id`
- **Base URL:** `https://api.c-bot.pro`
- **Official documentation:** [Get Bot Details](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/get-public_id-bots-bot_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `public_id` | path | `string` | yes | Public ID of API |
| `bot_id` | path | `string` | yes | BOT ID |
| `properties` | query | `string` | no | Comma-separated extra bot detail fields |
