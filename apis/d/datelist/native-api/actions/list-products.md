# List Products with Datelist

Retrieves available products from Datelist by name or calendar.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://datelist.io/api`
- **Official documentation:** [List Products](https://apidoc.datelist.io/products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Only return products matching a specific name. |
| `calendar_id` | query | `number` | no | Only return products for a specific calendar. |
