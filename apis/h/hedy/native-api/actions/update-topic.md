# Update Topic with Hedy

Updates an existing topic in Hedy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.hedy.bot/topics/:topicId`
- **Base URL:** `https://api.hedy.bot`
- **Official documentation:** [Update Topic](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | New hex color code. |
| `description` | body | `string` | no | New description for the topic. |
| `iconName` | body | `string` | no | New material icon name. |
| `name` | body | `string` | no | New name for the topic. |
| `topicContext` | body | `string` | no | New custom instructions for this topic. |
| `topicId` | path | `string` | yes | Unique identifier of the topic. |
