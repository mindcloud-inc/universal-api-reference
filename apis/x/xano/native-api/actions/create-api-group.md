# Create API Group with Xano

Creates a new API group in a Xano workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Create API Group](https://docs.xano.com/xano-features/metadata-api/instance_api/create_a_new_api_group_in_a_workspace_include_name_description_and_optional_tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | yes | API group description. |
| `name` | body | `string` | yes | API group name. |
| `swagger` | body | `boolean` | yes | Whether Swagger/OpenAPI is enabled for the API group. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
