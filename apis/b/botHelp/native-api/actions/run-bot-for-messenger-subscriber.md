# Run Bot For Messenger Subscriber with BotHelp

Runs a bot for a subscriber by Facebook Messenger user ID in BotHelp.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/subscribers/messenger/:messenger_user_id/bot`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Run Bot For Messenger Subscriber](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botReferral` | body | `string` | yes | Bot referral to start for the subscriber. |
| `messenger_user_id` | path | `string` | yes | Facebook Messenger user PSID. |
| `stepReferral` | body | `string` | no | Optional bot step referral to start at a specific step. |
