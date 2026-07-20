# Update Subscriber with BotHelp

Updates an existing subscriber in BotHelp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/subscribers/:subscriber_id`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Update Subscriber](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations array for tags or common subscriber fields. |
| `subscriber_id` | path | `string` | yes | BotHelp subscriber ID. |
