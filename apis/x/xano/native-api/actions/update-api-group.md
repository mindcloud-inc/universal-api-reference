# Update API Group with Xano

Updates an existing API group in Xano.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Update API Group](https://docs.xano.com/xano-features/metadata-api/instance_api/update_an_existing_api_group_modify_name_description_documentation_settings_or_tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apigroup_id` | path | `number` | yes | The Xano API group ID. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
