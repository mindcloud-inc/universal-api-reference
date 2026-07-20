# Schedule Workflow with Kadoa

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/workflows/:workflowId/schedule`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Schedule Workflow](https://docs.kadoa.com/api-reference/workflows/schedule-a-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | Workflow ID |
| `date` | body | `string` | yes | ISO 8601 UTC date |
