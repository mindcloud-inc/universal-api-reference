# Reindex Document with CustomGPT.ai

Reindexes a URL-based document in a CustomGPT.ai agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/pages/:pageId/reindex`
- **Base URL:** `https://app.customgpt.ai/api/v1`
- **Official documentation:** [Reindex Document](https://docs.customgpt.ai/reference/post_api-v1-projects-projectid-pages-pageid-reindex-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project ID of the agent. |
| `pageId` | path | `number` | yes | The document page ID. |
