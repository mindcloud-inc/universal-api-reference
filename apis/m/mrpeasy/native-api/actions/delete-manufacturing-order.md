# Delete Manufacturing Order with MRPeasy

Cancels an existing manufacturing order in MRPeasy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/manufacturing-orders/{{manOrdId}}`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Delete Manufacturing Order](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `man_ord_id` | path | `number` | yes | MRPeasy manufacturing order ID. |
