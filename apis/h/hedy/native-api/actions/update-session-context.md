# Update Session Context with Hedy

Updates an existing session context in Hedy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.hedy.bot/contexts/:contextId`
- **Base URL:** `https://api.hedy.bot`
- **Official documentation:** [Update Session Context](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | New content for the session context. |
| `contextId` | path | `string` | yes | Unique identifier of the session context. |
| `isDefault` | body | `boolean` | no | Set as the default context. |
| `title` | body | `string` | no | New title for the session context. |
