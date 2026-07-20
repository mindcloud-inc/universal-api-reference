# Create a workflow with Pipedream

Creates a new workflow in Pipedream.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Create a workflow](https://pipedream.com/docs/rest-api/api-reference/workflows/create-a-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | body | `string` | yes | The workspace organization ID where the workflow will be created. |
| `project_id` | body | `string` | yes | The project ID where the new workflow will be created. |
| `settings` | body | `object` | yes | Workflow settings such as name and auto_deploy. |
| `steps[]` | body | `array<object>` | yes | Definitions of the workflow steps, including namespace and props. |
| `template_id` | body | `string` | yes | The workflow template ID to base the new workflow on. |
| `triggers[]` | body | `array<object>` | yes | Definitions of the workflow triggers and their props. |
