# Assign Customer to Bot with Landbot

Assigns a customer to a bot in Landbot.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/customers/:customer_id/assign_bot/:bot_id/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [Assign Customer to Bot](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idAssign_botBot_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `number` | yes | Customer ID to assign. |
| `bot_id` | path | `number` | yes | Bot ID to assign the customer to. |
