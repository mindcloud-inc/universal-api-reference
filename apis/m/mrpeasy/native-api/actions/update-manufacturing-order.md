# Update Manufacturing Order with MRPeasy

Updates an existing manufacturing order in MRPeasy.

## Endpoint

- **Method:** `PUT`
- **Path:** `/manufacturing-orders/{{manOrdId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Update Manufacturing Order](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `man_ord_id` | path | `number` | yes | MRPeasy manufacturing order ID. |
| `quantity` | body | `number` | no | Updated manufacturing quantity. |
| `assigned_id` | body | `number` | no | Updated MRPeasy assigned user ID. |
