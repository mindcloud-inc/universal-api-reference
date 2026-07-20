# Update Workflow with Skyvern

Updates an existing workflow in Skyvern.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/workflows/:workflow_id`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Update Workflow](https://www.skyvern.com/docs/api-reference/workflows/update-a-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `json_definition` | body | `object` | no | Workflow definition in JSON format |
| `workflow_id` | path | `string` | yes | The ID of the workflow to update. Workflow ID starts with wpid_. |
| `yaml_definition` | body | `string` | no | Workflow definition in YAML format |
