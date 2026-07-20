# Delete Source with DocsBot AI

Deletes an existing source from DocsBot AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/teams/:teamId/bots/:botId/sources/:sourceId`
- **Base URL:** `https://docsbot.ai/api`
- **Official documentation:** [Delete Source](https://docsbot.ai/documentation/developer/source-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The DocsBot bot ID. |
| `sourceId` | path | `string` | yes | The DocsBot source ID. |
| `teamId` | path | `string` | yes | The DocsBot team ID. |
