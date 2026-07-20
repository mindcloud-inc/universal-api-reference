# List Invoices with Chargback

Retrieves billing invoice records from Chargback.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/v1/invoices/`
- **Base URL:** `https://api.chargeback.io`
- **Official documentation:** [List Invoices](https://api.chargeback.io/api/public/docs/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `page_size` | query | `number` | no |
| `ordered_by` | query | `string` | no |
| `status` | query | `string` | no |
| `business_account` | query | `string` | no |
