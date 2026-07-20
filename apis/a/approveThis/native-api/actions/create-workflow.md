# Create Workflow with ApproveThis

Creates a workflow from an ApproveThis template.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/:template/workflow`
- **Base URL:** `https://app.approvethis.com/api/v1`
- **Official documentation:** [Create Workflow](https://app.approvethis.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template` | path | `string` | yes | The template slug. |
