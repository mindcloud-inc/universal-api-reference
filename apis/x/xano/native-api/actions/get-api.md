# Get API with Xano

Retrieves an API endpoint from Xano by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api/:api_id`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Get API](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_a_specific_api_endpoint_by_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_id` | path | `number` | yes | The Xano API ID. |
| `apigroup_id` | path | `number` | yes | The Xano API group ID. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
