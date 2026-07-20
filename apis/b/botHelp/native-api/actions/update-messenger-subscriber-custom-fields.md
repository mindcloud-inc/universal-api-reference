# Update Messenger Subscriber Custom Fields with BotHelp

Updates subscriber custom fields by Facebook Messenger user ID in BotHelp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/subscribers/messenger/:messenger_user_id/custom-fields`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Update Messenger Subscriber Custom Fields](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messenger_user_id` | path | `string` | yes | Facebook Messenger user PSID. |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations array for custom field replacements. |
