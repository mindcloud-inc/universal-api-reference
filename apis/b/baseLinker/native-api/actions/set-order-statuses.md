# Set Order Statuses with BaseLinker

Updates multiple order statuses in BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Set Order Statuses](https://api.baselinker.com/index.php?method=setOrderStatuses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_ids[]` | body | `array<number>` | yes | Array of order identifiers to update. |
| `status_id` | body | `number` | yes | Status identifier to assign to every listed order. |
| `parameters` | body | `object` | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |
