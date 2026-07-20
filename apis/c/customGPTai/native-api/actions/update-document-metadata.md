# Update Document Metadata with CustomGPT.ai

Updates document metadata in a CustomGPT.ai agent.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId/pages/:pageId/metadata`
- **Base URL:** `https://app.customgpt.ai/api/v1`
- **Official documentation:** [Update Document Metadata](https://docs.customgpt.ai/reference/put_api-v1-projects-projectid-pages-pageid-metadata-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project ID of the agent. |
| `pageId` | path | `number` | yes | The document page ID. |
| `title` | body | `string` | yes | The updated document title. |
