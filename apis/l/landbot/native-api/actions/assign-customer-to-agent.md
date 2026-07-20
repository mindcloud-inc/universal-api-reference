# Assign Customer to Agent with Landbot

Assigns a customer to an agent in Landbot.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/customers/:customer_id/assign/:agent_id/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [Assign Customer to Agent](https://api.landbot.io/#api-Customers-PutHttpsApiLandbotIoV1CustomersCustomer_idAssignAgent_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `number` | yes | Customer ID to assign. |
| `agent_id` | path | `number` | yes | Agent ID to assign the customer to. |
