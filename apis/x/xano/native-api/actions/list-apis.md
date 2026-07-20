# List APIs with Xano

Finds API endpoints in a Xano API group.

## Endpoint

- **Method:** `GET`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [List APIs](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_all_api_endpoints_in_a_group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apigroup_id` | path | `number` | yes | The Xano API group ID. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
