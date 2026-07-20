# Get Source with DocsBot AI

Retrieves a source from DocsBot AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:teamId/bots/:botId/sources/:sourceId`
- **Base URL:** `https://docsbot.ai/api`
- **Official documentation:** [Get Source](https://docsbot.ai/documentation/developer/source-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The DocsBot bot ID. |
| `sourceId` | path | `string` | yes | The DocsBot source ID. |
| `teamId` | path | `string` | yes | The DocsBot team ID. |
