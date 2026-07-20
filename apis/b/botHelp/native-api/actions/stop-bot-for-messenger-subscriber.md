# Stop Bot For Messenger Subscriber with BotHelp

Stops a bot for a subscriber by Facebook Messenger user ID in BotHelp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/subscribers/messenger/:messenger_user_id/bot`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Stop Bot For Messenger Subscriber](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botReferral` | query | `string` | no | Optional bot referral to stop. |
| `messenger_user_id` | path | `string` | yes | Facebook Messenger user PSID. |
