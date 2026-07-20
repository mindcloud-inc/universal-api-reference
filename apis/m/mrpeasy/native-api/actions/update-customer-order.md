# Update Customer Order with MRPeasy

Updates an existing customer order in MRPeasy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customer-orders/{{custOrdId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Update Customer Order](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cust_ord_id` | path | `number` | yes | MRPeasy customer order ID. |
| `reference` | body | `string` | no | Updated customer order reference. |
| `products` | body | `array<object>` | no | Updated MRPeasy order line array. |
