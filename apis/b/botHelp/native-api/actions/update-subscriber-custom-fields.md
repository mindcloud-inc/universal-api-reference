# Update Subscriber Custom Fields with BotHelp

Updates subscriber custom fields in BotHelp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/subscribers/:subscriber_id/customFields`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Update Subscriber Custom Fields](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations array for custom field replacements. |
| `subscriber_id` | path | `string` | yes | BotHelp subscriber ID. |
