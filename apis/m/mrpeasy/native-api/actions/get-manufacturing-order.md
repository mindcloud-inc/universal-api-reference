# Get Manufacturing Order with MRPeasy

Retrieves a manufacturing order from MRPeasy.

## Endpoint

- **Method:** `GET`
- **Path:** `/manufacturing-orders/{{manOrdId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Get Manufacturing Order](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `man_ord_id` | path | `number` | yes | MRPeasy manufacturing order ID. |
