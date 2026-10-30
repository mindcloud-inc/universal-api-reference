# List Workflow Submissions with GoCanvas

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/submissions`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [List Workflow Submissions](https://api.gocanvas.com/api/v3/docs#list-workflow-submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | query | `number` | no | Restrict results to submissions and assignments on this form. |
| `workflow_id` | query | `number` | no | Restrict results to submissions routed through this workflow. |
