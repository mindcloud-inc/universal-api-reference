# Get Customer Billing Portal with mittwald

Retrieves a customer billing portal link from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/billing-portal`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Customer Billing Portal](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The unique identifier of the customer. |
