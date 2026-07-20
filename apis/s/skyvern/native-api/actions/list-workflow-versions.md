# List Workflow Versions with Skyvern

Retrieves all versions of a workflow from Skyvern.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/workflows/:workflow_permanent_id/versions`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [List Workflow Versions](https://www.skyvern.com/docs/api-reference/workflows)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template` | query | `boolean` | no |
| `workflow_permanent_id` | path | `string` | yes |
