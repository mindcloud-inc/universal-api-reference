# Update Messenger Subscriber with BotHelp

Updates a subscriber by Facebook Messenger user ID in BotHelp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/subscribers/messenger/:messenger_user_id`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Update Messenger Subscriber](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messenger_user_id` | path | `string` | yes | Facebook Messenger user PSID. |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations array for tags or common subscriber fields. |
