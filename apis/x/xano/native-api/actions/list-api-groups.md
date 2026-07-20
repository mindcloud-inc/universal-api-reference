# List API Groups with Xano

Finds API groups in a Xano workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api%3Ameta/workspace/:workspace_id/apigroup`
- **Base URL:** `https://x8ki-letl-twmt.n7.xano.io`
- **Official documentation:** [List API Groups](https://docs.xano.com/xano-features/metadata-api/instance_api/retrieve_a_list_of_api_groups_inside_of_a_workspace_use_the_optional_filtering_and_sorting_parameters_for_more_granular_returns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | path | `number` | yes | The Xano workspace ID. |
