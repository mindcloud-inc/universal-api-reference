# Delete Bot with DocsBot AI

Deletes an existing bot from DocsBot AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/teams/:teamId/bots/:botId`
- **Base URL:** `https://docsbot.ai/api`
- **Official documentation:** [Delete Bot](https://docsbot.ai/documentation/developer/bot-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The DocsBot bot ID. |
| `teamId` | path | `string` | yes | The DocsBot team ID. |
