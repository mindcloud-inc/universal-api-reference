# Get Invoice with Clientary

Retrieves an invoice from Clientary by invoice ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/:id`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Get Invoice](https://www.clientary.com/api/invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Clientary invoice ID. |
