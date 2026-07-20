# List Patient Estimates with Cerbo

Retrieves patient estimates from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:pt_id/estimates`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Estimates](https://docs.cer.bo/#tag/Patient-Charges/operation/listAllPatientEstimates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pt_id` | path | `number` | no | — |
| `date_method` | query | `string` | no | If you're filtering by date range, should the range be calculated by date the estimated charge was created, or the recorded transaction date (manual date assigned to the estimated charge)? Valid arguments are *created* and *transaction* (created is the default). |
| `start_date` | query | `date` | no | If this argument is included it will only show estimated charges from after this date (calculated by `date_method`). |
| `end_date` | query | `date` | no | If this argument is included it will only show estimated charges from before this date (calculated by `date_method`). |
