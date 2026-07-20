# Create API with Xano

Creates a new API endpoint in Xano.

## Endpoint

- **Method:** `POST`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Create API](https://docs.xano.com/xano-features/metadata-api/instance_api/create_a_new_api_endpoint_using_xanoscript)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apigroup_id` | path | `number` | yes | The Xano API group ID. |
| `description` | body | `string` | yes | API endpoint description. |
| `name` | body | `string` | yes | API endpoint name. |
| `verb` | body | `string` | yes | HTTP verb for the endpoint. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
