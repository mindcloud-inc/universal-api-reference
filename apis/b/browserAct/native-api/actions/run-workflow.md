# Run Workflow with BrowserAct

Creates a new task in BrowserAct from a workflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/run-task`
- **Base URL:** `https://api.browseract.com/v2/workflow`
- **Official documentation:** [Run Workflow](https://docs.browseract.com/api-reference/tasks/run-a-workflow-create-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | body | `string` | yes | The published BrowserAct workflow ID to run. |
| `input_parameters` | body | `string` | no | Optional JSON array of {"name","value"} objects matching the workflow input parameters. |
| `save_browser_data` | body | `boolean` | no | Whether BrowserAct should return a reusable browser profile for this run. |
| `profile_id` | body | `string` | no | Optional BrowserAct profile ID to reuse cookies and browser state. |
| `callback_url` | body | `string` | no | Optional webhook URL to receive the completed task result. |
| `status_change_callback_url` | body | `string` | no | Optional webhook URL to receive task status change events. |
