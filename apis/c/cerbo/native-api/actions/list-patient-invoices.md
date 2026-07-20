# List Patient Invoices with Cerbo

Retrieves patient invoices from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:patient_id/invoices`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Patient Invoices](https://docs.cer.bo/#tag/Patient-Invoices/operation/listPatientInvoices)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `patient_id` | path | `number` | no | ID of patient |
