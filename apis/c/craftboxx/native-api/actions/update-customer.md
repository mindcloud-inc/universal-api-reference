# Update Customer with Craftboxx

Updates a customer in Craftboxx.

## Endpoint

- **Method:** `PUT`
- **Path:** `customers/:customerId`
- **Base URL:** `https://api.craftboxx.de`
- **Official documentation:** [Update Customer](https://api.craftboxx.de/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | The Craftboxx customer ID. |
| `name` | body | `string` | no | The customer name. |
