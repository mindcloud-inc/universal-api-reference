# Delete API with Xano

Deletes an existing API endpoint from Xano.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api/:api_id`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Delete API](https://docs.xano.com/xano-features/metadata-api/instance_api/delete_an_api_endpoint_permanently_this_action_cannot_be_undone)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_id` | path | `number` | yes | The Xano API ID. |
| `apigroup_id` | path | `number` | yes | The Xano API group ID. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
