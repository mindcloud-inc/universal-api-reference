# Get customer order with MoySklad

Retrieves the customer order from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `entity/customerorder/:id`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Get customer order](https://dev.moysklad.ru/doc/api/remap/1.2/documents/#dokumenty-zakaz-pokupatelia)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | MoySklad customer order ID. |
