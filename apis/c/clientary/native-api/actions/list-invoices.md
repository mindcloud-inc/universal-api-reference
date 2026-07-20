# List Invoices with Clientary

Retrieves invoices from your Clientary account.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [List Invoices](https://www.clientary.com/api/invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `updated_since` | query | `string` | no | Return only invoices updated after this timestamp. |
