# List Customer Contracts with mittwald

Retrieves customer contracts from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/contracts`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Customer Contracts](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The unique identifier of the customer. |
