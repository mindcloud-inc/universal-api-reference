# Get API Group OpenAPI with Xano

Retrieves an OpenAPI specification for a Xano API group.

## Endpoint

- **Method:** `GET`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id/openapi`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Get API Group OpenAPI](https://docs.xano.com/xano-features/metadata-api/instance_api/get_the_openapi_specification_for_an_api_group_returns_the_complete_swagger_json_for_all_endpoints)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apigroup_id` | path | `number` | yes | The Xano API group ID. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
