# Get Validation Results with Kadoa

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/data-validation/workflows/:workflowId/jobs/:jobId/validations/latest`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Get Validation Results](https://docs.kadoa.com/api-reference/data-validation/latest-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeDryRun` | query | `boolean` | no | Include dry run results |
| `jobId` | path | `string` | yes | Job ID |
| `workflowId` | path | `string` | yes | Workflow ID |
