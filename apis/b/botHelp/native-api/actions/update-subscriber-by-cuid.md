# Update Subscriber By CUID with BotHelp

Updates a subscriber by CUID in BotHelp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/subscribers/cuid/:subscriber_cuid`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Update Subscriber By CUID](https://main.bothelp.io/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations array for tags or common subscriber fields. |
| `subscriber_cuid` | path | `string` | yes | BotHelp subscriber CUID. |
