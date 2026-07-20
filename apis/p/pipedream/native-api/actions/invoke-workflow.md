# Invoke workflow with Pipedream

Invokes a workflow run in Pipedream.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows/{workflow_id}/invoke`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Invoke workflow](https://pipedream.com/docs/rest-api/api-reference/workflows/invoke-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | The workflow identifier. |
