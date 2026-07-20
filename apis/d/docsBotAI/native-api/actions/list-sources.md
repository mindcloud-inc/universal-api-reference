# List Sources with DocsBot AI

Retrieves sources from DocsBot AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:teamId/bots/:botId/sources`
- **Base URL:** `https://docsbot.ai/api`
- **Official documentation:** [List Sources](https://docsbot.ai/documentation/developer/source-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The DocsBot bot ID. |
| `teamId` | path | `string` | yes | The DocsBot team ID. |
