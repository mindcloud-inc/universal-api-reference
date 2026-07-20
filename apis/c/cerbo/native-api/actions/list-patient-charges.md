# List Patient Charges with Cerbo

Retrieves patient charges from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:pt_id/charges`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Charges](https://docs.cer.bo/#tag/Charges/operation/listPatientCharges)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pt_id` | path | `number` | yes | The ID of the patient. |
| `date_method` | query | `string` | no | If you're filtering by date range, should the range be calculated by date the charge was created, or the recorded transaction date? Valid arguments are 'created' and 'transaction' (created is the default). |
| `start_date` | query | `string` | no | Show charges from after this date (calculated by date_method). |
| `end_date` | query | `string` | no | Show charges from before this date (calculated by date_method). |
