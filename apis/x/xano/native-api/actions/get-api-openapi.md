# Get API OpenAPI with Xano

Retrieves an OpenAPI specification for a Xano API endpoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/api/:api_id/openapi`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Get API OpenAPI](https://docs.xano.com/xano-features/metadata-api/instance_api/generate_openapi_specification_for_a_specific_api_endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_id` | path | `number` | yes | The Xano API ID. |
| `apigroup_id` | path | `number` | yes | The Xano API group ID. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
