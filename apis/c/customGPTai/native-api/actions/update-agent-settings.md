# Update Agent Settings with CustomGPT.ai

Updates current agent settings in CustomGPT.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/settings`
- **Base URL:** `https://app.customgpt.ai/api/v1`
- **Official documentation:** [Update Agent Settings](https://docs.customgpt.ai/reference/post_api-v1-projects-projectid-settings-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project ID of the agent. |
| `default_prompt` | body | `string` | no | The default prompt shown for the agent. |
| `response_source` | body | `string` | no | How the agent should cite or source responses. |
| `chatbot_msg_lang` | body | `string` | no | The language code used for chatbot UI messages. |
