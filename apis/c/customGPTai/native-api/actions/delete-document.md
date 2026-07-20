# Delete Document with CustomGPT.ai

Deletes a document from a CustomGPT.ai agent.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId/pages/:pageId`
- **Base URL:** `https://app.customgpt.ai/api/v1`
- **Official documentation:** [Delete Document](https://docs.customgpt.ai/reference/delete_api-v1-projects-projectid-pages-pageid-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project ID of the agent. |
| `pageId` | path | `number` | yes | The document page ID. |
