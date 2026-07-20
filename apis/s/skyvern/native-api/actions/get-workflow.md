# Get Workflow with Skyvern

Retrieves a workflow by permanent ID from Skyvern.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/workflows/:workflow_permanent_id`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Get Workflow](https://www.skyvern.com/docs/api-reference/workflows)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template` | query | `boolean` | no |
| `version` | query | `string` | no |
| `workflow_permanent_id` | path | `string` | yes |
