# Get Query Set with Deepset

Retrieves a query set from a Deepset workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/workspaces/:workspace_id/query_sets/:query_set_id`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Query Set](https://docs.cloud.deepset.ai/docs/api/jobs/get-query-set-api-v-2-workspaces-workspace-id-query-sets-query-set-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query_set_id` | path | `string` | yes | deepset query set ID. |
| `workspace_id` | path | `string` | yes | deepset workspace ID. |
