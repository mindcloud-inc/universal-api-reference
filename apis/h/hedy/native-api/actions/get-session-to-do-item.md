# Get Session To-Do Item with Hedy

Retrieves a to-do item from a Hedy session.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.hedy.bot/sessions/:sessionId/todos/:todoId`
- **Base URL:** `https://api.hedy.bot`
- **Official documentation:** [Get Session To-Do Item](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Unique identifier of the session. |
| `todoId` | path | `string` | yes | Unique identifier of the to-do item. |
