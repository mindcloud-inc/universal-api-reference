# List Receipts with Quaderno

Retrieves receipts from Quaderno.

## Endpoint

- **Method:** `GET`
- **Path:** `/receipts`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [List Receipts](https://developers.quaderno.io/api/#tag/Receipts/operation/listReceipts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | query | `string` | no | Filter receipts by contact ID. |
| `date` | query | `string` | no | Filter receipts by issue date range. |
| `processor_id` | query | `string` | no | Filter receipts by processor ID. |
| `q` | query | `string` | no | Filter receipts by number, customer name, or PO number. |
| `state` | query | `string` | no | Filter receipts by state. |
