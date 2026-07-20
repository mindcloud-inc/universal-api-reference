# Create Source with DocsBot AI

Creates a new source in DocsBot AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/:teamId/bots/:botId/sources`
- **Base URL:** `https://docsbot.ai/api`
- **Official documentation:** [Create Source](https://docsbot.ai/documentation/developer/source-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The DocsBot bot ID. |
| `teamId` | path | `string` | yes | The DocsBot team ID. |
