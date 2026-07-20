# Assign Customer with Landbot

Assigns a customer in Landbot.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/customers/:customer_id/assign/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [Assign Customer](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idAssign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `number` | yes | Customer ID to assign. |
