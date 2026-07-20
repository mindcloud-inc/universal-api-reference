# Create Presigned Upload URL with DocsBot AI

Retrieves a presigned upload URL from DocsBot AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/teams/:teamId/bots/:botId/upload-url`
- **Base URL:** `https://docsbot.ai/api`
- **Official documentation:** [Create Presigned Upload URL](https://docsbot.ai/documentation/developer/source-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The DocsBot bot ID. |
| `teamId` | path | `string` | yes | The DocsBot team ID. |
