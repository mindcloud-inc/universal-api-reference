# Get Patient Invoice with Cerbo

Retrieves patient invoice details from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/:invoice_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Patient Invoice](https://docs.cer.bo/#tag/Patient-Invoices/operation/showPatientInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `number` | no | ID of invoice |
