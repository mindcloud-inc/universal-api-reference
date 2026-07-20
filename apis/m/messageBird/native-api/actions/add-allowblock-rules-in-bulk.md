# Add Allow/Block Rules in Bulk with MessageBird

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/conversation-allowblock-rules-bulk`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Add Allow/Block Rules in Bulk](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/add-allow-block-rules-in-bulk)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/csv` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID where the bulk allow/block upload should run. |
