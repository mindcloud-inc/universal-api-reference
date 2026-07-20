# List Customer Memberships with mittwald

Retrieves customer memberships from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/memberships`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [List Customer Memberships](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The unique identifier of the customer. |
