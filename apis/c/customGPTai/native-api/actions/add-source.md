# Add Source with CustomGPT.ai

Adds a new source to a CustomGPT.ai agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/sources`
- **Base URL:** `https://app.customgpt.ai/api/v1`
- **Official documentation:** [Add Source](https://docs.customgpt.ai/reference/post_api-v1-projects-projectid-sources-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project ID of the agent. |
| `sitemap_path` | body | `string` | yes | The sitemap URL to add as a source. |
