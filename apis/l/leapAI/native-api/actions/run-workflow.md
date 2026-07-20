# Run Workflow with Leap AI

Runs a published workflow in Leap AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/runs`
- **Base URL:** `https://api.workflows.tryleap.ai`
- **Official documentation:** [Run Workflow](https://docs.tryleap.ai/api-reference/run-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | body | `string` | yes | The wkfv2_ identifier of the published workflow to run. |
| `trigger_id` | body | `string` | no | The trigger node ID used to start the workflow. |
| `webhook_url` | body | `string` | no | Optional URL that Leap calls when the workflow run finishes. |
| `input` | body | `object` | no | Optional object of workflow input variables. |
