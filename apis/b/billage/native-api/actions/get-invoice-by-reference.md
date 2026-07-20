# Get Invoice by Reference with Billage

Retrieves an invoice from Billage by reference code.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/invoices/by-ref`
- **Base URL:** `https://app.getbillage.com/api`
- **Official documentation:** [Get Invoice by Reference](https://app.getbillage.com/api/documentation.html#/Invoices/invoicesListByReference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | query | `number` | no | Invoice year |
| `serie` | query | `string` | yes | Invoice serie |
| `ref` | query | `string` | yes | Invoice reference |
