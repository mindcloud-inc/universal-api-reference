# Run Official Workflow Template with BrowserAct

Creates a new task in BrowserAct from an official workflow template.

## Endpoint

- **Method:** `POST`
- **Path:** `/run-task-by-template`
- **Base URL:** `https://api.browseract.com/v2/workflow`
- **Official documentation:** [Run Official Workflow Template](https://docs.browseract.com/api-reference/tasks/run-an-official-workflow-template-create-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_template_id` | body | `string` | yes | The official BrowserAct workflow template ID to run. |
| `proxyRegion` | body | `string` | no | Optional BrowserAct proxy region code. Defaults to US. |
| `input_parameters` | body | `string` | no | Optional JSON array of {"name","value"} objects matching the template input parameters. |
| `callback_url` | body | `string` | no | Optional webhook URL to receive the completed task result. |
| `status_change_callback_url` | body | `string` | no | Optional webhook URL to receive task status change events. |
