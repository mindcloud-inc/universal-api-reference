# Get Document Metadata with CustomGPT.ai

Retrieves document metadata from a CustomGPT.ai agent.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/pages/:pageId/metadata`
- **Base URL:** `https://app.customgpt.ai/api/v1`
- **Official documentation:** [Get Document Metadata](https://docs.customgpt.ai/reference/get_api-v1-projects-projectid-pages-pageid-metadata-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project ID of the agent. |
| `pageId` | path | `number` | yes | The document page ID. |
