# Get Purchase Order with MRPeasy

Retrieves a purchase order from MRPeasy.

## Endpoint

- **Method:** `GET`
- **Path:** `/purchase-orders/{{purOrdId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Get Purchase Order](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pur_ord_id` | path | `number` | yes | MRPeasy purchase order ID. |
