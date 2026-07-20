# Add Offline Order with Billetweb

Creates a new offline order in Billetweb.

## Endpoint

- **Method:** `POST`
- **Path:** `/event/:id/add_order`
- **Base URL:** `https://www.billetweb.fr/api`
- **Official documentation:** [Add Offline Order](https://www.billetweb.fr/bo/api.php#/api/event/:id/add_order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Event identifier that will receive offline orders. |
| `data[]` | body | `array<object>` | yes | Array of offline order objects to add. |
