# Retry Source Indexing with DocsBot AI

Updates a source to retry indexing in DocsBot AI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/teams/:teamId/bots/:botId/sources/:sourceId`
- **Base URL:** `https://docsbot.ai/api`
- **Official documentation:** [Retry Source Indexing](https://docsbot.ai/documentation/developer/source-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The DocsBot bot ID. |
| `sourceId` | path | `string` | yes | The DocsBot source ID. |
| `teamId` | path | `string` | yes | The DocsBot team ID. |
