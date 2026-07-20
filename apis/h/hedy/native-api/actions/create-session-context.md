# Create Session Context with Hedy

Creates a new session context in Hedy.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.hedy.bot/contexts`
- **Base URL:** `https://api.hedy.bot`
- **Official documentation:** [Create Session Context](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Content or instructions for the session context. |
| `isDefault` | body | `boolean` | no | Set as the default context for new sessions. |
| `title` | body | `string` | yes | Title for the session context. |
