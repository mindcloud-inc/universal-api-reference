# List Customer Invoices with mittwald

Retrieves customer invoices from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/invoices`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Customer Invoices](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The unique identifier of the customer. |
