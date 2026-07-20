# Chat with Deepset

Chats with a Deepset pipeline using one or more queries.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/chat`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Chat](https://docs.cloud.deepset.ai/docs/api/main/chat-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-chat-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
| `pipeline_name` | path | `string` | yes | deepset pipeline name. |
| `queries[]` | body | `array<string>` | yes | Queries to send to the chat pipeline. |
| `search_session_id` | body | `string` | yes | Search session ID required by deepset chat pipelines. |
