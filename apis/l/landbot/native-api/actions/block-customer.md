# Block Customer with Landbot

Blocks a customer in Landbot.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/customers/:customer_id/block/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [Block Customer](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idBlock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `number` | yes | Customer ID to block. |
