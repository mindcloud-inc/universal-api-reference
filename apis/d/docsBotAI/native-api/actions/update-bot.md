# Update Bot with DocsBot AI

Updates an existing bot in DocsBot AI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/teams/:teamId/bots/:botId`
- **Base URL:** `https://docsbot.ai/api`
- **Official documentation:** [Update Bot](https://docsbot.ai/documentation/developer/bot-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The DocsBot bot ID. |
| `teamId` | path | `string` | yes | The DocsBot team ID. |
