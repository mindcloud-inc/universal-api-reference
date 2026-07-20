# Get Order Payments History with BaseLinker

Retrieves payment history for an order in BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Get Order Payments History](https://api.baselinker.com/index.php?method=getOrderPaymentsHistory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `number` | yes | Order identifier from BaseLinker order manager. |
| `show_full_history` | body | `boolean` | no | Include full payment history, including manual edits and value changes. |
