# Create Topic with Hedy

Creates a new topic in Hedy.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.hedy.bot/topics`
- **Base URL:** `https://api.hedy.bot`
- **Official documentation:** [Create Topic](https://app.swaggerhub.com/apis-docs/HedyAI/hedy-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | Hex color code. |
| `description` | body | `string` | no | Description of the topic. |
| `iconName` | body | `string` | no | Material icon name. |
| `name` | body | `string` | yes | Name of the topic. |
| `topicContext` | body | `string` | no | Custom instructions for this topic. |
