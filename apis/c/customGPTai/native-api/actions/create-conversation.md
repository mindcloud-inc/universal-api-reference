# Create Conversation with CustomGPT.ai

Creates a new conversation in a CustomGPT.ai agent.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/conversations`
- **Base URL:** `https://app.customgpt.ai/api/v1`
- **Official documentation:** [Create Conversation](https://docs.customgpt.ai/reference/post_api-v1-projects-projectid-conversations-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project ID of the agent. |
| `name` | body | `string` | yes | The conversation name. |
