# Delete Workflow with Skyvern

Deletes an existing workflow from Skyvern.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/workflows/:workflow_id/delete`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Delete Workflow](https://www.skyvern.com/docs/api-reference/workflows/delete-a-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | The ID of the workflow to delete. Workflow ID starts with wpid_. |
