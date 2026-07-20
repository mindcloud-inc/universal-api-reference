# Get Customer Wallet with mittwald

Retrieves a customer's wallet from mittwald API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/customers/:customerId/wallet`
- **Base URL:** `https://api.mittwald.de`
- **Official documentation:** [Get Customer Wallet](https://api.mittwald.de/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | yes | The unique identifier of the customer. |
