# List Sessions with Hedy

Retrieves session records from Hedy.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.hedy.bot/sessions`
- **Base URL:** `https://api.hedy.bot`
- **Official documentation:** [List Sessions](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of sessions to return per page. |
| `format` | query | `string` | no | Set to zapier to return a flat array response. |
