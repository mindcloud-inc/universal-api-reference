# Get Allow/Block Bulk Upload Status with MessageBird

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/:workspaceId/conversation-allowblock-rules-bulk/:bulkId/status`
- **Base URL:** `https://api.bird.com`
- **Official documentation:** [Get Allow/Block Bulk Upload Status](https://docs.bird.com/api/conversations-api/api-reference/workspace-settings/get-allow-block-bulk-upload-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The Bird workspace ID that owns the bulk upload. |
| `bulkId` | path | `string` | yes | The Bird bulk upload ID to inspect. |
