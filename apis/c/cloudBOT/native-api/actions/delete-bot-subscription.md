# Delete Bot Subscription with Cloud BOT

Deletes a bot subscription from Cloud BOT.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/:public_id/bots/:bot_id/subscriptions/:subscribe_id`
- **Base URL:** `https://api.c-bot.pro`
- **Official documentation:** [Delete Bot Subscription](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/delete-public_id-bots-bot_id-subscriptions-subscribe_id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `public_id` | path | `string` | yes |
| `bot_id` | path | `string` | yes |
| `subscribe_id` | path | `number` | yes |
