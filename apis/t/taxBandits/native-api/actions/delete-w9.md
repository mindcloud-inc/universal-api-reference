# Delete W-9 with TaxBandits

Deletes a W-9 from TaxBandits.

## Endpoint

- **Method:** `DELETE`
- **Path:** `FormW9/Delete`
- **Base URL:** `https://testapi.taxbandits.com/v1.7.3/`
- **Official documentation:** [Delete W-9](https://developer.taxbandits.com/docs/formw9/delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | query | `string` | no | Payee email. |
| `PayeeRef` | query | `string` | no | Payee reference. |
| `SubmissionId` | query | `string` | no | Submission identifier. |
