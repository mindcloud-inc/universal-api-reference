# Update Subscriber Custom Fields By CUID with BotHelp

Updates subscriber custom fields by CUID in BotHelp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/subscribers/cuid/:subscriber_cuid/customFields`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Update Subscriber Custom Fields By CUID](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations array for custom field replacements. |
| `subscriber_cuid` | path | `string` | yes | BotHelp subscriber CUID. |
