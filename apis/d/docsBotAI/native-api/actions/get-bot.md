# Get Bot with DocsBot AI

Retrieves a bot from DocsBot AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:teamId/bots/:botId`
- **Base URL:** `https://docsbot.ai/api`
- **Official documentation:** [Get Bot](https://docsbot.ai/documentation/developer/bot-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The DocsBot bot ID. |
| `teamId` | path | `string` | yes | The DocsBot team ID. |
