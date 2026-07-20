# Create Agent with CustomGPT.ai

Creates a new agent in CustomGPT.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://app.customgpt.ai/api/v1`
- **Official documentation:** [Create Agent](https://docs.customgpt.ai/reference/post_api-v1-projects)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_name` | body | `string` | yes | Name for the temporary agent used during pagination remediation. |
| `sitemap_path` | body | `string` | yes | Source URL used to initialize the temporary agent. |
