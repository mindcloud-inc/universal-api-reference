# Get Session Context with Hedy

Retrieves a session context from Hedy.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.hedy.bot/contexts/:contextId`
- **Base URL:** `https://api.hedy.bot`
- **Official documentation:** [Get Session Context](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contextId` | path | `string` | yes | Unique identifier of the session context. |
| `format` | query | `string` | no | Set to zapier to receive a flat response. |
