# Create Workflow with Skyvern

Creates a new workflow in Skyvern.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/workflows`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Create Workflow](https://www.skyvern.com/docs/api-reference/workflows/create-a-new-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folder_id` | query | `string` | no | Optional folder ID to assign the workflow to |
| `json_definition` | body | `object` | no | Workflow definition in JSON format |
| `yaml_definition` | body | `string` | no | Workflow definition in YAML format |
