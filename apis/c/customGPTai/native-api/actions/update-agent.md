# Update Agent with CustomGPT.ai

Updates an existing agent in CustomGPT.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://app.customgpt.ai/api/v1`
- **Official documentation:** [Update Agent](https://docs.customgpt.ai/reference/post_api-v1-projects-projectid-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project ID of the agent to update. |
| `project_name` | body | `string` | yes | The updated name for the agent. |
