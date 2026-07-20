# Get Run Status with Comfy.ICU

Retrieves a workflow run status from Comfy.ICU.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workflows/:workflow_id/runs/:run_id`
- **Base URL:** `https://comfy.icu`
- **Official documentation:** [Get Run Status](https://comfy.icu/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | Comfy.ICU workflow ID from the workflow page or API code snippet. |
| `run_id` | path | `string` | yes | Run ID returned by the Run Workflow action. |
