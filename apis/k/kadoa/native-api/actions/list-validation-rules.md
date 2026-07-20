# List Validation Rules with Kadoa

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/data-validation/rules`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [List Validation Rules](https://docs.kadoa.com/api-reference/data-validation/list-rules)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number |
| `pageSize` | query | `number` | no | Results per page |
| `status` | query | `string` | no | Status: preview, enabled, disabled |
| `workflowId` | query | `string` | no | Filter by workflow ID |
