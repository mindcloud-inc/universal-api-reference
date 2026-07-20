# List Customer Extension Orders with mittwald

Retrieves customer extension orders from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/extension-orders`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Customer Extension Orders](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The unique identifier of the customer. |
