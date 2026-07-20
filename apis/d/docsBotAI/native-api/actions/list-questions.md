# List Questions with DocsBot AI

Retrieves questions from DocsBot AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:teamId/bots/:botId/questions`
- **Base URL:** `https://docsbot.ai/api`
- **Official documentation:** [List Questions](https://docsbot.ai/documentation/developer/questions-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The DocsBot bot ID. |
| `teamId` | path | `string` | yes | The DocsBot team ID. |
