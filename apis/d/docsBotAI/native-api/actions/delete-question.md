# Delete Question with DocsBot AI

Deletes a question from DocsBot AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/teams/:teamId/bots/:botId/questions/:questionId`
- **Base URL:** `https://docsbot.ai/api`
- **Official documentation:** [Delete Question](https://docsbot.ai/documentation/developer/questions-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The DocsBot bot ID. |
| `questionId` | path | `string` | yes | The DocsBot question ID. |
| `teamId` | path | `string` | yes | The DocsBot team ID. |
