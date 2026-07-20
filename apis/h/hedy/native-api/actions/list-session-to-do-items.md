# List Session To-Do Items with Hedy

Retrieves to-do items for a Hedy session.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.hedy.bot/sessions/:sessionId/todos`
- **Base URL:** `https://api.hedy.bot`
- **Official documentation:** [List Session To-Do Items](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | query | `string` | no | Set to zapier to receive a flat array response suitable for Zapier triggers. |
| `sessionId` | path | `string` | yes | Unique identifier of the session. |
