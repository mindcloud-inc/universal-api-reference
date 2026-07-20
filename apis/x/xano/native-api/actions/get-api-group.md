# Get API Group with Xano

Retrieves an API group from Xano by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup/:apigroup_id`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [Get API Group](https://docs.xano.com/xano-features/metadata-api/instance_api/get_detailed_information_for_a_specific_api_group_returns_complete_metadata_and_configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apigroup_id` | path | `number` | yes | The Xano API group ID. |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
