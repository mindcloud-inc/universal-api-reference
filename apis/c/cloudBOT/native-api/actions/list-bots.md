# List Bots with Cloud BOT

Retrieves bots from Cloud BOT.

## Endpoint

- **Method:** `GET`
- **Path:** `/:public_id/bots`
- **Base URL:** `https://api.c-bot.pro`
- **Official documentation:** [List Bots](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/get-public_id-bots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `public_id` | path | `string` | yes | Public ID of API |
| `properties` | query | `string` | no | Comma-separated extra bot fields |
