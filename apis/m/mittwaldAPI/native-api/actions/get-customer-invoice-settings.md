# Get Customer Invoice Settings with mittwald

Retrieves customer invoice settings from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/invoice-settings`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Customer Invoice Settings](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The unique identifier of the customer. |
