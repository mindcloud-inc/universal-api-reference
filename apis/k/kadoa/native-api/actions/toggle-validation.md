# Toggle Validation with Kadoa

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/data-validation/workflows/:workflowId/validation/toggle`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Toggle Validation](https://docs.kadoa.com/api-reference/data-validation/toggle-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | body | `boolean` | yes | Enable or disable |
| `workflowId` | path | `string` | yes | Workflow ID |
