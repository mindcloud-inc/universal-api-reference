# Run Bot with Cloud BOT

Creates a bot job in Cloud BOT.

## Endpoint

- **Method:** `POST`
- **Path:** `/:public_id/bots/:bot_id/jobs`
- **Base URL:** `https://api.c-bot.pro`
- **Official documentation:** [Run Bot](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/post-public_id-bots-bot_id-jobs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `public_id` | path | `string` | yes |
| `bot_id` | path | `string` | yes |
| `timeout` | body | `number` | no |
| `callback_endpoint` | body | `string` | no |
| `callback_tries` | body | `number` | no |
| `input` | body | `object` | no |
