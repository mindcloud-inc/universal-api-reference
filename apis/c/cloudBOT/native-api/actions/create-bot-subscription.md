# Create Bot Subscription with Cloud BOT

Creates a bot subscription in Cloud BOT.

## Endpoint

- **Method:** `POST`
- **Path:** `/:public_id/bots/:bot_id/subscriptions`
- **Base URL:** `https://api.c-bot.pro`
- **Official documentation:** [Create Bot Subscription](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/post-public_id-bots-bot_id-subscriptions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `public_id` | path | `string` | yes |
| `bot_id` | path | `string` | yes |
| `event` | body | `string` | yes |
| `callback_type` | body | `string` | yes |
| `callback_endpoint` | body | `string` | yes |
