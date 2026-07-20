# Get Customer Order with MRPeasy

Retrieves a customer order from MRPeasy.

## Endpoint

- **Method:** `GET`
- **Path:** `/customer-orders/{{custOrdId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Get Customer Order](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cust_ord_id` | path | `number` | yes | MRPeasy customer order ID. |
