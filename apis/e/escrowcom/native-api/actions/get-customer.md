# Get Customer with Escrow.com

Retrieves a customer from Escrow.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/customer/:customer_id`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Get Customer](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `number` | yes | Escrow.com customer ID. Use `me` through the separate Get Current Customer action. |
