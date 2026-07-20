# Get Workflow Data with Kadoa

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/workflows/:workflowId/data`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Get Workflow Data](https://docs.kadoa.com/api-reference/workflows/get-workflow-data-by-id)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflowId` | path | `string` | yes | Workflow ID |
| `format` | query | `list` | no | Response format: json or csv Accepted values: `csv`, `json`. |
| `page` | query | `number` | no | Page number |
| `runId` | query | `string` | no | Specific run ID |
| `rowIds` | query | `string` | no | Filter output to specific row IDs. |
| `includeAnomalies` | query | `boolean` | no | Include anomalies in response. |
| `gzip` | query | `boolean` | no | Return gzip-compressed payload. |
